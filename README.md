# FusionFits E-commerce Application

![MIT License](https://img.shields.io/badge/License-MIT-blue.svg)

It is a modern e-commerce platform built with Flask and SQLAlchemy, designed for a seamless shopping experience in the furniture industry. Customers can browse furniture, add items to their cart or wishlist, and place orders, while admins can manage products and orders efficiently.
## Features

### User Features:

- **Registration and Login:** Users can register accounts and securely log in.
- **Product Browsing:** View product details, including images, descriptions, and pricing.
- **Wishlist:** Add products to a wishlist for later purchase.
- **Shopping Cart:** Add products to a shopping cart, update quantities, and remove items.
- **Checkout:** Proceed to checkout, providing shipping information.
- **Order Placement:** Place orders securely.
- **Order History:** View past orders.
- **Password Management:** Reset forgotten passwords.
- **Profile Management:** Update user profile information.

### Admin Features:

- **Admin Dashboard:** Overview of application statistics.
- **Product Management:** Add, update, delete, and view products with image uploads.
- **User Management:** View and manage user details, including roles.
- **Order Management:** View orders placed by users.
- **Role Approval:** Approve or reject role requests (delivery person).

### Delivery Person Features:

- **Dashboard:** Shows orders assigned to them based on city/location.
- **Order Status Updates:** Update order status (e.g., "Shipped", "Delivered").

## Technologies Used

- **Python:** Backend programming language.
- **Flask:** Web framework.
- **Flask-SQLAlchemy:** Object-Relational Mapper (ORM) for database interaction.
- **Flask-Login:** User authentication and session management.
- **Flask-Bcrypt:** Password hashing for security.
- **Flask-Migrate:** Database migration management.
- **Flask-Mail:** Sending email notifications.
- **WTForms:** Handling HTML forms.
- **SQLAlchemy:** ORM for database operations.
- **SQLite:** Database (for development). Consider PostgreSQL or MySQL for production.
- **dotenv:** For managing environment variables.
- **pytest:** Testing framework.

## Setup

1. **Create a virtual environment:**
   ```bash
   python3 -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

2. **Install dependencies:**
   ```bash
   pip install -r requirements.txt
   ```

3. **Set environment variables:** Create a `.env` file in the project root directory and populate it with your email settings and secret key. Example:
   ```ini
   MAIL_SERVER=smtp.gmail.com
   MAIL_PORT=587
   MAIL_USE_TLS=True
   MAIL_USE_SSL=False
   MAIL_USERNAME=your_email@gmail.com
   MAIL_PASSWORD=your_app_password
   SECRET_KEY=a_very_secret_key
   ```

4. **Create the database:**
   ```bash
   flask db upgrade
   ```

5. **Run the application:**
   ```bash
   flask run
   ```

## Testing

This application uses pytest for comprehensive testing.  The tests are located in the `tests/` directory and cover:

- **Unit Tests:** Individual components (functions, models) are tested in isolation.
- **Integration Tests:** Interactions between different components are tested.  For example,  tests verify the interaction between the views and the database.
- **Functional Tests:** End-to-end testing of user flows (e.g., registration, adding to cart, checkout). These tests simulate actual user actions.


To run the tests, navigate to the project's root directory and execute the following command:

```bash
pytest tests/ 
```


## Directory Structure

```
FusionFits/
├── app/                  # Application code
│   ├── __init__.py       # Application initialization
│   ├── views.py          # Main application routes
│   ├── auth.py           # Authentication routes
│   ├── models.py         # Database models
│   ├── forms.py          # WTForms
│   ├── admin.py          # Admin routes
│   ├── password.py       # Password reset routes
│   ├── rating.py         # Rating routes
│   ├── delivery_person.py # Delivery person routes
│   ├── templates/        # HTML templates
│   │   └── ...
│   ├── static/           # Static files (CSS, JS, images)
│   │   └── uploads/      # Folder to store uploaded product images
├── migrations/           # Database migration files
├── tests/                # Test files using pytest
├── requirements.txt      # Project dependencies
├── .env                  # Environment variables
```

## Contributing

Contributions are welcome! Please open an issue or submit a pull request.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
