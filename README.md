------------------------------------------------------------
Supermarket Management System (C# WinForms)
------------------------------------------------------------

This project is a desktop supermarket simulation application built in C# using WinForms,
designed to demonstrate Object-Oriented Programming (OOP) principles, inheritance hierarchies,
and UI-driven business logic.

The system models a real-world supermarket with categorized products, a shopping cart,
age-based restrictions, and a checkout flow.

## 📸 Screenshots

### Main Menu
![Main Menu](assets/screenshots/main-menu.png)

### Product Categories
![Dairy Section](assets/screenshots/dairy-section.png)
![Meat Section](assets/screenshots/meat-section.png)

### Age Restriction (Drinks)
![Underage Restriction](assets/screenshots/drinks-underage.png)

### Weight-Based Product Input
![Weight Input](assets/screenshots/weight-input.png)

### Shopping Cart
![Shopping Cart](assets/screenshots/shopping-cart.png)

### Checkout & Validation
![Checkout Validation](assets/screenshots/checkout-validation.png)

### Payment Success
![Payment Success](assets/screenshots/payment-success.png)

------------------------------------------------------------
CORE CONCEPTS & DESIGN
------------------------------------------------------------

At the core of the system is an abstract Product class:

public class Product {
    public int SerialNum { get; set; }
    public string Name { get; set; }
    public double Price { get; set; }
    public double Amount { get; set; }
}

From Product, four categories inherit:
- Dairy
- Drink
- Meat
- Vegan

Each category adds its own specific attributes.

Concrete product types:
- Dairy: Cheese, IceCream, Milk
- Drink: Alcoholic, SoftDrinks, Wine
- Meat: Beef, Chicken, Lamb
- Vegan: Frozen, Fruits, Vegetables

------------------------------------------------------------
USER INTERFACE (WINFORMS)
------------------------------------------------------------

- Main screen with category buttons
- Category-specific internal views with product shelves and images
- Prices displayed visually on product images
- Shopping cart panel updates in real time
- Optional background music with toggle button

------------------------------------------------------------
SHOPPING CART LOGIC
------------------------------------------------------------

- Products are added by clicking on them
- Weight-based products prompt for numeric input
- Unit-based products use a dropdown selection
- Cart displays selected items and total price
- Cart can be saved and loaded using a phone number

Cart data is persisted using JSON serialization.

------------------------------------------------------------
AGE RESTRICTION LOGIC
------------------------------------------------------------

- On first entry to the Drinks section, the user enters birth date
- Age is calculated using the current date
- Users under 18 cannot view Alcoholic or Wine products
- Age restriction persists even after loading a saved cart

------------------------------------------------------------
CHECKOUT & VALIDATION
------------------------------------------------------------

- Separate checkout screen
- Credit card validation and card type detection
- Phone number / ID validation
- Dynamic UI feedback
- Checkout button enabled only when all fields are valid
- Address field required (prototype behavior)

After checkout:
- Cart is cleared
- Total price reset
- Application returns to main menu

------------------------------------------------------------
PROJECT GOALS
------------------------------------------------------------

- Demonstrate OOP and inheritance
- Apply abstraction in a real-world domain
- Build UI-driven business logic
- Use serialization and persistence
- Create a complete desktop application prototype

------------------------------------------------------------
TECHNOLOGIES
------------------------------------------------------------

- C#
- .NET
- WinForms
- JSON serialization & deserialization
- Object-Oriented Programming


