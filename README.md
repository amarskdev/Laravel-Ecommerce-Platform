# 🛒 Laravel E-Commerce Platform
### Full-stack e-commerce · Laravel · MySQL · Stripe · Admin Panel · MVC Architecture

![Laravel](https://img.shields.io/badge/Laravel-PHP-FF2D20?style=flat-square&logo=laravel)
![MySQL](https://img.shields.io/badge/MySQL-Database-4479A1?style=flat-square&logo=mysql)
![Stripe](https://img.shields.io/badge/Stripe-Payments-635BFF?style=flat-square&logo=stripe)
![Bootstrap](https://img.shields.io/badge/Bootstrap-5.x-7952B3?style=flat-square&logo=bootstrap)
![License](https://img.shields.io/badge/License-Portfolio-lightgrey?style=flat-square)

> A production-ready e-commerce platform built in Laravel — covering the full shopping lifecycle from product browsing to Stripe checkout, order management, return workflows, and a complete admin panel with sales analytics.

---

## 🏗️ Architecture

```
┌─────────────────────────────────────────────────────┐
│                  USER LAYER                          │
│  Browse · Cart · Checkout · Orders · Returns         │
└───────────────────┬─────────────────────────────────┘
                    │
┌───────────────────▼─────────────────────────────────┐
│              APPLICATION LAYER (Laravel MVC)         │
│                                                      │
│  User Controllers    │    Admin Controllers           │
│  Auth Guards         │    Admin Guards (separate)     │
│  Middleware Stack    │    CRUD + Soft Delete          │
└───────────────────┬─────────────────────────────────┘
                    │
┌───────────────────▼─────────────────────────────────┐
│              INFRASTRUCTURE LAYER                    │
│  MySQL (orders, products, users, invoices)           │
│  Stripe API (payments, webhooks)                     │
│  Laravel Queue (async processing)                    │
└─────────────────────────────────────────────────────┘
```

---

## ✨ Features

### 👤 Customer Facing
- Email-verified user authentication
- Product browsing by category with detailed product pages
- Cart management — add, update, remove items
- Secure checkout with **Stripe payment gateway**
- Order history, invoice generation, and return requests
- User profile management

### 🛠️ Admin Panel
- Separate admin authentication system with custom Laravel guards
- Category and product CRUD with soft delete + trash restore
- Order and return request management
- Customer and billing detail management
- Sales reports and analytics dashboard
- Middleware-protected admin routes (`/admin` prefix)

### 💳 Payments & Orders
- Stripe payment gateway — secure card processing
- Idempotent order processing — no duplicate charges
- Invoice generation per order
- Return workflow with admin approval

---

## 🧩 Tech Stack

| Layer | Technology |
|-------|-----------|
| Backend | Laravel (PHP) · MVC Architecture |
| Database | MySQL — relational schema, foreign keys |
| Frontend | HTML5 · Bootstrap · JavaScript |
| Auth | Laravel Auth — separate User + Admin guards |
| Payments | Stripe API |
| Routing | RESTful · middleware-protected admin routes |

---

## 📁 Project Structure

```
app/
├── Http/
│   ├── Controllers/
│   │   ├── Admin/        # Product, Order, Category, Customer management
│   │   ├── User/         # Cart, Checkout, Orders, Profile
│   │   └── Auth/         # User + Admin authentication
│   └── Middleware/       # Admin guard, auth checks
├── Models/               # User, Product, Order, Invoice, Category
routes/
├── web.php               # User + Admin route definitions
resources/
└── views/                # Blade templates — user + admin panels
```

---

## 🚀 Getting Started

```bash
# Clone the repository
git clone https://github.com/amarkumar55/Laravel-Ecommerce-Platform.git
cd Laravel-Ecommerce-Platform

# Install PHP dependencies
composer install

# Install frontend dependencies
npm install && npm run dev

# Configure environment
cp .env.example .env
php artisan key:generate
```

Update `.env` with your credentials:

```env
# Database
DB_DATABASE=your_db_name
DB_USERNAME=your_db_user
DB_PASSWORD=your_db_password

# Stripe
STRIPE_KEY=your_publishable_key
STRIPE_SECRET=your_secret_key
```

```bash
# Run migrations
php artisan migrate

# Start the server
php artisan serve
# Open http://localhost:8000
```

### Admin Access
Admin routes are prefixed at `/admin` — protected by a dedicated middleware guard. Register via `/admin/register` on first setup.

---

## 🔭 Roadmap

- [ ] Coupon and discount system
- [ ] REST API layer for mobile client support
- [ ] Advanced analytics dashboard with charts
- [ ] Docker + AWS deployment with CI/CD pipeline
- [ ] Elasticsearch for product search

---

## 👤 Author

**Amar Kumar** — Senior Backend Engineer · IBM Certified AI Engineer  
📌 [LinkedIn](https://www.linkedin.com/in/amarkumar241429017) · 💻 [GitHub](https://github.com/amarkumar55)

---

*Full e-commerce lifecycle in Laravel — from product catalog to Stripe checkout to admin analytics.*
