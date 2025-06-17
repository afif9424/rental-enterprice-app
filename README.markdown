# Real Estate Rental Application

A scalable, enterprise-grade full-stack real estate rental application built with modern technologies and AWS services. This project leverages **Next.js** for the frontend, **Node.js** with **Express.js** for the backend, and a suite of AWS services for robust cloud infrastructure. The application supports apartment search, user authentication, and geospatial data visualization with a modern, responsive UI.

---

## Table of Contents

- [Features](#features)
- [Tech Stack](#tech-stack)
- [Architecture](#architecture)
- [Prerequisites](#prerequisites)
- [Getting Started](#getting-started)
  - [Frontend Setup](#frontend-setup)
  - [Backend Setup](#backend-setup)
  - [AWS Configuration](#aws-configuration)
- [Environment Variables](#environment-variables)
- [Running the Application](#running-the-application)
- [Deployment](#deployment)
- [Testing](#testing)
- [Contributing](#contributing)
- [Resources](#resources)
- [License](#license)

---

## Features

- **Apartment Search**: Search for rental apartments with geospatial visualization using Mapbox.
- **User Authentication**: Secure user authentication and authorization with AWS Cognito.
- **Responsive UI**: Modern, animated UI built with Tailwind CSS, Shadcn, and Framer Motion.
- **Form Validation**: Robust form handling with React Hook Form and Zod.
- **State Management**: Efficient state management with Redux Toolkit and RTK Query.
- **Scalable Backend**: RESTful API built with Node.js, Express.js, and Prisma, hosted on AWS EC2.
- **Database**: PostgreSQL with PostGIS for geospatial data, managed on AWS RDS.
- **File Storage**: Store images and assets in AWS S3.
- **API Gateway**: Secure and scalable API management with AWS API Gateway.
- **CI/CD**: Streamlined deployment with AWS Amplify.

---

## Tech Stack

### Frontend
- **Next.js**: React framework for server-side rendering and static site generation.
- **Redux Toolkit**: State management with RTK Query for data fetching.
- **Tailwind CSS**: Utility-first CSS framework for rapid UI development.
- **Shadcn**: Reusable UI components for a polished look.
- **TypeScript**: Static typing for enhanced developer experience.
- **Framer Motion**: Smooth animations for a dynamic UI.
- **React Hook Form**: Performant form handling.
- **Zod**: Schema validation for forms and API payloads.
- **Mapbox & Mapbox React GL**: Interactive maps for geospatial visualization.

### Backend
- **Node.js & Express.js**: Lightweight, scalable backend framework.
- **Prisma**: Modern ORM for database interactions.
- **PostgreSQL with PostGIS**: Relational database with geospatial capabilities.
- **AWS Services**:
  - **EC2**: Hosting the backend application.
  - **RDS**: Managed PostgreSQL database.
  - **S3**: File storage for images and assets.
  - **API Gateway**: Secure API endpoints.
  - **Amplify**: CI/CD and hosting for the frontend.
  - **Cognito**: User authentication and authorization.

### Tools
- **Postman**: API testing and development.
- **PgAdmin**: PostgreSQL database management.
- **AWS CLI**: Command-line interface for AWS services.
- **Nominatim**: Open-source geocoding service.

---

## Architecture

The application follows a modern full-stack architecture:
- **Frontend**: Next.js app hosted on AWS Amplify, integrated with Mapbox for geospatial visualization and Redux Toolkit for state management.
- **Backend**: Node.js/Express.js API hosted on AWS EC2, connected to a PostgreSQL database on AWS RDS with PostGIS for geospatial queries.
- **Authentication**: AWS Cognito for user management and secure authentication.
- **Storage**: AWS S3 for storing apartment images and other assets.
- **API**: AWS API Gateway for secure, scalable API endpoints.
- **Geocoding**: Nominatim for address-to-coordinates conversion.

For detailed diagrams, refer to: [Architecture Diagrams](https://www.edroh.com/subscribe/real-...).

---

## Prerequisites

Before setting up the project, ensure you have the following installed:
- **Node.js** (v18 or higher)
- **npm** or **yarn**
- **PostgreSQL** with **PostGIS** extension
- **PgAdmin** (optional, for database management)
- **Postman** (for API testing)
- **AWS CLI** (configured with your AWS credentials)
- **Git**

You also need:
- An AWS account with access to EC2, RDS, S3, API Gateway, Amplify, and Cognito.
- A Mapbox account and API key for geospatial features.

---

## Getting Started

### Frontend Setup
1. Clone the repository:
   ```bash
   git clone https://github.com/ed-roh/real-estate.git
   cd real-estate/frontend
   ```
2. Install dependencies:
   ```bash
   npm install
   ```
3. Set up environment variables (see [Environment Variables](#environment-variables)).
4. Run the development server:
   ```bash
   npm run dev
   ```

### Backend Setup
1. Navigate to the backend directory:
   ```bash
   cd real-estate/backend
   ```
2. Install dependencies:
   ```bash
   npm install
   ```
3. Set up PostgreSQL with PostGIS:
   - Install PostgreSQL: [Download](https://www.postgresql.org/download/)
   - Install PostGIS: [Instructions](https://postgis.net/workshops/postgis...)
   - Set up a database and enable the PostGIS extension.
4. Configure Prisma:
   ```bash
   npx prisma migrate dev
   ```
5. Set up environment variables (see [Environment Variables](#environment-variables)).
6. Run the backend server:
   ```bash
   npm run start
   ```

### AWS Configuration
1. **EC2**: Set up an EC2 instance for the backend. Follow [AWS EC2 Instructions](https://github.com/ed-roh/real-estate...).
2. **RDS**: Configure a PostgreSQL database on AWS RDS with PostGIS enabled.
3. **S3**: Create an S3 bucket for storing assets.
4. **API Gateway**: Set up API endpoints for the backend.
5. **Cognito**: Configure user pools for authentication. Refer to [AWS Cognito Docs](https://aws.amazon.com/cognito/).
6. **Amplify**: Deploy the frontend using AWS Amplify.
7. Install and configure the AWS CLI: [AWS CLI Docs](https://docs.aws.amazon.com/cli/latest...).

---

## Environment Variables

Create a `.env` file in both the `frontend` and `backend` directories with the following variables:

### Frontend (.env)
```env
NEXT_PUBLIC_MAPBOX_TOKEN=your_mapbox_token
NEXT_PUBLIC_API_URL=http://your-backend-url
NEXT_PUBLIC_AWS_COGNITO_CLIENT_ID=your_cognito_client_id
NEXT_PUBLIC_AWS_COGNITO_REGION=your_aws_region
```

### Backend (.env)
```env
DATABASE_URL=postgresql://user:password@your-rds-endpoint:5432/dbname?schema=public
AWS_ACCESS_KEY_ID=your_aws_access_key
AWS_SECRET_ACCESS_KEY=your_aws_secret_key
AWS_REGION=your_aws_region
AWS_S3_BUCKET=your_s3_bucket_name
AWS_COGNITO_USER_POOL_ID=your_cognito_user_pool_id
```

---

## Running the Application

1. Start the backend server:
   ```bash
   cd backend
   npm run start
   ```
2. Start the frontend development server:
   ```bash
   cd frontend
   npm run dev
   ```
3. Access the application at `http://localhost:3000` (or your deployed URL).

---

## Deployment

- **Frontend**: Deploy to AWS Amplify for automatic scaling and CI/CD.
- **Backend**: Deploy to AWS EC2 with a load balancer for scalability.
- **Database**: Use AWS RDS for managed PostgreSQL with automated backups.
- **Assets**: Store in AWS S3 with public read access for images.

For detailed deployment steps, refer to the [AWS EC2 Instructions](https://github.com/ed-roh/real-estate...).

---

## Testing

- **Frontend**: Use Jest and React Testing Library for unit and integration tests.
- **Backend**: Test API endpoints using Postman: [Download Postman](https://www.postman.com/downloads/).
- **Database**: Verify geospatial queries with PgAdmin: [Download PgAdmin](https://www.pgadmin.org/download/).

---

## Contributing

Contributions are welcome! Please follow these steps:
1. Fork the repository.
2. Create a feature branch (`git checkout -b feature/your-feature`).
3. Commit your changes (`git commit -m 'Add your feature'`).
4. Push to the branch (`git push origin feature/your-feature`).
5. Open a pull request.

---

## Resources

- **Code**: [GitHub Repository](https://github.com/ed-roh/real-estate)
- **Diagrams**: [Architecture Diagrams](https://www.edroh.com/subscribe/real-...)
- **Assets**: [Google Drive](https://drive.google.com/drive/folder...)
- **Frontend**:
  - [Mapbox](https://www.mapbox.com/)
  - [Mapbox React GL](https://docs.mapbox.com/help/tutorial...)
  - [Shadcn](https://ui.shadcn.com/docs)
  - [Shadcn Sonner](https://ui.shadcn.com/docs/components...)
  - [Shadcn React Hook Form](https://ui.shadcn.com/docs/components...)
  - [React Hook Form](https://react-hook-form.com/get-started...)
  - [Zod](https://zod.dev/?id=table-of-contents)
  - [Redux Toolkit](https://redux-toolkit.js.org/)
  - [Redux Toolkit Query](https://redux-toolkit.js.org/rtk-query...)
- **Backend**:
  - [PostgreSQL](https://www.postgresql.org/download/)
  - [PostGIS](https://postgis.net/workshops/postgis...)
  - [PgAdmin](https://www.pgadmin.org/download/)
  - [Prisma](https://www.prisma.io/docs/getting-started)
  - [Postman](https://www.postman.com/downloads/)
  - [AWS](https://aws.amazon.com/)
  - [AWS CLI](https://docs.aws.amazon.com/cli/latest...)
  - [AWS Cognito](https://aws.amazon.com/cognito/)
  - [AWS Amplify Auth](https://ui.docs.amplify.aws/react/connected-components/authenticator)
  - [Nominatim](https://nominatim.org/release-docs/latest/)

---

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.