# B2B-Ecommerce-Fraud-Case-Study
B2B Ecommerce Fraud: Case Study
ABC Company operates an e-commerce platform and processes thousands of orders daily. To deliver these orders, ABC has partnered with several courier companies in India, which charge them based on the weight of the products and the distance between the warehouse and the customer’s delivery address. ABC wants to check if the fees charged by the courier companies for each order are correct.

ABC has internal data split across three reports: Website Order Report, Master SKU, and Warehouse PIN for all India Pincode mappings. In addition, they receive billing data from courier companies.

The website order report includes order IDs and products (SKUs) for each order. The SKU master provides the gross weight of each product, which is needed to calculate the total weight of each order. Courier company invoices contain information such as AWB number, order ID, shipment weight, warehouse pickup PIN, customer delivery PIN, delivery area, the charge per shipment and type of shipment.

ABC wants to compare the total weight of each order calculated using the SKU master with the weight stated by the courier company in their invoice. The weight should be rounded up to the nearest multiple of 0.5 kg to determine the weight of the tile. The warehouse PIN to all India Pincode mappings is used to determine the delivery area, which should be compared to the area reported by the courier company.

In addition, ABC must apply the logic of calculating charges based on the slab weight, delivery area and type of shipment listed on the courier company’s invoice. The courier fee rate card provides a fixed fee and an additional fee for each weight plate and PIN. The total charge per shipment should be calculated by adding the fixed charge and any additional charges based on plate weight.

##INTRODUCTION
In today’s fast-paced e-commerce industry, fast and efficient order delivery is crucial to business success. To ensure seamless order fulfilment, businesses often partner with courier companies to ship their products to customers. However, managing the charges collected by these courier companies can be difficult, especially when dealing with a high volume of orders. It is one of the real-time problems B2B businesses experience when their estimated charges for the same invoice don’t match. In this article, I will take you through a solution to one such problem statement based on B2B Courier Charges Accuracy Analysis using Python.
B2B Courier Charges Accuracy Analysis
B2B courier charges accuracy analysis focuses on assessing the accuracy of fees charged by courier companies for the delivery of goods in B2B transactions. The aim is to ensure that companies are billed appropriately for the services provided by courier companies.

It is one of the problems that will help you use most of your skills in working with data. You can find the dataset I will use to solve this problem along with the complete problem statement here.

Now in the section below, I’ll take you through the task of B2B Courier Charges Accuracy Analysis using the Python programming language.

B2B Courier Charges Accuracy Analysis using Python
Let’s start this task by importing the necessary Python libraries and the dataset:
import pandas as pd

order_report = pd.read_csv('Order Report.csv')
sku_master = pd.read_csv('SKU Master.csv')
pincode_mapping = pd.read_csv('pincodes.csv')
courier_invoice = pd.read_csv('Invoice.csv')
courier_company_rates = pd.read_csv('Courier Company - Rates.csv')

print("Order Report:")
print(order_report.head())
print("\nSKU Master:")
print(sku_master.head())
print("\nPincode Mapping:")
print(pincode_mapping.head())
print("\nCourier Invoice:")
print(courier_invoice.head())
print("\nCourier Company rates:")
print(courier_company_rates.head())
