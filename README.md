

# CS5500-Mall (E-Commerce Platform)

![Build Passing](https://img.shields.io/badge/build-passing-green.svg) ![v2.0.0](https://img.shields.io/badge/version-2.0.0-yellow.svg) [![License: GPL 3.0](https://img.shields.io/badge/license-GPL3.0-blue.svg)](https://chatgpt.com/g/g-p-679f4190c9c88191ba9cc271f04d04cf-5500-assignment1/c/LICENSE)

A full-featured e-commerce system combining server-rendered pages and a modern SPA frontend, with support for coupons, flash-sales, and third-party payments.

------

## Features

- **Homepage & Navigation**: Carousels, category menus, “new arrivals,” featured products.
- **Product Browsing**: Search, filters, detailed views.
- **User Accounts**: Registration, login/logout, profile management.
- **Shopping Cart**: Add/remove items, view totals, apply coupons.
- **Checkout & Orders**: Create orders, calculate shipping/taxes, view order history.
- **Coupon System**: Registration rewards, category-specific, product-specific.
- **Flash-Sale (“Seckill”)**: High-speed ordering with countdown timers.
- **Payments**: Integrated Zelle, bank payment (extendable to other gateways).
- **Vendor Portal**: Inventory management, product catalog updates, sales reports.
- **Admin Console**: User management, banners, categories, system settings.

------

## Technical Stack

- **Backend**: Java 17, Spring Boot 3, MyBatis, RabbitMQ, Redis
- **Database**: MySQL 8
- **Frontend**: Thymeleaf, Vue 3, Element-Plus, Vant
- **DevOps**: Maven 3.5+, JDK 17+, Docker (optional)
- **Testing**: JMeter (load tests), JUnit (unit tests)

------

## Getting Started

### Prerequisites

- **Java 17+**, **Maven 3.5+**
- **MySQL 8+**, **Redis 3+**
- (Optional) Docker for quick setup

### Installation

1. **Clone the repo**

   ```bash
   git clone https://github.com/DucianX/5500FP.git
   cd mallplus
   ```

2. **Import database schema**

   ```bash
   CREATE DATABASE mallplus_db;
   mysql -u root -p mallplus_db < sql/mallplus_schema.sql
   mysql -u root -p mallplus_db < sql/seckill_procedure.sql
   ```

3. **Configure application**

   - Copy `src/main/resources/application-dev.yml.example` → `application-dev.yml`
   - Update MySQL & Redis connection details.

4. **Unzip assets**

   ```bash
   unzip upload.zip -d /path/to/upload
   ```

5. **Build & Run**

   ```bash
   mvn clean package
   mvn spring-boot:run -Dspring-boot.run.profiles=dev
   ```

6. **Access**

   - Frontend: `http://localhost:8080/index.html`
   - Admin: `http://localhost:8080/admin/login.html`

------

## License

This project is licensed under the [GPL 3.0](https://chatgpt.com/g/g-p-679f4190c9c88191ba9cc271f04d04cf-5500-assignment1/c/LICENSE) license.