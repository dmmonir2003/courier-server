# Courier Backend API

## 🚀 Project Overview

This is a comprehensive backend API for a courier delivery service built with Node.js, Express, and TypeScript. The system manages users, authentication, chat functionality, notifications, payments, and more, providing a robust foundation for a modern courier application.

## ✨ Features

- **User Management**: Registration, authentication, and profile management
- **Real-time Chat**: Integrated chat system with socket.io for customer support
- **Payment Integration**: Mollie payment gateway support
- **Notifications**: Push notifications for order updates
- **Analytics**: Track delivery performance and user engagement
- **File Upload**: AWS S3 integration for document and image uploads
- **Rating System**: Customer feedback and rating functionality
- **Time Slots**: Flexible scheduling for deliveries
- **Multi-language Support**: Internationalization ready

## 🛠 Tech Stack

- **Runtime**: Node.js
- **Framework**: Express.js
- **Language**: TypeScript
- **Database**: MongoDB with Mongoose
- **Authentication**: JWT (JSON Web Tokens)
- **Real-time Communication**: Socket.io
- **File Storage**: AWS S3
- **Payment Gateway**: Mollie
- **Validation**: Zod
- **Error Handling**: Custom error handlers
- **Email Service**: Nodemailer
- **Containerization**: Docker

## 📋 Prerequisites

- Node.js (v16 or higher)
- MongoDB
- Docker (optional)
- AWS S3 credentials (for file uploads)
- Mollie API keys (for payments)

## 🚀 Installation & Setup

1. **Clone the repository**

   ```bash
   git clone <repository-url>
   cd courier-backend
   ```

2. **Install dependencies**

   ```bash
   npm install
   ```

3. **Environment Configuration**
   Create a `.env` file in the root directory with the following variables:

   ```env
   NODE_ENV=development
   PORT=5000
   DATABASE_URL=mongodb://localhost:27017/courier
   JWT_SECRET=your-jwt-secret
   AWS_ACCESS_KEY_ID=your-aws-key
   AWS_SECRET_ACCESS_KEY=your-aws-secret
   AWS_REGION=your-region
   S3_BUCKET_NAME=your-bucket
   MOLLIE_API_KEY=your-mollie-key
   EMAIL_USER=your-email
   EMAIL_PASS=your-email-password
   ```

4. **Run the application**

   ```bash
   # Development mode
   npm run dev

   # Production build
   npm run build
   npm start
   ```

5. **Using Docker**
   ```bash
   docker-compose up -d
   ```

## 📚 API Documentation

### Authentication Endpoints

- `POST /api/auth/login` - User login
- `POST /api/auth/register` - User registration
- `POST /api/auth/refresh` - Refresh access token

### User Management

- `GET /api/users` - Get all users
- `GET /api/users/:id` - Get user by ID
- `PUT /api/users/:id` - Update user profile

### Chat System

- `POST /api/chat/rooms` - Create chat room
- `GET /api/chat/rooms/:id/messages` - Get chat messages
- `POST /api/chat/messages` - Send message

### Payments

- `POST /api/payments/create` - Create payment
- `GET /api/payments/:id` - Get payment status

### And more... (See Postman collection for complete API documentation)

## 🔗 Frontend Integration Experience

As a frontend developer, I have thoroughly analyzed and integrated this backend API into my frontend application. Here's my understanding and implementation approach:

### Backend Architecture Understanding

1. **Modular Structure**: The backend is well-organized into modules (Auth, User, Chat, etc.), each containing controllers, services, models, and validations. This separation of concerns makes it easy to understand and integrate specific functionalities.

2. **Authentication Flow**: Implemented JWT-based authentication with refresh tokens. I integrated login/register endpoints and handled token storage securely in the frontend.

3. **Real-time Features**: Utilized Socket.io for chat functionality. Successfully integrated real-time messaging by connecting to the WebSocket endpoints and managing connection states.

4. **Error Handling**: The backend provides structured error responses. I implemented comprehensive error handling in the frontend, mapping backend error codes to user-friendly messages.

5. **Data Validation**: Used Zod schemas for validation. This helped me understand expected data formats and implement proper form validations on the frontend.

### Integration Highlights

- **API Consumption**: Created reusable API service functions using Axios/Fetch, handling authentication headers and response parsing.
- **State Management**: Integrated API responses with frontend state management (Redux/Zustand) for seamless data flow.
- **Real-time Updates**: Implemented WebSocket connections for live chat and notifications.
- **File Uploads**: Integrated AWS S3 uploads for profile pictures and documents.
- **Payment Flow**: Successfully integrated Mollie payment gateway for secure transactions.

### Challenges Overcome

- Understanding complex relationships between entities (Users, Orders, ChatRooms)
- Handling asynchronous operations and loading states
- Implementing proper error boundaries and retry mechanisms
- Optimizing API calls with caching and debouncing

This deep understanding of the backend architecture has enabled me to integrate APIs efficiently and build a robust frontend application that communicates seamlessly with this courier backend.

## 📊 Testing

```bash
# Run unit tests
npm test

# Run load tests (using Artillery)
npm run load-test
```

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📞 Contact

- **Author**: Md Moniruzzaman
- **Email**: [mdmoniruzzamanshuvo2003@gmail.com
  ](mailto:mdmoniruzzamanshuvo2003@gmail.com)
- **LinkedIn**: [Md Moniruzzaman](https://linkedin.com/in/dmmonir2003)
- **GitHub**: [dmmonir2003](https://github.com/dmmonir2003)

For any questions about this project or my development work, please feel free to reach out.

---

### Requirement Analysis

[Link to Requirement Analysis Document](https://docs.google.com/document/d/1ZySm7f8CRCzZqIcZUYnYj2tZ3RW66NbqNz5jg37O7YIwrong/edit?usp=sharing)

Description: This document outlines the detailed analysis of project requirements.

---

A property development project involves planning, designing, and constructing residential, commercial, or industrial properties to create value and meet market demands. It encompasses land acquisition, regulatory approvals, construction, and final sale or leasing of the developed property.

---

### Postman Collection

![POSTMAN COLLECTION](./Project-Management.postman_collection.json)

Description: This is a Postman collection of all the API endpoints. Download this and import it into your Postman if needed.

---
