🍔 OOP Food Delivery System

A simple Object-Oriented Programming (OOP) Food Delivery System built with Python and a Streamlit web interface.

📌 Project Overview

This project simulates a basic food delivery workflow:

Register a customer

Register a delivery partner

Create a restaurant

Add food items to the restaurant menu

Add money to the customer's wallet

Place a food order

Calculate the bill

Accept the order by a delivery partner

Verify OTP

Complete the delivery

Send delivery notifications

🛠️ Technologies Used

Python

Object-Oriented Programming (OOP)

Streamlit

ABC / Abstract Base Class

📂 Project Structure

food-delivery/
│
├── food_delivery.py
├── food_delivery_app.py
├── demo.py
├── requirements.txt
└── README.md

File

Description

food_delivery.py

Main OOP classes and business logic

food_delivery_app.py

Streamlit user interface

demo.py

Complete demonstration workflow

requirements.txt

Project dependency

README.md

Project documentation

🧱 OOP Classes

User

User is an abstract base class. It contains common user information such as name, phone, and wallet balance. It also defines the abstract methods notify() and display_profile().

Customer

Customer inherits from User. A customer can add money to the wallet, place orders, display a profile, and receive notifications.

Example:

priya = Customer("Priya", "9876543210", "Bangalore")

DeliveryPartner

DeliveryPartner inherits from User. A delivery partner can accept orders, deliver orders using OTP verification, display a profile, and receive notifications.

Example:

rajesh = DeliveryPartner("Rajesh", "9123456780", "Bike")

MenuItem

MenuItem represents a food item and stores its name, price, and vegetarian/non-vegetarian information.

biryani = MenuItem("Biryani", 250, False)

Restaurant

Restaurant stores restaurant information and its menu. It can add menu items, return the menu, and check whether the restaurant is open.

bawarchi = Restaurant("Bawarchi", "MG Road")
bawarchi.add_item(biryani)

Order

Order manages the order ID, items, status, OTP, bill calculation, estimated delivery time, and OTP verification.

💰 Bill Calculation

The project uses:

Subtotal
+ GST (5%)
+ Packaging Fee
----------------
Total

For the demo:

Biryani = ₹250
Kebab   = ₹150

Subtotal      = ₹400
GST (5%)      = ₹20
Packaging Fee = ₹20
Total         = ₹440

🚀 Demo Flow

demo.py demonstrates the complete workflow:

1. Register Customer

priya = Customer("Priya", "9876543210", "Bangalore")

2. Register Delivery Partner

rajesh = DeliveryPartner("Rajesh", "9123456780", "Bike")

3. Create Restaurant

bawarchi = Restaurant("Bawarchi", "MG Road")

Biryani and Kebab are added to the menu.

4. Wallet

Priya adds ₹500 and then attempts a negative top-up of -₹100.

5. Place Order

Priya orders Biryani and Kebab.

6. Bill

The demo prints subtotal, GST, packaging fee, total, and estimated delivery time.

7. Delivery

Rajesh accepts the order. The demo tries the wrong OTP 9999 and then the correct OTP 1234.

8. Notifications

priya.notify("Order delivered")
rajesh.notify("Order delivered")

▶️ How to Run Locally

1. Clone the repository

git clone <YOUR_GITHUB_REPOSITORY_URL>
cd food-delivery

2. Install dependencies

pip install -r requirements.txt

Or:

pip install streamlit

3. Run the demo

python demo.py

4. Run the Streamlit application

streamlit run food_delivery_app.py

🌐 Deploy on Streamlit Community Cloud

Push all project files to GitHub.

Create a new Streamlit app.

Select your GitHub repository and main branch.

Select food_delivery_app.py as the main file.

Deploy the application.

Make sure these files are in the repository:

food_delivery.py
food_delivery_app.py
requirements.txt
README.md

🔄 Application Flow

Customer Registration
        ↓
Wallet Top-up
        ↓
Restaurant Menu
        ↓
Place Order
        ↓
Order Created
        ↓
Delivery Partner
        ↓
Accept Order
        ↓
OTP Verification
        ↓
Delivery Completed
        ↓
Notifications

🎯 Learning Objectives

This project demonstrates:

Classes and Objects

Constructors

Inheritance

Abstraction

Abstract Base Classes

Encapsulation

Method Overriding

Instance Attributes

Class Attributes

Lists and Dictionaries

Python Modules and Imports

Streamlit UI

👩‍💻 Author

Mayuri Singal

Data Analytics Learner | Python | SQL | Excel | Power BI | Tableau

GitHub: MayuriRajput239

⭐ Project Purpose

This project was created as an OOP practice project to understand how Python classes can be connected to model a real-world food delivery system.
