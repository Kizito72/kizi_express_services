# Kizi Express Services - Global Logistics & Transport Platform

## Project Overview

**Kizi Express Services** is a comprehensive web-based logistics and transportation management platform designed to provide global freight forwarding, sea/air charter, customs clearance, 3PL warehousing, and mobile freight services.

---

## Table of Contents

1. [Project Structure](#project-structure)
2. [Technology Stack](#technology-stack)
3. [Installation & Setup](#installation--setup)
4. [Key Features](#key-features)
5. [Admin Features](#admin-features)
6. [Customer Features](#customer-features)
7. [Database Schema](#database-schema)
8. [API Documentation](#api-documentation)
9. [Security](#security)
10. [Troubleshooting](#troubleshooting)

---

## Project Structure

```
kizi_express_services/
├── index.html                          # Main landing page
├── css/                                # Stylesheets
│   ├── testimony.css                   # Testimonial carousel styling
│   └── (other CSS files)
├── js/                                 # JavaScript files
│   └── testimoy.js                     # Testimonial carousel functionality
├── images/                             # Image assets
├── tracking-portal/                      # Shipment tracking & management module
│   ├── index.php                       # Main tracking page
│   ├── login.php                       # User login
│   ├── signup.php                      # New user registration
│   ├── tracking.php                    # Track shipments
│   ├── main-admin/                        # Core admin panel
│   │   ├── admin.php                   # Admin dashboard
│   │   ├── customer.php                # Customer management
│   │   ├── courier-list.php            # Courier management
│   │   ├── add-courier.php             # Add new courier
│   │   ├── add-new-users.php           # Add users
│   │   ├── add-office.php              # Add office locations
│   │   ├── delivery-list.php           # View deliveries
│   │   ├── delivered-list.php          # Completed deliveries
│   │   ├── list-of-shipping-paid.php   # Paid shipments
│   │   ├── list-of-shipping-cash-on-delivery.php  # COD shipments
│   │   ├── online-bookings.php         # Online booking management
│   │   ├── funciones.php               # Core library functions
│   │   ├── library.php                 # Utility functions
│   │   ├── database.php                # Database connection
│   │   ├── admin-panel-customer.php    # Customer portal
│   │   ├── search-courier.php          # Courier search
│   │   └── DB/
│   │       └── kodzzjwa_delivery.sql   # Database schema
│   └── main-admin_components/             # Reusable components
├── services/                           # Service pages
│   ├── index.html
│   └── post40a9.html
├── freight-forwarding-services/
├── customs-clearance-services/
├── 3pl-logistics-warehousing/
├── air-and-sea-charter/
├── mobile-freight-services/
├── pick-and-pack/
├── project-cargo/
├── transportation-and-distribution/
├── about-us/
├── careers/
├── contact-us/
└── wp-content/                         # WordPress content & plugins
    ├── plugins/
    ├── themes/
    └── uploads/
```

---

## Technology Stack

### Frontend
- **HTML5** - Semantic markup
- **CSS3** - Responsive styling (Bootstrap, custom)
- **JavaScript** - ES5/jQuery for interactivity
- **Bootstrap Framework** - Responsive grid & components
- **Font Awesome** - Icon library

### Backend
- **PHP 5.6+** - Server-side scripting
- **MySQL/MariaDB** - Relational database
- **WordPress** - CMS integration (optional)

### Libraries & Tools
- **jQuery** - DOM manipulation
- **FPDF** - PDF generation for invoices
- **DOMPDF** - HTML to PDF conversion
- **Bootstrap 3** - Frontend framework
- **Font Awesome 4.7** - Icon set

---

## Installation & Setup

### Prerequisites
- PHP 5.6 or higher
- MySQL 5.6 or higher
- Apache/Nginx web server
- WAMP, LAMP, or XAMPP stack

### Step-by-Step Installation

1. **Clone/Download Project**
   ```bash
   git clone <repository-url>
   cd kizi_express_services
   ```

2. **Database Setup**
   - Create a new MySQL database
   - Import the schema: `tracking-portal/DB/kodzzjwa_delivery.sql`
   ```bash
   mysql -u root -p database_name < tracking-portal/DB/kodzzjwa_delivery.sql
   ```

3. **Configure Database Connection**
   - Edit `tracking-portal/main-admin/database-settings.php`
   - Update database credentials:
   ```php
   define('DB_HOST', 'localhost');
   define('DB_USER', 'root');
   define('DB_PASSWORD', 'your_password');
   define('DB_NAME', 'delivery_db');
   ```

4. **Configure Web Server**
   - Point your web root to the `kizi_express_services` directory
   - Ensure `.htaccess` files are enabled

5. **Set File Permissions**
   ```bash
   chmod 755 tracking-portal/main-admin/
   chmod 755 tracking-portal/upload/
   chmod 755 tracking-portal/reports_pdf/
   ```

6. **Access the Application**
   - Frontend: `http://localhost/kizi_express_services/`
   - Admin Panel: `http://localhost/kizi_express_services/tracking-portal/main-admin/admin.php`
   - Customer Portal: `http://localhost/kizi_express_services/tracking-portal/main-admin/admin-panel-customer.php`

---

## Key Features

### 1. **Testimonial Carousel**
- Auto-sliding testimonials every 5 seconds
- Smooth fade and slide-from-right animations
- Manual navigation with previous/next arrows
- Pause on hover functionality
- Fully responsive design
- **Files:** `js/testimoy.js`, `css/testimony.css`

### 2. **Service Pages**
- 8+ service categories with dedicated pages
- Responsive layouts
- SEO optimized
- Service descriptions and benefits

### 3. **Tracking System**
- Real-time shipment tracking
- Multiple tracking statuses
- Customer and admin views
- Tracking number generation

### 4. **User Management**
- Customer registration & login
- Admin user management
- Role-based access control
- User profile management

### 5. **Shipment Management**
- Create new shipments
- Track shipment status
- Update delivery information
- Generate invoices and reports

### 6. **Payment Processing**
- Cash on Delivery (COD) support
- Pre-paid shipping options
- Payment status tracking
- Invoice generation

---

## Admin Features

### Dashboard
Located in: `tracking-portal/main-admin/admin.php`

#### Key Administrative Functions:

1. **Shipment Management**
   - View all shipments
   - Filter by status (pending, in-transit, delivered)
   - Update shipment details
   - Generate shipping labels and invoices

2. **Courier Management** (`courier-list.php`, `add-courier.php`)
   - Add new couriers
   - View all couriers
   - Edit courier information
   - Track courier activities

3. **Customer Management** (`add-new-users.php`, `customer.php`)
   - Add new customers
   - View customer profiles
   - Update customer information
   - Track customer orders

4. **Office Management** (`add-office.php`)
   - Add new office locations
   - Manage multiple locations
   - Set office operational details

5. **Delivery Tracking**
   - View pending deliveries
   - Mark deliveries as completed
   - Track delivery performance

6. **Reports & Analytics**
   - Shipping reports
   - Revenue reports
   - Delivery performance metrics
   - Financial summaries

7. **Payment Management**
   - COD payments
   - Paid shipments verification
   - Financial reconciliation
   - Transaction history

#### Admin Access Points:
- **Main Admin Panel:** `tracking-portal/main-admin/admin.php`
- **Courier Management:** `tracking-portal/main-admin/courier-list.php`
- **Customer Management:** `tracking-portal/main-admin/customer.php`
- **Shipment List:** `tracking-portal/main-admin/shipping-list.php`
- **Delivered List:** `tracking-portal/main-admin/delivered-list.php`
- **Online Bookings:** `tracking-portal/main-admin/online-bookings.php`

---

## Customer Features

### Customer Portal
Located in: `tracking-portal/main-admin/admin-panel-customer.php`

#### Available Features:

1. **Shipment Booking**
   - Create new shipments
   - Select delivery options
   - Choose payment method

2. **Tracking**
   - Track shipments in real-time
   - View shipment history
   - Get status notifications

3. **Shipment History**
   - View all past shipments
   - Filter by date and status
   - Download invoices

4. **Account Management**
   - Update profile information
   - Change password
   - View account details

5. **Payment Information**
   - View payment history
   - Download receipts
   - Outstanding balance tracking

#### Customer Access Points:
- **Login Page:** `tracking-portal/login.php`
- **Sign Up:** `tracking-portal/signup.php`
- **Tracking:** `tracking-portal/tracking.php`
- **Customer Portal:** `tracking-portal/main-admin/admin-panel-customer.php`

---

## Database Schema

### Key Tables

#### `users`
- User authentication and profiles
- Stores customer and admin information
- Manages login credentials

#### `shipments`
- Shipment records
- Tracks origin, destination, weight
- Stores tracking information

#### `couriers`
- Courier information
- Delivery personnel management
- Performance tracking

#### `offices`
- Company office locations
- Geographic coverage areas

#### `payments`
- Payment transactions
- Invoice tracking
- COD payments

#### `deliveries`
- Delivery status updates
- Delivery assignment management
- Completion tracking

#### `company`
- Company profile information
- Settings and configuration

### Database Location
- **Schema File:** `tracking-portal/DB/kodzzjwa_delivery.sql`
- **Connection File:** `tracking-portal/main-admin/database.php`

---

## API Documentation

### Authentication

#### Login
- **Endpoint:** POST `/tracking-portal/process.php`
- **Parameters:**
  - `action=login`
  - `username` - User email/username
  - `password` - User password
  - `user_type` - 'admin' or 'customer'

#### Logout
- **Endpoint:** POST `/tracking-portal/process.php`
- **Parameters:**
  - `action=logout`

### Shipment Endpoints

#### Create Shipment
- **Endpoint:** POST `/tracking-portal/main-admin/process.php`
- **Parameters:**
  - `action=add_shipment`
  - `origin` - Starting location
  - `destination` - Ending location
  - `weight` - Package weight
  - `description` - Package description
  - `customer_id` - Customer ID

#### Get Shipment Status
- **Endpoint:** GET `/tracking-portal/tracking.php`
- **Parameters:**
  - `tracking_number` - Shipment tracking number

#### Update Shipment
- **Endpoint:** POST `/tracking-portal/main-admin/process.php`
- **Parameters:**
  - `action=update_shipment`
  - `shipment_id` - Shipment ID
  - `status` - New status

### Reports Endpoints

#### Generate Invoice
- **Endpoint:** `/tracking-portal/main-admin/print-invoice/`
- **Parameters:**
  - `shipment_id` - Shipment ID

#### Generate Delivery Report
- **Endpoint:** `/tracking-portal/main-admin/reports_pdf/`
- **Parameters:**
  - `report_type` - Type of report
  - `date_from` - Start date
  - `date_to` - End date

---

## Security

### Important Security Measures

1. **Input Validation**
   - All user inputs are validated
   - SQL injection prevention via prepared statements
   - XSS protection through output encoding

2. **Authentication**
   - Session-based authentication
   - Password hashing (ensure bcrypt or similar)
   - Role-based access control (RBAC)

3. **File Uploads**
   - Restricted file types
   - Size limitations
   - Secure upload directories outside web root

4. **Database Security**
   - Use strong database passwords
   - Regular backups
   - Principle of least privilege for DB users

5. **HTTPS**
   - Ensure SSL/TLS is enabled
   - Redirect HTTP to HTTPS
   - Update all URLs to use HTTPS

### Recommendations

- Regularly update PHP and MySQL
- Implement Web Application Firewall (WAF)
- Monitor access logs
- Implement rate limiting on login attempts
- Use environment variables for sensitive config
- Enable security headers (CSP, X-Frame-Options, etc.)

---

## Troubleshooting

### Common Issues

#### 1. Database Connection Error
**Error:** "Unable to connect to database"
**Solution:**
- Check database credentials in `database.php`
- Verify MySQL service is running
- Ensure database user has proper permissions
- Test connection: `mysqli_connect('localhost', 'user', 'password', 'database')`

#### 2. Login Issues
**Error:** "Invalid username or password"
**Solution:**
- Verify credentials are correct
- Check if user exists in database
- Clear session/cookies and try again
- Check `isUser()` function in `library.php`

#### 3. File Upload Errors
**Error:** "Upload failed"
**Solution:**
- Check directory permissions (755)
- Verify file size limits
- Check file type restrictions
- Ensure upload directories exist

#### 4. Carousel Not Sliding
**Error:** Testimonials not auto-rotating
**Solution:**
- Check if `js/testimoy.js` is loaded
- Verify jQuery is loaded before custom JS
- Check browser console for JavaScript errors
- Ensure CSS is applied correctly

#### 5. PDF Generation Issues
**Error:** "Unable to generate PDF"
**Solution:**
- Check FPDF/DOMPDF library availability
- Verify file write permissions
- Check available disk space
- Review error logs

### Debug Mode

Enable debug mode in `tracking-portal/main-admin/library.php`:
```php
error_reporting(E_ALL);
ini_set('display_errors', 1);
```

### Log Files

- **PHP Error Log:** Check server error_log file
- **Database Log:** Enable MySQL query logging
- **Application Log:** Check `tracking-portal/main-admin/error_log`

---

## Maintenance

### Regular Tasks

1. **Database Maintenance**
   - Weekly: Optimize tables
   - Monthly: Backup database
   - Quarterly: Archive old records

2. **File System**
   - Clean temporary files
   - Archive old reports
   - Manage upload storage

3. **Security**
   - Update dependencies
   - Review access logs
   - Test backup restore

4. **Performance**
   - Monitor response times
   - Optimize slow queries
   - Cache optimization

---

## Contact & Support

- **Email:** kizzy.ngo@gmail.com
