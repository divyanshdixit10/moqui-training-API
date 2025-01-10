# moqui-training-API

RESTful API for Party, Product, and Order Management
This project implements a RESTful API to manage party data, product data, and order data. Below are the available API endpoints for each task.


1. Create a Party: `POST /parties`
Creates a new party.
Request Body:

{
  "name": "Party Name",
  "description": "Party Description",
  "startDate": "2025-01-01",
  "endDate": "2025-01-02"
}

Response:
Status: `201 Created`
Body: Party details with a unique `party_id`

![Screenshot 2025-01-09 175828](https://github.com/user-attachments/assets/6e54c546-ef3f-456e-a4c6-b0fcd1925d9d)

2. Retrieve Party Details: `GET /parties/{party_id}`
Retrieves details of a specific party using its `party_id`.

Response:
Status: `200 OK`
Body: Party details

![Screenshot 2025-01-09 175910](https://github.com/user-attachments/assets/da3c4e85-9660-4299-ad56-ce0d67f03816)

3. Update a Party: `PUT /parties/{party_id}`
Updates the information of a specific party.
Request Body:

{
  "name": "Updated Party Name",
  "description": "Updated Description",
  "startDate": "2025-01-03",
  "endDate": "2025-01-04"
}

Response:
Status: `200 OK`
Body: Updated party details

![Screenshot 2025-01-09 181821](https://github.com/user-attachments/assets/3633c144-f0ae-4ec5-8245-bcee672e8c73)

4. Delete a Party: `DELETE /parties/{party_id}`
Deletes a specific party by its `party_id`.

Response:
Status: `200 OK`
Body: Success message

![Screenshot 2025-01-09 175944](https://github.com/user-attachments/assets/866b422a-0357-44ca-91c5-88ef3ef5ac02)

Manage Contact Mechanisms for a Party

1. Add Contact Mechanism: `POST /parties/{party_id}/contacts`
Adds a new contact mechanism (e.g., email, phone) for a specific party.
Request Body:

{
  "type": "email",
  "value": "contact@party.com"
}

Response:
Status: `201 Created`
Body: New contact mechanism details

![Screenshot 2025-01-09 181957](https://github.com/user-attachments/assets/fcf82bb2-e45f-462c-8e7d-c7c65984f9c9)

2. Retrieve Contact Mechanisms: `GET /parties/{party_id}/contacts`
Retrieves all contact mechanisms associated with a specific party.

Response:
Status: `200 OK`
Body: List of contact mechanisms

![Screenshot 2025-01-09 181957](https://github.com/user-attachments/assets/7be42a0e-9c65-4345-b274-9f1b6ead58b1)

3. Update Contact Mechanism: `PUT /parties/{party_id}/contacts/{contact_mech_id}`
Updates a specific contact mechanism.
Request Body:

{
  "type": "phone",
  "value": "123-456-7890"
}

Response:
Status: `200 OK`
Body: Updated contact mechanism details

![Screenshot 2025-01-09 182915](https://github.com/user-attachments/assets/3fcf931a-7c73-412a-8a02-984dbff99f48)

4. Delete Contact Mechanism: `DELETE /parties/{party_id}/contacts/{contact_mech_id}`
Deletes a specific contact mechanism for a party.

Response:
Status: `200 OK`
Body: Success message

![Screenshot 2025-01-09 183027](https://github.com/user-attachments/assets/12301830-440d-4956-8072-c57bd54ce117)

Task 3: Develop RESTful APIs for Product Data

1. Create a Product: `POST /products`
Creates a new product.
Request Body:

{
  "name": "Product Name",
  "description": "Product Description",
  "price": 100.0
}

Response:
Status: `201 Created`
Body: Product details with a unique `product_id`

![Screenshot 2025-01-09 183209](https://github.com/user-attachments/assets/62cb5f00-a72f-40a1-8607-ef7ae3b2d0af)

2. Retrieve Product Details: `GET /products/{product_id}`
Retrieves details of a specific product using its `product_id`.

Response:
Status: `200 OK`
Body: Product details

![Screenshot 2025-01-09 183301](https://github.com/user-attachments/assets/b67f5c17-0e2a-4447-aded-c3fcacbccef7)

3. Update a Product: `PUT /products/{product_id}`
Updates a product's information.
Request Body:

{
  "name": "Updated Product Name",
  "description": "Updated Description",
  "price": 150.0
}

Response:
Status: `200 OK`
Body: Updated product details

![Screenshot 2025-01-09 183449](https://github.com/user-attachments/assets/dece6f9a-e9f1-49e2-86e2-5f816d943a2e)

4. Delete a Product: `DELETE /products/{product_id}`
Deletes a specific product.

Response:
Status: `200 OK`
Body: Success message

![Screenshot 2025-01-09 183724](https://github.com/user-attachments/assets/0f20601c-bfc1-4f69-a9e2-1615a4fe1dda)

Task 4: Develop RESTful APIs for Order Data

1. Create an Order: `POST /orders`
Creates a new order.
Request Body:

{
  "customerId": "123",
  "orderDate": "2025-01-01",
  "totalAmount": 250.0
}

Response:
Status: `201 Created`
Body: Order details with a unique `order_id`

![Screenshot 2025-01-09 184103](https://github.com/user-attachments/assets/ce12d9c3-2b4e-4b2e-9854-8e8f12c9313a)

2. Retrieve Order Details: `GET /orders/{order_id}`
Retrieves details of a specific order using its `order_id`.

Response:
Status: `200 OK`
Body: Order details

![Screenshot 2025-01-09 184411](https://github.com/user-attachments/assets/46c28e6a-d9e4-4378-97ff-0db4e6f3deff)

3. Update an Order: `PUT /orders/{order_id}`
Updates the details of a specific order.
Request Body:

{
  "customerId": "123",
  "orderDate": "2025-01-02",
  "totalAmount": 300.0
}

Response:
Status: `200 OK`
Body: Updated order details

![Screenshot 2025-01-09 185602](https://github.com/user-attachments/assets/a11f8764-203b-4a99-b780-f5fb6db75b21)

4. Delete an Order: `DELETE /orders/{order_id}`
Deletes a specific order.

Response:
Status: `200 OK`
Body: Success message

![Screenshot 2025-01-09 185801](https://github.com/user-attachments/assets/20bfe100-01d3-4c41-9078-8d914611d4ab)

6. Add an Order Item: `POST /orders/{order_id}/items`
Adds an item to an order.
Request Body:

{
  "productId": "456",
  "quantity": 2,
  "price": 50.0
}

Response:
Status: `201 Created`
Body: New order item details

![Screenshot 2025-01-09 191235](https://github.com/user-attachments/assets/f2c0f00c-7c33-4bd0-b305-d3dfad632012)

