
# 🛒 E-Commerce Microservices System

This project is a microservices-based e-commerce system using **NestJS**, **Prisma**, **RabbitMQ**, **Cloudinary**, and **PostgreSQL**. It includes the following services:

- **API Gateway**
- **Customer Service**
- **Product Service**
- **Order Service**

---

## 📦 Folder Structure

backend/ ├── api-gateway/ ├── customer-service/ ├── product-service/ └── order-service/

---

## 🛠 Prerequisites

Before running any service, make sure you have the following installed:

- [Node.js](https://nodejs.org/)
- [RabbitMQ](https://www.rabbitmq.com/download.html) (run locally)
- [PostgreSQL](https://www.postgresql.org/download/)
  - Create the following PostgreSQL databases:
    - `customer-service-db`
    - `product-service-db`
    - `order-service-db`

---

## 🚀 Setup Instructions (Per Service)

### ✅ Customer Service

**Description**: Handles user-related operations such as registration, login, and profile management.

**Folder Structure**:

customer-service/ ├── prisma/               # Prisma schema and seed ├── src/ │   ├── common/           # Prisma service │   └── customer/         # DTOs, controller, services

**Setup**:
```bash
cd customer-service
npm install
npx prisma init
npx prisma generate
npx prisma migrate dev --name init
npx prisma db seed
npm run start:dev


---

✅ Product Service

Description: Manages all product operations and file uploads to Cloudinary.

Folder Structure:

product-service/
├── prisma/               # Prisma schema and seed
├── src/
│   ├── cloudinary/       # Cloudinary service
│   ├── common/prisma/    # Prisma service
│   └── product/          # DTOs, controller, services

Setup:

cd product-service
npm install
npx prisma init
npx prisma generate
npx prisma migrate dev --name init
npx prisma db seed
npm run start:dev


---

✅ Order Service

Description: Handles cart operations, order placement, order history, and related actions.

Folder Structure (similar to product service):

order-service/
├── prisma/
├── src/
│   ├── common/prisma/
│   └── order/            # Cart/order-related logic

Setup:

cd order-service
npm install
npx prisma init
npx prisma generate
npx prisma migrate dev --name init
npm run start:dev


---

✅ API Gateway

Description: Acts as the central entry point for all services. Responsible for:

Routing requests to the correct service

Validating JWT tokens

Attaching user info to requests

Communicating with microservices via RabbitMQ


Setup:

cd api-gateway
npm install
npx prisma init
npx prisma generate
npx prisma migrate dev --name init
npm run start:dev


---

🧪  



---

📌  



---

🔐 Environment Variables

Each service should have a .env file with the following:

DATABASE_URL=postgresql://username:password@localhost:5432/your-db-name
RABBITMQ_URL=amqp://localhost
JWT_SECRET=your_jwt_secret


---

📚 License

This project is open-source and free to use for educational or commercial purposes.

---

Let me know if you'd like this in a downloadable `README.md` file or want Swagger setup instructions added as well.

