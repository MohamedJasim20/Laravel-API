Laravel API CRUD Project

This project is a Laravel-based REST API with CRUD operations. It includes authentication using Laravel Passport and follows the Entity-Attribute-Value (EAV) model for handling dynamic attributes.

Features

User authentication (Register, Login, Logout) using Laravel Passport.

CRUD operations for Users, Projects, and Timesheets.

Entity-Attribute-Value (EAV) model for dynamic attributes.

Filtering capabilities using standard and EAV attributes.

Database migrations and seeders.

Requirements

PHP 8.0+

Composer

MySQL or any supported database

Laravel 8+

Installation

Step 1: Clone the Repository

git clone https://github.com/your-repo/laravel-api-crud.git
cd laravel-api-crud

Step 2: Install Dependencies

composer install

Step 3: Configure Environment

Copy the .env.example file and set up your database credentials:

cp .env.example .env

Update .env with your database configuration:

DB_DATABASE=laravel_db
DB_USERNAME=root
DB_PASSWORD=

Step 4: Generate Application Key

php artisan key:generate

Step 5: Run Migrations

php artisan migrate

Step 6: Install Laravel Passport

php artisan passport:install

Step 7: Seed Database (Optional)

php artisan db:seed

Step 8: Serve the Application

php artisan serve

API Endpoints

Authentication

Register: POST /api/register

Login: POST /api/login

Logout: POST /api/logout

Project Management

Get all projects: GET /api/projects

Get project by ID: GET /api/projects/{id}

Create a project: POST /api/projects

Update a project: PUT /api/projects/{id}

Delete a project: DELETE /api/projects/{id}

Filtering

You can filter projects using standard and EAV attributes with operators (=, >, <, LIKE). Example:

GET /api/projects?name=MyProject

License

This project is open-source and available under the MIT License.
