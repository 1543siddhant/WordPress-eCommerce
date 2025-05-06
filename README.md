## Organic Store Website 📦

A clean, eco-friendly e-commerce site built on WordPress to showcase and sell organic products.

**Live Demo:** [Organic Store Demo](https://dev-siddhant-ecommerce2.pantheonsite.io/)  
**YouTube Walkthrough:** [Watch Demo Video](https://youtu.be/R9vVAzHpMs8)

---

## Table of Contents

1. [Project Overview](#project-overview)  
2. [WordPress Theory & Architecture](#wordpress-theory--architecture)  
3. [Setup & Installation](#setup--installation)  
4. [Execution Steps](#execution-steps)  
5. [Directory Structure](#directory-structure)  
6. [Screenshots](#screenshots)  
7. [Deployment](#deployment)  
8. [Contributing](#contributing)  
9. [License](#license)  

---

## Project Overview

Organic Store is a WordPress-powered e-commerce platform designed to provide customers with a seamless shopping experience for organic goods. Key features include:

- **Custom Theme** tailored for organic branding  
- **WooCommerce Integration** for product catalog, cart, and checkout  
- **SEO Optimization** with Yoast SEO plugin  
- **Responsive Design** for desktop and mobile  

---

## WordPress Theory & Architecture

WordPress is an open-source Content Management System (CMS) written in PHP and paired with a MySQL or MariaDB database. It powers over 43% of all websites, providing a flexible architecture through **Themes** for presentation and **Plugins** for functionality.

### Core Components

1. **Themes** control the visual design (templates, stylesheets).  
2. **Plugins** extend functionality (e.g., WooCommerce, Yoast SEO).  
3. **Database** stores posts, pages, users, settings in MySQL/MariaDB.  
4. **wp-config.php** file holds database connection info and salts.  

### How It Works

- **Request Flow**: Browser → WordPress PHP scripts → Database → Rendered HTML  
- **Template Hierarchy**: Defines which PHP template loads for each page type.  
- **Hook System**: Actions & Filters let themes/plugins modify core behavior without editing core files.  

---

## Setup & Installation

Follow these steps to set up the project locally or on your Pantheon environment:

### Clone Repository  
```bash
git clone https://github.com/your-username/organic-store.git
cd organic-store
```

### Create Database  
In Pantheon or your local MySQL:

```sql
CREATE DATABASE wp_organic;
```

### Download & Extract WordPress  
```bash
wget https://wordpress.org/latest.zip
unzip latest.zip
mv wordpress/* .
```

### Configure wp-config.php  
```php
define('DB_NAME', 'wp_organic');
define('DB_USER', 'your_db_user');
define('DB_PASSWORD', 'your_db_pass');
define('DB_HOST', 'localhost');
```

### Install Dependencies  
Ensure PHP ≥7.4, MySQL, Apache/Nginx are installed.

### Run Installer  
Navigate to:  
[https://dev-siddhant-ecommerce2.pantheonsite.io/wp-admin/install.php](https://dev-siddhant-ecommerce2.pantheonsite.io/wp-admin/install.php)  
and follow the on-screen prompts.

---

## Execution Steps

### Activate Theme & Plugins

- Go to **Appearance → Themes**, activate your custom theme.  
- Go to **Plugins → Installed Plugins**, activate WooCommerce and Yoast SEO.

### Configure WooCommerce

- Store Setup Wizard: Add store address, currency, shipping & tax.  
- **Products → Add New**: Create product entries with images (apple1.jpg–apple5.jpg).

### Set Up Menus & Widgets

- **Appearance → Menus**: Create Main Menu linking to Home, Shop, Blog, Contact.  
- **Appearance → Widgets**: Add Search, Recent Products, Cart in sidebar.

### Customize Theme

- Under **Appearance → Customize**:  
  - Site Identity (logo, tagline)  
  - Colors & Typography  
  - Homepage Settings

### SEO & Performance

- Configure Yoast SEO meta titles and descriptions for each page.  
- Install **W3 Total Cache** and generate static assets.

---

## Directory Structure

```
├── wp-admin/
├── wp-content/
│   ├── themes/
│   │   └── organic-store-theme/
│   ├── plugins/
│   │   ├── woocommerce/
│   │   └── yoast-seo/
│   └── uploads/
│       └── 2025/05/
│           └── apple1.jpg … apple5.jpg  
├── wp-includes/
├── index.php
├── wp-config.php
└── README.md
```

---

## Screenshots

- `apple1.jpg` – Homepage with hero banner showcasing organic produce.  
- `apple2.jpg` – Shop page listing products with filters.  
- `apple3.jpg` – Single product detail page with “Add to Cart”.  
- `apple4.jpg` – Cart overview before checkout.  
- `apple5.jpg` – Custom contact form powered by WPForms.

---

## Deployment

- **Pantheon**: Push branch to Pantheon Git, deploy via Dashboard.  
- **Backup**: Use Pantheon Automated Backups.  
- **SSL**: Enable free Let’s Encrypt certificate in Pantheon Dashboard.

---

## Contributing

1. Fork the repo  
2. Create feature branch (`git checkout -b feature-name`)  
3. Commit changes (`git commit -m 'Add new feature'`)  
4. Push (`git push origin feature-name`)  
5. Open a Pull Request

---

## License

Distributed under the MIT License. See LICENSE file for details.

---

Thank you for checking out the Organic Store project! Feel free to reach out with issues or feature requests.
