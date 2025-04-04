# CreatorFlow Project

CreatorFlow is a YouTube content management platform designed to help creators organize and streamline their video production process using a Trello-like interface.

## Project Structure

This project consists of two main repositories that work together:

1. [**CreatorFlow Landing Page**](https://github.com/saifaleee/CreatorFlow-Landing-Page) - A modern, responsive landing page that introduces users to the platform's features and benefits.

2. [**YT-Trello Application**](https://github.com/saifaleee/YT-Trello) - The main application, featuring a Trello-like interface tailored specifically for YouTube content creators.

## Features

### Landing Page
- Modern, responsive design
- Feature showcases
- Pricing information
- Testimonials
- Call-to-action buttons integrated with the main application
- Seamless navigation to authentication pages

### Main Application (YT-Trello)
- Kanban-style board management
- Video content organization by production stage
- Drag-and-drop interface
- User authentication and authorization
- Workspace and board management
- Task assignment and tracking
- Rich content cards for video ideas

## How They Connect

The two applications work together to provide a complete user experience:

1. Users discover CreatorFlow through the landing page
2. "Get Started" and navigation buttons on the landing page redirect to the main application
3. Authentication happens in the main application
4. Users can navigate back to the landing page from the main application
5. URL parameters maintain context between applications

## Technical Implementation

- Both applications are built with React + TypeScript
- Styling uses Tailwind CSS
- Backend API is built with Node.js and Express
- PostgreSQL database stores user, workspace, and board data
- CORS is configured to allow secure communication between services

## Setup Instructions

### Prerequisites
- Node.js (v16+)
- npm or yarn
- PostgreSQL database

### Landing Page Setup
1. Clone the repository
   ```bash
   git clone https://github.com/saifaleee/CreatorFlow-Landing-Page.git
   cd CreatorFlow-Landing-Page
   ```

2. Install dependencies
   ```bash
   npm install
   ```

3. Start the development server
   ```bash
   npm run dev -- --port 5174
   ```

### Main Application Setup
1. Clone the repository
   ```bash
   git clone https://github.com/saifaleee/YT-Trello.git
   cd YT-Trello
   ```

2. Install dependencies
   ```bash
   npm install
   ```

3. Set up the backend
   ```bash
   cd backend
   npm install
   ```

4. Configure environment variables
   Create a `.env` file in the backend directory with:
   ```
   PORT=5000
   DB_USER=your_db_user
   DB_HOST=localhost
   DB_DATABASE=yt_trello_db
   DB_PASSWORD=your_db_password
   DB_PORT=5432
   JWT_SECRET=your_very_secret_key_please_change
   JWT_EXPIRES_IN=1d
   ```

5. Start the backend server
   ```bash
   npm run dev
   ```

6. In another terminal, start the frontend
   ```bash
   cd ..
   npm run dev -- --port 5175
   ```

7. Access the applications:
   - Landing Page: http://localhost:5174
   - Main Application: http://localhost:5175

## Development and Deployment

Both repositories should be developed and deployed separately, but with careful coordination to ensure the integration points work correctly, especially:

- URL paths for navigation between applications
- API endpoint references
- Authentication flows

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request to either repository.

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Contact

For questions or feedback, please open an issue on the relevant repository.
