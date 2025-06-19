# Product API

## How to Run
```bash
npm install
node server.js
```

## API Endpoints

### GET /api/products
- List all products
- Supports: `?category=...`, `?search=...`, `?page=...&limit=...`

### GET /api/products/:id
- Retrieve single product by ID

### POST /api/products
- Create a new product
- Requires fields: `name`, `description`, `price`, `category`, `inStock`

### PUT /api/products/:id
- Update a product by ID

### DELETE /api/products/:id
- Delete a product by ID

### GET /api/products/stats
- Get product count by category

## Auth
Use header: `x-api-key: 12345`

## Example Request
```bash
curl -H "Content-Type: application/json" -H "x-api-key: 12345" \
     -d '{"name":"Mouse","description":"Wireless","price":20,"category":"electronics","inStock":true}' \
     http://localhost:3000/api/products
```