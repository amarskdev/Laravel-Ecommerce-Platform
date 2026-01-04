# 🛒 Laravel E-commerce Application

A full-featured e-commerce web application built using **Laravel** and **MySQL**, supporting product browsing, cart management, secure checkout, Stripe payments, and a powerful admin panel.

---

## 🚀 Features

### 👤 User Features
- User authentication with email verification
- Browse products by categories
- View detailed product pages
- Add, update, and remove items from cart
- Secure checkout flow
- Online payments via **Stripe Payment Gateway**
- Order history & invoice generation
- Order return requests
- User profile management

---

### 🛠️ Admin Panel Features
- Separate admin authentication system
- Category & product management (CRUD)
- Soft delete & restore (trash management)
- Order & return request management
- Customer & billing detail management
- Sales reports & analytics
- Admin profile management

---

### 💳 Payment & Orders
- Stripe payment gateway integration
- Secure order processing
- Invoice generation
- Subscription & payment handling
- Order return workflow

---

## 🧩 Tech Stack

- **Backend:** Laravel (PHP)
- **Database:** MySQL
- **Frontend:** HTML5, Bootstrap, JavaScript
- **Authentication:** Laravel Auth (User & Admin Guards)
- **Payments:** Stripe
- **Architecture:** MVC, RESTful routing
- **Version Control:** Git

---

## 🗂️ Project Structure (High Level)

```text
app/
├── Http/
│   ├── Controllers/
│   │   ├── Admin/
│   │   ├── User/
│   │   └── Auth/
├── Models/
routes/
├── web.php
resources/
├── views/
public/
├── assets/
```

---

## 🔐 Authentication & Authorization
- User authentication with email verification
- Separate admin authentication using custom guards
- Middleware-protected admin routes
- Role-based access control

---

## ⚙️ Installation & Setup

###  Clone the repository

```bash
    git clone https://github.com/amarkumar55/laravel-ecommerce.git
    cd laravel-ecommerce
```


### Install dependencies

```bash
    composer install
    npm install
```

###Environment configuration

```bash
    cp .env.example .env
    php artisan key:generate
```

### Update .env with:
    
    Database credentials
    Stripe API keys

### Run migrations
```bash
    php artisan migrate
```

### Start the application
```bash
    php artisan serve
```


🧪 Admin Access

    Admin routes are prefixed with /Admin
    
    Dedicated admin login & registration
    
    Secure admin dashboard with middleware protection
    

📈 Highlights

    Clean and modular Laravel architecture
    
    Secure Stripe payment integration
    
    Scalable admin panel
    
    Real-world e-commerce workflows
    
    Production-ready routing and middleware


📌 Future Enhancements

    Coupon & discount system
    
    API versioning
    
    Advanced analytics dashboard
    
    Dockerized deployment
    
    AWS hosting & CI/CD pipeline


📄 License

This project is intended for learning and portfolio purposes.
Commercial usage requires prior permission.

---

If you want, I can also:
- Make a **short README** for recruiters  
- Add a **screenshots/demo section**
- Create a **1-line GitHub repo description**
- Rewrite this for a **SaaS / senior-level tone**

Just tell me 🚀





