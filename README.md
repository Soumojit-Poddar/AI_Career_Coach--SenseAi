# AI Career Coach

## Project Overview
AI Career Coach is a web application designed to provide personalized career insights and recommendations using AI. Users can complete their profile by selecting their industry, specialization, and providing professional details. The app offers tailored career advice based on the user's profile.

## Features
- User authentication and onboarding
- Industry and specialization selection
- Profile completion with experience, skills, and bio
- Personalized AI-generated career insights
- Dashboard with industry insights and recommendations

## Setup Instructions

### Prerequisites
- Node.js (v16 or higher recommended)
- npm or yarn package manager
- A Clerk account for authentication (https://clerk.com/)
- A database supported by Prisma (e.g., PostgreSQL)

### Installation
1. Clone the repository:
   ```bash
   git clone <repository-url>
   cd ai-career-coach
   ```

2. Install dependencies:
   ```bash
   npm install
   # or
   yarn install
   ```

3. Configure environment variables:
   Create a `.env` file in the root directory with the following variables:
   ```
   DATABASE_URL=your_database_connection_string
   NEXT_PUBLIC_CLERK_FRONTEND_API=your_clerk_frontend_api
   CLERK_API_KEY=your_clerk_api_key
   CLERK_JWT_KEY=your_clerk_jwt_key
   ```

4. Run database migrations:
   ```bash
   npx prisma migrate deploy
   ```

5. Start the development server:
   ```bash
   npm run dev
   # or
   yarn dev
   ```

6. Open your browser and navigate to `http://localhost:3000`

## Usage Guide

### User Onboarding
- New users must sign in using Clerk authentication.
- Upon first login, users are redirected to the onboarding page.
- Users complete their profile by selecting their industry, specialization, and providing experience, skills, and a professional bio.
- The onboarding form validates inputs and submits data to update the user profile.
- If the user is not authenticated during profile completion, they are redirected to the sign-in page with an error message.

### Dashboard
- After onboarding, users are redirected to the dashboard.
- The dashboard displays personalized industry insights and career recommendations based on the user's profile.

### Error Handling
- Unauthorized access attempts redirect users to the sign-in page.
- Form validation errors are displayed inline.
- Server errors during profile update show toast notifications.

## Technologies Used
- Next.js 13 with App Router
- React Hook Form and Zod for form handling and validation
- Prisma ORM for database access
- Clerk for user authentication
- Tailwind CSS for styling
- Sonner for toast notifications

## Contributing
Contributions are welcome! Please open issues or pull requests for bug fixes and feature requests.

## License
This project is licensed under the MIT License.

---

For any questions or support, please contact the project maintainer.
