# My React Projects - Backend

This is the backend for the "My React Projects" application. It is built using Node.js, Express, and MongoDB.

## Table of Contents

- [My React Projects - Backend](#my-react-projects---backend)
  - [Table of Contents](#table-of-contents)
  - [Project Overview](#project-overview)
  - [Features](#features)
  - [Technologies Used](#technologies-used)
  - [Project Setup](#project-setup)
    - [1. Initialize the Project](#1-initialize-the-project)
    - [2. Install Dependencies](#2-install-dependencies)
    - [3. Configure Environment Variables](#3-configure-environment-variables)
    - [4. Start the Server](#4-start-the-server)
  - [API Endpoints](#api-endpoints)
    - [Products](#products)
  - [Testing](#testing)
    - [Postman](#postman)
  - [Deployment](#deployment)
  - [Credits](#credits)

---

## Project Overview

The backend provides a RESTful API for managing products. It supports CRUD operations and integrates with MongoDB for data storage.

---

## Features

- **CRUD Operations**: Create, Read, Update, and Delete products.
- **RESTful API**: Provides endpoints for managing products.
- **MongoDB Integration**: Uses Mongoose for database operations.
- **Error Handling**: Includes robust error handling for invalid requests.

---

## Technologies Used

- **Node.js**: Backend runtime.
- **Express**: Web framework.
- **MongoDB**: NoSQL database.
- **Mongoose**: MongoDB object modeling.
- **Postman**: API testing tool.

---

## Project Setup

### 1. Initialize the Project

Run the following command to initialize the project:

```bash
npm init -y
```

### 2. Install Dependencies

Install the required dependencies:

```bash
npm install express mongoose dotenv
```

Install `nodemon` as a development dependency:

```bash
npm i nodemon -D
```

### 3. Configure Environment Variables

Create a `.env` file in the `backend` directory and add the following:

```
MONGO_URI=<your-mongodb-connection-string>
```

### 4. Start the Server

Add the following script to your `package.json` file:

```json
"scripts": {
    "dev": "nodemon backend/server.js"
}
```

Then, start the server:

```bash
npm run dev
```

The server will start at `http://localhost:5000`.

---

## API Endpoints

### Products

- **GET** `/api/products` - Get all products.
- **POST** `/api/products` - Create a new product.
- **PUT** `/api/products/:id` - Update a product by ID.
- **DELETE** `/api/products/:id` - Delete a product by ID.

---

## Testing

### Postman

The API was tested using Postman. Below are the steps to test the API:

1. **GET** `/api/products`: Fetch all products.
2. **POST** `/api/products`: Create a new product by sending a JSON payload:
   ```json
   {
       "name": "Sample Product",
       "price": 100,
       "image": "sample-image-url"
   }
   ```
3. **PUT** `/api/products/:id`: Update an existing product by ID.
4. **DELETE** `/api/products/:id`: Delete a product by ID.

---

## Deployment

This project is currently set up for local development. Deployment instructions can be added later if required.

---

## Credits

- **Code Institute**: For providing the README template.
- **MongoDB Documentation**: For database setup and integration.
- **Postman**: For API testing.
