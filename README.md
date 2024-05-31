# boxigo-backend

# My Express API

This project is a simple Express.js API deployed using Vercel. The API fetches data from an external source and provides it via an endpoint.

## Table of Contents

- [Project Structure](#project-structure)
- [Installation](#installation)
- [Running Locally](#running-locally)
- [Deployment](#deployment)
- [Environment Variables](#environment-variables)
- [Usage](#usage)

## Project Structure

\`\`\`
my-express-app/
├── api/
│   └── index.js
├── package.json
├── vercel.json
└── .env
\`\`\`

- **api/index.js**: The main Express.js application file.
- **package.json**: Contains project metadata and dependencies.
- **vercel.json**: Configuration file for Vercel deployment.
- **.env**: Environment variables file.

## Installation

1. Clone the repository:
   \`\`\`bash
   git clone https://github.com/mdamir-012/boxigo-backend.git
   cd my-express-app
   \`\`\`

2. Install dependencies:
   \`\`\`bash
   npm install
   \`\`\`

## Running Locally

1. Create a \`.env\` file in the root directory and add your environment variables:
   \`\`\`
   PORT=3001
   BACK_API_URL=http://test.api.boxigo.in/sample-data/
   \`\`\`

2. Start the development server:
   \`\`\`bash
   npm start
   \`\`\`

3. Your API will be running on \`http://localhost:3001\`.

## Deployment

1. Ensure you have the Vercel CLI installed. If not, install it globally:
   \`\`\`bash
   npm install -g vercel
   \`\`\`

2. Deploy the project to Vercel:
   \`\`\`bash
   vercel
   \`\`\`

3. Follow the prompts to complete the deployment. Vercel will provide a URL where your API is accessible.

## Environment Variables

Ensure you have the following environment variables set either in your local \`.env\` file or in the Vercel dashboard for your deployed project:

- **PORT**: The port your API will run on (default is \`3001\`).
- **BACK_API_URL**: The URL of the backend API from which data will be fetched.

## Usage

### Endpoint

- **GET /api/sample-data**

  Fetches data from the backend API specified in the environment variable \`BACK_API_URL\`.

  **Response:**
  - \`200 OK\`: Returns the data fetched from the backend API.
  - \`500 Internal Server Error\`: Failed to fetch data.

### Example Request

\`\`\`bash
curl https://<your-project-name>.vercel.app/api/sample-data
\`\`\`

Replace \`<your-project-name>\` with the actual name of your Vercel project.
