-- question1
SELECT paymentDate, SUM(amount) AS totalAmount
FROM payments
GROUP BY paymentDate
ORDER BY paymentDate DESC
LIMIT 5;

-- question2
SELECT customerName, country, AVG(creditLimit) AS averageCreditLimit
FROM customers
GROUP BY customerName, country;

-- question3
SELECT productCode, quantityOrdered, quantityOrdered * priceEach AS totalPrice
FROM orderdetails
GROUP BY productCode, quantityOrdered, priceEach;

-- question4
SELECT checkNumber, MAX(amount) AS highestAmount
FROM payments
GROUP BY checkNumber;
