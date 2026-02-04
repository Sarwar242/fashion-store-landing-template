# Fashion Store - Modern E-commerce Template

A beautiful, responsive e-commerce template for fashion stores built with PHP, HTML5, CSS3, and JavaScript. Features a modern design with Docker support for easy deployment.

![License](https://img.shields.io/badge/license-MIT-blue.svg)
![PHP](https://img.shields.io/badge/PHP-8.2-777BB4?logo=php)
![Docker](https://img.shields.io/badge/Docker-Ready-2496ED?logo=docker)
![MySQL](https://img.shields.io/badge/MySQL-8.0-4479A1?logo=mysql)

## ✨ Features

- 🎨 **Modern Design** - Clean and elegant UI with responsive layout
- 🛒 **E-commerce Ready** - Product listings, categories, and shopping cart interface
- 🐳 **Docker Support** - Containerized deployment with Docker Compose
- 💾 **MySQL Database** - Pre-configured database connection
- 📱 **Fully Responsive** - Works seamlessly on desktop, tablet, and mobile devices
- ⚡ **Fast & Lightweight** - Optimized assets and minimal dependencies
- 🎭 **Multiple Sections** - Homepage, products, blog, newsletter, and more

## 📸 Preview

The template includes:
- Hero banner with product showcases
- Product collections and categories
- Featured items and deals
- Blog section
- Newsletter signup
- Instagram feed integration
- Customer testimonials
- Footer with social media links

## 🚀 Quick Start

### Prerequisites

- **Docker** and **Docker Compose** installed on your system
- Or alternatively: PHP 8.2+, Apache/Nginx, and MySQL 8.0+

### Option 1: Using Docker (Recommended)

1. **Clone the repository**
   ```bash
   git clone https://github.com/yourusername/fashion-store.git
   cd fashion-store
   ```

2. **Start the application**
   ```bash
   docker-compose up -d
   ```

3. **Access the application**
   - Web Application: [http://localhost:9082](http://localhost:9082)
   - MySQL Database: `localhost:3307`

That's it! The application is now running with MySQL database.

### Option 2: Manual Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/yourusername/fashion-store.git
   cd fashion-store
   ```

2. **Configure your web server**
   - Point document root to the project directory
   - Ensure PHP 8.2+ with mysqli extension is installed

3. **Setup database**
   - Create a MySQL database
   - Update `db-config.php` with your credentials

4. **Access via browser**
   - Navigate to your configured local URL

## 🗄️ Database Configuration

### Docker Environment (Automatic)

When using Docker, the database connection is automatically configured via environment variables.

**Connection Details:**
- **Host:** `localhost` (from host machine) or `mysql` (from container)
- **Port:** `3307` (external) / `3306` (internal)
- **Database:** `phpproject`
- **Username:** `phpuser`
- **Password:** `phppassword`

### Manual Configuration

Edit `db-config.php` to configure your database connection:

```php
<?php
$host = 'localhost';
$dbname = 'your_database';
$username = 'your_username';
$password = 'your_password';
```

## 📁 Project Structure

```
fashion-store/
├── index.php              # Main application file
├── style.css              # Custom styles
├── db-config.php          # Database configuration
├── docker-compose.yml     # Docker services configuration
├── Dockerfile             # Docker image definition
├── .dockerignore          # Docker ignore rules
├── css/                   # Stylesheets
│   ├── vendor.css
│   ├── normalize.css
│   └── swiper-bundle.min.css
├── js/                    # JavaScript files
│   ├── jquery.min.js
│   ├── plugins.js
│   └── script.min.js
└── images/                # Image assets
    ├── products/
    ├── banners/
    └── logos/
```

## 🐳 Docker Commands

### Basic Operations

```bash
# Start all services
docker-compose up -d

# Stop all services
docker-compose down

# View logs
docker-compose logs -f

# Rebuild after changes
docker-compose up -d --build

# Stop specific service
docker-compose stop web-9082
```

### Database Operations

```bash
# Connect to MySQL from host
mysql -h 127.0.0.1 -P 3307 -u phpuser -p
# Password: phppassword

# Access MySQL container shell
docker exec -it php-project-mysql mysql -u root -p
# Password: rootpassword
```

For more Docker commands and troubleshooting, see [README-DOCKER.md](README-DOCKER.md).

## 🎨 Customization

### Styling

- **Primary Styles:** Edit `style.css`
- **Vendor Styles:** Located in `css/` directory
- **Colors & Fonts:** Configured in CSS variables at the top of `style.css`

### Content

- **Main Content:** Edit `index.php`
- **Images:** Replace files in `images/` directory
- **Products:** Modify product sections in `index.php`

### Database Integration

The template includes database configuration but requires you to implement specific features:
- Product management
- User authentication
- Shopping cart functionality
- Order processing

## 🛠️ Technology Stack

- **Frontend:**
  - HTML5
  - CSS3 (Bootstrap 5.3)
  - JavaScript (jQuery)
  - Swiper.js for carousels
  - Google Fonts (Jost, Marcellus)

- **Backend:**
  - PHP 8.2
  - MySQL 8.0
  - Apache 2.4

- **DevOps:**
  - Docker
  - Docker Compose

## 📦 Dependencies

### PHP Extensions Required:
- mysqli
- pdo
- pdo_mysql

### Frontend Libraries (CDN):
- Bootstrap 5.3.0
- Swiper.js 9
- jQuery (included locally)

## 🔒 Security

This project has been thoroughly security-checked and cleaned. See [SECURITY_REPORT.md](SECURITY_REPORT.md) for details.

**Security Best Practices:**
- ✅ Use Docker containers for isolation
- ✅ Keep all dependencies updated
- ✅ Never commit sensitive credentials to Git
- ✅ Use environment variables for configuration
- ✅ Sanitize all user inputs
- ✅ Use prepared statements for database queries

## 📝 To-Do / Roadmap

- [ ] Implement shopping cart functionality
- [ ] Add user authentication system
- [ ] Create admin panel
- [ ] Add payment gateway integration
- [ ] Implement product search
- [ ] Add product filters and sorting
- [ ] Create database schema and migrations
- [ ] Add product reviews system
- [ ] Implement order management
- [ ] Add email notifications

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the LICENSE file for details.

## 🙏 Acknowledgments

- Design inspired by modern e-commerce platforms
- Icons and fonts from Google Fonts and Bootstrap Icons
- Template structure based on modern web development best practices

## 📞 Support

If you encounter any issues or have questions:
- 🐛 Open an issue on GitHub
- 📧 Contact: info@sarwar.com.bd
- 💬 Discussions: Use GitHub Discussions tab

## 🌟 Show Your Support

If you find this project useful, please consider giving it a ⭐ on GitHub!

---

**Made with ❤️ for the open-source community**
