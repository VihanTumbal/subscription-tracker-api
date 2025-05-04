<div align="center">
  <h1>🔄 Subscription Management System API</h1>
  <p>A robust RESTful API for managing user subscriptions, payments, and automated notifications</p>
  <div>
    <img src="https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=nodedotjs&logoColor=white" alt="nodejs" />
    <img src="https://img.shields.io/badge/Express.js-000000?style=for-the-badge&logo=express&logoColor=white" alt="express" />
    <img src="https://img.shields.io/badge/MongoDB-4EA94B?style=for-the-badge&logo=mongodb&logoColor=white" alt="mongodb" />
  </div>
</div>

## 📑 Table of Contents

- [Overview](#overview)
- [Key Features](#features)
- [Tech Stack](#tech-stack)
- [Getting Started](#getting-started)
  - [Prerequisites](#prerequisites)
  - [Installation](#installation)
  - [Configuration](#configuration)
- [API Documentation](#api-documentation)
- [Project Structure](#structure)
- [Contributing](#contributing)

## 🌟 Overview <a name="overview"></a>

This API provides a complete subscription management solution with user authentication, payment processing, and automated email notifications. Built with scalability and security in mind, it offers a robust foundation for subscription-based services.

## 🎯 Key Features <a name="features"></a>

- **User Management**

  - JWT-based authentication
  - Role-based access control
  - User profile management

- **Subscription Handling**

  - Multiple subscription plans
  - Payment processing
  - Subscription status tracking
  - Automated renewal processing

- **Security**

  - Request rate limiting
  - Input validation
  - Error handling middleware
  - Secure password hashing

- **Notifications**
  - Automated email reminders
  - Payment confirmation
  - Subscription status updates
  - Custom email templates

## 🛠️ Tech Stack <a name="tech-stack"></a>

- **Runtime Environment:** Node.js
- **Framework:** Express.js
- **Database:** MongoDB with Mongoose ODM
- **Authentication:** JSON Web Tokens (JWT)
- **Email Service:** Nodemailer
- **Task Scheduling:** Upstash Workflows
- **Development Tools:** ESLint, Nodemon

## 🚀 Getting Started <a name="getting-started"></a>

### Prerequisites <a name="prerequisites"></a>

- Node.js (v18 or higher)
- MongoDB
- npm or yarn
- Git

### Installation <a name="installation"></a>

1. Clone the repository

```bash
git clone https://github.com/VihanTumbal/subscription-tracker-api.git
cd subscription-tracker-api
```

2. Install dependencies

```bash
npm install
```

### Configuration <a name="configuration"></a>

1. Create `.env.development.local` for development environment:

```env
# Server Configuration
PORT=3000
NODE_ENV=development
SERVER_URL="http://localhost:3000"

# Database
DB_URI="your_mongodb_connection_string"

# Authentication
JWT_SECRET="your_jwt_secret"
JWT_EXPIRES_IN="1d"

# Email Configuration
EMAIL_PASSWORD="your_email_app_password"

# Upstash Configuration
QSTASH_URL="your_qstash_url"
QSTASH_TOKEN="your_qstash_token"
```

2. Start the development server

```bash
npm run dev
```

## 📚 API Documentation <a name="api-documentation"></a>

### Authentication Endpoints

- `POST /api/v1/auth/register` - Register a new user
- `POST /api/v1/auth/login` - User login
- `POST /api/v1/auth/logout` - User logout

### User Endpoints

- `GET /api/v1/users/profile` - Get user profile
- `PUT /api/v1/users/profile` - Update user profile

### Subscription Endpoints

- `GET /api/v1/subscriptions` - List all subscriptions
- `POST /api/v1/subscriptions` - Create new subscription
- `PUT /api/v1/subscriptions/:id` - Update subscription
- `DELETE /api/v1/subscriptions/:id` - Cancel subscription

## 📁 Project Structure <a name="structure"></a>

```
subscription-tracker-api/
├── config/           # Configuration files
├── controllers/      # Request handlers
├── models/          # Database models
├── routes/          # API routes
├── middlewares/     # Custom middlewares
├── utils/           # Utility functions
├── services/        # Business logic
└── tests/           # Test files
```

## 🤝 Contributing <a name="contributing"></a>

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the project
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request
