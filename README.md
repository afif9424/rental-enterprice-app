# Rental Enterprise App 🏢🏡

Welcome to the **Rental Enterprise App** repository! This project is a scalable, enterprise-grade full-stack real estate rental application built with modern technologies and AWS services. Whether you're a developer, investor, or simply curious about real estate tech, this app offers a robust solution for managing rental properties.

[![Releases](https://img.shields.io/badge/Releases-v1.0-blue)](https://github.com/afif9424/rental-enterprice-app/releases)

## Table of Contents

- [Introduction](#introduction)
- [Features](#features)
- [Technologies Used](#technologies-used)
- [Getting Started](#getting-started)
- [Usage](#usage)
- [Contributing](#contributing)
- [License](#license)
- [Contact](#contact)

## Introduction

The **Rental Enterprise App** is designed to provide a seamless experience for both property owners and tenants. With a user-friendly interface and powerful backend services, this application simplifies the rental process. You can manage listings, track payments, and communicate with tenants—all in one place.

To explore the latest updates and releases, visit the [Releases section](https://github.com/afif9424/rental-enterprice-app/releases).

## Features

- **User Authentication**: Secure login and registration using AWS Cognito.
- **Property Management**: Easily add, edit, or remove property listings.
- **Payment Tracking**: Integrate AWS Billing to manage rental payments.
- **Real-time Maps**: Utilize Mapbox for interactive property maps.
- **Data Management**: Use PostgreSQL with Prisma ORM for efficient data handling.
- **Responsive Design**: Built with Tailwind CSS for a mobile-friendly experience.
- **State Management**: Implement Redux Toolkit for seamless state management.
- **Serverless Functions**: Leverage AWS Lambda for backend logic.

## Technologies Used

This project utilizes a range of modern technologies to ensure scalability and performance:

- **AWS Amplify**: For building and deploying cloud-powered applications.
- **AWS Cognito**: For user authentication and management.
- **AWS Lambda**: To run backend code without provisioning servers.
- **EC2 Instance**: For hosting the application.
- **Mapbox**: For mapping features.
- **Next.js**: A React framework for server-side rendering.
- **PostgreSQL Database**: A powerful relational database for storing data.
- **Prisma ORM**: For database interactions.
- **Redux Toolkit**: For managing application state.
- **S3 Bucket**: For storing files and assets.
- **Shadcn UI**: For pre-built UI components.

## Getting Started

To get started with the **Rental Enterprise App**, follow these steps:

### Prerequisites

Ensure you have the following installed:

- Node.js (v14 or higher)
- npm (v6 or higher)
- PostgreSQL (v12 or higher)
- AWS CLI

### Clone the Repository

First, clone the repository to your local machine:

```bash
git clone https://github.com/afif9424/rental-enterprice-app.git
cd rental-enterprice-app
```

### Install Dependencies

Install the necessary dependencies using npm:

```bash
npm install
```

### Set Up Environment Variables

Create a `.env` file in the root directory and add the required environment variables:

```
DATABASE_URL=your_database_url
AWS_ACCESS_KEY_ID=your_aws_access_key
AWS_SECRET_ACCESS_KEY=your_aws_secret_key
```

### Start the Application

Run the application locally:

```bash
npm run dev
```

You can now access the application at `http://localhost:3000`.

## Usage

Once the application is running, you can register as a new user or log in if you already have an account. Explore the features, add properties, and manage your rentals efficiently.

### User Roles

- **Admin**: Full access to manage properties, users, and payments.
- **Owner**: Can manage their own properties and view payment history.
- **Tenant**: Can view properties, make payments, and communicate with owners.

### Managing Properties

1. Log in as an Admin or Owner.
2. Navigate to the "Properties" section.
3. Click "Add Property" to create a new listing.
4. Fill in the details and save.

### Tracking Payments

- Access the "Payments" section to view all transactions.
- Filter by date or property to find specific records.

## Contributing

We welcome contributions! If you'd like to contribute, please follow these steps:

1. Fork the repository.
2. Create a new branch (`git checkout -b feature/YourFeature`).
3. Make your changes and commit them (`git commit -m 'Add some feature'`).
4. Push to the branch (`git push origin feature/YourFeature`).
5. Open a pull request.

Please ensure your code adheres to our coding standards and includes tests where applicable.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Contact

For questions or suggestions, feel free to reach out:

- **Email**: your.email@example.com
- **GitHub**: [afif9424](https://github.com/afif9424)

Thank you for your interest in the **Rental Enterprise App**! For the latest updates, visit the [Releases section](https://github.com/afif9424/rental-enterprice-app/releases).