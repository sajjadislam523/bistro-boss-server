# Bistro Boss Server

This is the backend server for the Bistro Boss restaurant application. It manages APIs, database interactions, and payment integrations.

---

## Features

-   **Express.js** for building the server and managing routes.
-   **MongoDB** for database management.
-   **JWT (JSON Web Token)** for secure user authentication.
-   **Stripe** for payment processing.
-   **CORS** for handling cross-origin requests.
-   **dotenv** for managing environment variables.

---

## Installation

### Prerequisites

Ensure you have the following installed on your system:

-   **Node.js** (version 18 or higher)
-   **npm** (comes with Node.js)
-   A database instance (e.g., MongoDB)

### Steps to Install and Run the Server

1. Clone the repository:

    ```bash
    git clone <repository-url>
    ```

2. Navigate to the project directory:

    ```bash
    cd server
    ```

3. Install dependencies:

    ```bash
    npm install
    ```

4. Set up environment variables:

    - Create a `.env` file in the root directory of the project.
    - Add the following environment variables:
        ```env
        PORT=<your-server-port>
        MONGO_URI=<your-mongodb-connection-string>
        JWT_SECRET=<your-jwt-secret-key>
        STRIPE_SECRET_KEY=<your-stripe-secret-key>
        ```

5. Start the server:

    ```bash
    npm start
    ```

6. The server will typically run at:
    ```
    http://localhost:<your-server-port>
    ```

---

## Scripts

-   **Start the Server**:

    ```bash
    npm start
    ```

-   **Run Tests**:
    (Currently not configured)
    ```bash
    npm test
    ```

---

## Dependencies

| Package          | Version | Description                                                                 |
| ---------------- | ------- | --------------------------------------------------------------------------- |
| **cors**         | ^2.8.5  | Middleware to enable Cross-Origin Resource Sharing in APIs.                 |
| **dotenv**       | ^16.4.7 | Loads environment variables from a `.env` file into `process.env`.          |
| **express**      | ^4.21.2 | Fast, unopinionated, minimalist web framework for Node.js.                  |
| **jsonwebtoken** | ^9.0.2  | For creating and verifying JSON Web Tokens (JWT) for secure authentication. |
| **mongodb**      | ^6.12.0 | Official MongoDB driver for Node.js.                                        |
| **stripe**       | ^17.5.0 | Stripe API library for handling payment processing.                         |

---

## API Endpoints

-   **Authentication**

    -   `POST /login` - User login with JWT token generation.
    -   `POST /register` - User registration.

-   **Menu Management**

    -   `GET /menu` - Fetch all menu items.
    -   `POST /menu` - Add a new menu item (admin only).

-   **Order Management**

    -   `GET /orders` - Fetch user orders.
    -   `POST /orders` - Place a new order.

-   **Payments**
    -   `POST /create-payment-intent` - Create a Stripe payment intent.
