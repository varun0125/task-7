# task-7

/*CREATE TABLE Users (
    user_id INT PRIMARY KEY,
    name VARCHAR(100),
    email VARCHAR(100)
);

CREATE TABLE Purchases (
    purchase_id INT PRIMARY KEY,
    user_id INT,
    product VARCHAR(100),
    amount DECIMAL(10,2),
    purchase_date DATE,
    FOREIGN KEY (user_id) REFERENCES Users(user_id)
);



INSERT INTO Users (user_id, name, email) VALUES
(1, 'Varun Sharma', 'varun@gmail.com'),
(2, 'Aman Verma', 'aman@gmail.com'),
(3, 'raju', 'raju@gmail.com');


INSERT INTO Purchases (purchase_id, user_id, product, amount, purchase_date) VALUES
(101, 1, 'Laptop', 60000.00, '2025-07-01'),
(102, 2, 'Keyboard', 1500.00, '2025-07-01'),
(103, 1, 'Mouse', 700.00, '2025-07-02'),
(104, 3, 'Monitor', 9000.00, '2025-07-03');

*/
CREATE VIEW UserPurchaseView AS
SELECT 
    u.name AS user_name,
    u.email,
    p.product,
    p.amount,
    p.purchase_date
FROM 
    Users u
JOIN 
    Purchases p ON u.user_id = p.user_id;
    
    SELECT * FROM UserPurchaseView;

