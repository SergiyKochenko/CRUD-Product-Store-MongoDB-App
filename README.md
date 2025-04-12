# My React Projects - Backend and Frontend
- This project includes both the backend and frontend components for the "My React Projects" application. The backend is built using Node.js, Express, and MongoDB, while the frontend is built with React using Vite and styled with Chakra UI.

This is the backend for the "My React Projects" application. It is built using Node.js, Express, and MongoDB.

## Table of Contents

- [My React Projects - Backend and Frontend](#my-react-projects---backend-and-frontend)
  - [Table of Contents](#table-of-contents)
  - [Project Overview](#project-overview)
  - [Features](#features)
  - [Technologies Used](#technologies-used)
  - [Project Setup](#project-setup)
    - [1. Initialize the Project](#1-initialize-the-project)
    - [2. Install Dependencies](#2-install-dependencies)
    - [3. Configure Environment Variables](#3-configure-environment-variables)
    - [4. Added a `.gitignore` File](#4-added-a-gitignore-file)
    - [5. Start the Server](#5-start-the-server)
  - [Frontend Setup](#frontend-setup)
    - [1. Initialize the Frontend](#1-initialize-the-frontend)
    - [2. Install Chakra UI](#2-install-chakra-ui)
    - [3. Install Additional Dependencies](#3-install-additional-dependencies)
      - [React Router DOM](#react-router-dom)
      - [React Icons](#react-icons)
      - [Chakra UI Icons](#chakra-ui-icons)
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

### 4. Added a `.gitignore` File

Create a `.gitignore` file in the root directory to exclude unnecessary files and directories from version control. The file should include:

```
node_modules/
.env
logs/
*.log
.vscode/
.idea/
.DS_Store
Thumbs.db
```

### 5. Start the Server

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

## Frontend Setup

### 1. Initialize the Frontend

Navigate to the `frontend` directory and create a new React project using Vite:

```bash
cd ./frontend/
npm create vite@latest .
```

Follow the prompts:

- **Select a framework**: React
- **Select a variant**: JavaScript

Once the scaffolding is complete, install the dependencies:

```bash
npm install
```

Start the development server:

```bash
npm run dev
```

### 2. Install Chakra UI

Install Chakra UI and its dependencies:

```bash
npm i @chakra-ui/react@2 @emotion/react @emotion/styled framer-motion
```

Wrap your application with the `ChakraProvider` in `main.jsx`:

```jsx
// filepath: c:\Users\Sergiy\Desktop\My-React-Projects\frontend\src\main.jsx
import React from 'react';
import { createRoot } from 'react-dom/client';
import App from './App.jsx';
import { ChakraProvider } from '@chakra-ui/react';

createRoot(document.getElementById('root')).render(
  <React.StrictMode>
    <ChakraProvider>
      <App />
    </ChakraProvider>
  </React.StrictMode>,
);
```

### 3. Install Additional Dependencies

#### React Router DOM

Install `react-router-dom` for routing:

```bash
npm i react-router-dom
```

Documentation: [React Router DOM](https://reactrouter.com/)

#### React Icons

Install `react-icons` for using popular icons:

```bash
npm i react-icons
```

Documentation: [React Icons](https://react-icons.github.io/react-icons/)

#### Chakra UI Icons

Install `@chakra-ui/icons` for Chakra-specific icons:

```bash
npm i @chakra-ui/icons
```

Documentation: [Chakra UI Icons](https://v2.chakra-ui.com/docs/components/icon/usage)

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

