# Online Book Store

Online book store using php, javascript, Mysql, Html, Css

### Introduction:
The online bookstore website is a dynamic and user-friendly platform designed to facilitate the purchase and exploration of a wide range of books. It was created using PHP as the server-side scripting language and MariaDB as the relational database management system, providing a seamless shopping experience for book enthusiasts.

### Features:
- Register and login
- Empty card at once
- Quantity selection of books
- Checkout and Payment
- Place order without login/Register
- Edit personal details
- Saving login, place order information,address,credit card information in MariaDB database

### Main Website Page

- Main Website Page

![image](https://github.com/AlpeshJasani/bookstore/assets/112234589/c60c851d-8e6e-46a7-b22d-b02176fe9ba8)

- Login Page

![image](https://github.com/AlpeshJasani/bookstore/assets/112234589/a8ed4729-2f4d-4762-a2fa-54ab158a3583)

- Register Page
  
![image](https://github.com/AlpeshJasani/bookstore/assets/112234589/338ead10-2fbf-442b-ad88-8cad5c54674f)

- Page after login

![image](https://github.com/AlpeshJasani/bookstore/assets/112234589/9809576e-f03e-4868-87ee-62e7fa009b45)

- Edit Profile Page

![image](https://github.com/AlpeshJasani/bookstore/assets/112234589/8a0f0bf3-1e14-464e-b183-e8f87db8ab24)

- Place Order with login

![image](https://github.com/AlpeshJasani/bookstore/assets/112234589/d016a76e-0903-4a45-ba9f-6b089f6b08ed)

- Place Order without login info

![image](https://github.com/AlpeshJasani/bookstore/assets/112234589/926317a4-3c37-446d-a679-1c355d0feab8)

### About Database
- 5 Tables:

**Book**(BookID varchar(50), BookTitle varchar(200), ISBN varchar(20), Price double(12,2), Author varchar(128), Type varchar(128), Image varchar(128), PRIMARY KEY (BookID) );

**Users**( UserID int not null AUTO_INCREMENT, UserName varchar(128), Password varchar(16), PRIMARY KEY (UserID) );

**Customer**( CustomerID int not null AUTO_INCREMENT, CustomerName varchar(128), CustomerPhone varchar(12), CustomerIC varchar(14), CustomerEmail varchar(200), CustomerAddress varchar(200), CustomerGender varchar(10), UserID int, PRIMARY KEY (CustomerID), CONSTRAINT FOREIGN KEY (UserID) REFERENCES Users(UserID) ON DELETE SET NULL ON UPDATE CASCADE );

**Order**( OrderID int not null AUTO_INCREMENT, CustomerID int, BookID varchar(50), DatePurchase datetime, Quantity int, TotalPrice double(12,2), Status varchar(1), PRIMARY KEY (OrderID), CONSTRAINT FOREIGN KEY (BookID) REFERENCES Book(BookID) ON DELETE SET NULL ON UPDATE CASCADE, CONSTRAINT FOREIGN KEY (CustomerID) REFERENCES Customer(CustomerID) ON DELETE SET NULL ON UPDATE CASCADE );

**Cart**( CartID int not null AUTO_INCREMENT, CustomerID int, BookID varchar(50), Price double(12,2), Quantity int, TotalPrice double(12,2), PRIMARY KEY (CartID), CONSTRAINT FOREIGN KEY (BookID) REFERENCES Book(BookID) ON DELETE SET NULL ON UPDATE CASCADE, CONSTRAINT FOREIGN KEY (CustomerID) REFERENCES Customer(CustomerID) ON DELETE SET NULL ON UPDATE CASCADE );






### Conclusion:
The online bookstore website built with PHP and MariaDB provides a user-friendly and secure platform for book lovers to explore, purchase, and manage their favorite books. With an extensive catalog, a seamless shopping experience, and robust user and admin features, this website caters to both book buyers and administrators, making it a valuable addition to the world of online bookstores. It combines the power of PHP for dynamic web functionality and MariaDB for efficient data management.

