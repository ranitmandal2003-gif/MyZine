# MyZine - Magazine Management System

A PHP-based web application for managing and publishing digital magazines with an admin dashboard.

## Features

- **Admin Dashboard** - Manage magazines, categories, users, and system settings
- **Magazine Management** - Create, edit, and publish digital magazines
- **User Authentication** - Secure login system for admins and authors
- **Responsive Design** - Works on desktop and mobile devices
- **Cover Management** - Custom branding with logo and cover images
- **Comments System** - Readers can comment on magazines

## Requirements

- PHP 7.4 or higher
- MySQL 5.7 or higher
- Apache Web Server (or compatible)
- Composer (for dependency management)

## Installation

### Local Setup

1. Clone the repository:
   ```bash
   git clone <your-repo-url>
   cd magazines
   ```

2. Create a MySQL database:
   ```sql
   CREATE DATABASE magazines_db;
   ```

3. Import the database schema (if provided):
   ```bash
   mysql -u root magazines_db < database.sql
   ```

4. Configure environment variables:
   ```bash
   cp .env.example .env
   ```

5. Update `.env` with your database credentials

6. Run on local server:
   ```bash
   php -S localhost:8000
   ```

### Render Deployment

1. Push your code to GitHub
2. Connect your GitHub repository to Render
3. Set up the following in Render:
   - **Build Command**: `composer install` (if using Composer)
   - **Start Command**: Not needed for static hosting
   - **Environment Variables**: Set DB credentials in Render dashboard

4. Configure your database (use Render's PostgreSQL or external MySQL)

## Project Structure

```
├── admin/              # Admin panel
│   ├── categories/    # Category management
│   ├── magazines/     # Magazine management
│   ├── users/         # User management
│   └── inc/           # Include files
├── classes/           # PHP classes
├── plugins/           # Third-party libraries
├── uploads/           # User uploads
├── index.php          # Main entry point
└── config.php         # Configuration
```

## Default Admin Login

Username: `dev_oretnom`
Password: `5da283a2d990e8d8512cf967df5bc0d0`

**⚠️ Change this immediately in production!**

## Configuration

Edit `initialize.php` or use environment variables:

```php
define('DB_SERVER', getenv('DB_SERVER') ?: 'localhost');
define('DB_USERNAME', getenv('DB_USERNAME') ?: 'root');
define('DB_PASSWORD', getenv('DB_PASSWORD') ?: '');
define('DB_NAME', getenv('DB_NAME') ?: 'magazines_db');
define('base_url', getenv('BASE_URL') ?: 'http://localhost/magazines/');
```

## License

This project is proprietary.

## Support

For issues or questions, please create an issue on GitHub.
