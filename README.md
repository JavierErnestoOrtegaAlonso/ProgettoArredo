# Furniture Store Management API

This project is a **Spring Boot** application designed for managing an online furniture store. It provides features for adding, updating, and deleting furniture items, handling user interactions such as browsing the inventory, managing a shopping cart, and processing payments using **Stripe**.

## Features
- Manage furniture inventory (add, update, delete items).
- Browse the store and shopping cart.
- Send order confirmation emails with images using an email service.
- Process payments using Stripe integration.

## Technologies Used
- **Spring Boot** for the backend.
- **Stripe API** for payment processing.
- **Jakarta Mail** for email notifications.
- **Thymeleaf** for server-side rendering of HTML views.
- **Java JDBC** for database interaction.

## Setup Instructions

### Prerequisites
1. Java 17 or higher installed.
2. Maven installed.
3. A configured database (compatible with JDBC).
4. A Stripe account with API keys.
5. SMTP credentials for sending emails.

### Installation
1. Clone the repository:
   ```bash
   git clone https://github.com/JavierErnestoOrtegaAlonso/ProgettoArredo.git



  API Endpoints
  Public Endpoints
  
GET	/	Displays the home page.
GET	/store	Displays the store inventory.
GET	/carrello	Displays the shopping cart.
GET	/lista	Returns the list of furniture items (JSON).



Private Endpoints (Manager)
HTTP Method	Endpoint	Description

GET	/private/form	Displays the form for adding items.
POST	/submit	Adds a new furniture item.
POST	/update	Updates the price of an item.
POST	/delete	Deletes a furniture item.
GET	/private/inventory	Displays the full inventory.


Shopping Cart Management
HTTP Method	Endpoint	Description
POST	/add	Adds an item to the cart.
POST	/del	Removes an item from the cart.
POST	/clear	Clears the shopping cart.

HTTP Method	Endpoint	Description
POST	/buy	Processes the payment and sends an order confirmation email.


Stripe Integration
The Stripe API is used to handle payments securely. The payment flow involves:

Generating a payment token on the frontend.
Sending the token and user details to the /buy endpoint.
Processing the payment on the server and sending a receipt to the user.
Email Service
The application uses Jakarta Mail for sending order confirmation emails. The emails include:

A summary of purchased items.
Images of the purchased furniture.
Project Structure
Controller: Handles HTTP requests and business logic.
Model: Contains classes like arredo and arredo2 for managing furniture data.
Service: Manages database interactions and email functionality.
Views: Thymeleaf templates for rendering HTML pages.
Future Improvements
Add authentication and authorization for secure access to private endpoints.
Implement frontend validation for forms.
Enhance cart functionality to persist user sessions.
