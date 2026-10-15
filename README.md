# ProductHub – Product Management REST API

A RESTful API built using Node.js, Express.js, MongoDB and Mongoose to manage product inventory through CRUD operations.

## Features

- Create new products
- Retrieve all products or a single product
- Update products using PUT and PATCH
- Delete products
- Mongoose schema validation
- Centralized error handling
- Basic request logging
- Environment variable configuration
- Postman API collection

## Tech Stack

- Node.js
- Express.js
- MongoDB
- Mongoose
- dotenv
- Postman

## Project Structure

```text
ProductHub-REST-API/
├── config/db.js
├── controllers/productController.js
├── middleware/errorMiddleware.js
├── models/Product.js
├── routes/productRoutes.js
├── postman/ProductHub.postman_collection.json
├── .env.example
├── .gitignore
├── package.json
├── package-lock.json
├── README.md
└── server.js
```

## Installation

1. Clone this repository.
2. Open the project folder.
3. Install dependencies:

```bash
npm install
```

4. Create a `.env` file using `.env.example` as a template.
5. Add your MongoDB connection string to `MONGO_URI`.
6. Start the development server:

```bash
npm run dev
```

The server runs at `http://localhost:5000` by default.

## Environment Variables

```env
PORT=5000
MONGO_URI=your_mongodb_connection_string
NODE_ENV=development
```

Never commit your actual `.env` file or database credentials.

## API Endpoints

| Method | Endpoint | Description |
|---|---|---|
| GET | `/` | API health check |
| GET | `/api/products` | Get all products |
| GET | `/api/products/:id` | Get one product |
| POST | `/api/products` | Create a product |
| PUT | `/api/products/:id` | Replace/update a product |
| PATCH | `/api/products/:id` | Partially update a product |
| DELETE | `/api/products/:id` | Delete a product |

## Sample Product

```json
{
  "name": "Wireless Mouse",
  "description": "Ergonomic wireless mouse",
  "price": 799,
  "category": "Electronics",
  "stock": 25
}
```

## Testing

Import `postman/ProductHub.postman_collection.json` into Postman and test each endpoint. Create a product first and use its returned MongoDB `_id` for single-product, update and delete requests.

## Error Handling

The API handles schema validation errors, invalid MongoDB ObjectIds, missing resources, unknown routes and unexpected server errors.

## Future Improvements

- Pagination and product search
- Authentication and authorization
- Automated unit and integration tests
- API deployment and monitoring

## Author

Add your name and GitHub profile here before submission.
