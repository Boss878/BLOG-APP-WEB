Blog Web Application
This is a web-based blog platform built using Angular for the frontend and ASP.NET Core for the backend. The application allows users to create, edit, and manage blog posts with support for categories, live markdown previews, and image handling.

Table of Contents
Features
Technologies Used
Setup Instructions
API Endpoints
Contributing
License
Features
Blog Management: Create, edit, and delete blog posts with rich content support (Markdown syntax).
Category Management: Assign multiple categories to blog posts and manage categories easily.
Live Preview: Real-time preview of markdown content and images while creating or editing blog posts.
Admin Dashboard: Manage blog posts and categories from a dedicated admin interface.
Responsive Design: Fully responsive UI with a user-friendly experience on desktop and mobile devices.
Technologies Used
Frontend
Angular: Frontend framework for building a dynamic, single-page application (SPA).
TypeScript: Typed superset of JavaScript used in Angular development.
HTML/CSS: Markup and styling for the frontend UI.
Backend
ASP.NET Core: Backend framework for building the API.
Entity Framework Core: ORM for managing the database and migrations.
SQL Server: Relational database used for storing blog data.
Tools
Swagger: API documentation and testing tool used in the backend.
Postman: API testing and debugging.
Visual Studio Code: IDE for both frontend and backend development.
Setup Instructions
Prerequisites
Node.js (for Angular): Download and install from Node.js official site.
.NET 6 SDK: Download and install from Microsoft official site.
SQL Server: Set up a local SQL Server instance or use a cloud service.
Step 1: Clone the Repository
bash
Copy code
git clone https://github.com/your-username/your-repo-name.git
cd your-repo-name
Step 2: Set Up the Backend
Navigate to the backend project directory:
bash
Copy code
cd API/BlogAppAPI/BlogAppAPI
Update the connection string in appsettings.json to match your SQL Server instance:
json
Copy code
"DefaultConnection": "Server=localhost;Database=BlogDb;Trusted_Connection=True;TrustServerCertificate=True;"
Apply the database migrations:
bash
Copy code
dotnet ef database update
Run the backend API:
bash
Copy code
dotnet run
The API will be available at https://localhost:7156/swagger/index.html.
Step 3: Set Up the Frontend
Navigate to the frontend project directory:
bash
Copy code
cd WEB/Blog/src
Install the dependencies:
bash
Copy code
npm install
Update the apiUrl in environment.ts and environment.staging.ts to match your API URL:
typescript
Copy code
export const environment = {
    production: false,
    apiUrl: 'https://localhost:7156/api'
};
Run the frontend:
bash
Copy code
ng serve
The application will be available at http://localhost:4200.
API Endpoints
The API includes the following endpoints:

Blog Posts:
GET /api/blogposts: Get all blog posts.
POST /api/blogposts: Create a new blog post.
PUT /api/blogposts/{id}: Update an existing blog post.
DELETE /api/blogposts/{id}: Delete a blog post.
Categories:
GET /api/categories: Get all categories.
POST /api/categories: Create a new category.
PUT /api/categories/{id}: Update an existing category.
DELETE /api/categories/{id}: Delete a category.
For more detailed API documentation, visit the Swagger UI.

Contributing
Contributions are welcome! Please fork the repository and create a pull request with your changes.

Fork the repository.
Create a feature branch (git checkout -b feature/your-feature).
Commit your changes (git commit -m 'Add some feature').
Push to the branch (git push origin feature/your-feature).
Create a new Pull Request.
License
This project is licensed under the MIT License - see the LICENSE file for details.

Feel free to customize this README.md further based on the specific needs of your project.
