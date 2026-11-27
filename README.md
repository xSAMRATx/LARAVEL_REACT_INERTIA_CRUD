# Laravel + React + Inertia CRUD

A product management CRUD app built with **Laravel 12**, **React 19**, **Inertia.js 2** and **TypeScript**, styled with **Tailwind CSS 4** and **shadcn/ui** components.

## Features

- **Authentication** (login, register, email verification, password reset)
- **Products CRUD**, only for logged-in users:
  - list all products
  - create a product (name, price, description)
  - edit and update a product
  - delete a product
- Server-side validation (name required, price numeric) with success flash messages
- **Settings** pages for profile, password and appearance (light / dark mode)
- Single-page app feel with Inertia: no separate API needed

## Tech stack

- PHP 8.2+, Laravel 12, Inertia.js (Laravel adapter), Ziggy for named routes in JavaScript
- React 19, TypeScript, Vite
- Tailwind CSS 4, shadcn/ui (Radix UI), lucide-react icons
- SQLite by default

## Getting started

Requirements: PHP 8.2+, Composer, Node.js 20+ and npm.

```bash
git clone https://github.com/xSAMRATx/LARAVEL_REACT_INERTIA_CRUD.git
cd LARAVEL_REACT_INERTIA_CRUD

composer install
npm install

cp .env.example .env
php artisan key:generate
php artisan migrate

php artisan serve   # terminal 1
npm run dev         # terminal 2
```

Open http://localhost:8000, register an account, then go to **/products**.

## Project structure

- `app/Http/Controllers/ProductController.php` — index, create, store, edit, update, destroy
- `app/Models/Product.php` — product model
- `resources/js/pages/Products` — `Index.tsx`, `Create.tsx`, `Edit.tsx`
- `routes/web.php` — product routes behind the `auth` and `verified` middleware

## Author

**Md. Abdul Aziz Samrat** — [GitHub](https://github.com/xSAMRATx) · [LinkedIn](https://www.linkedin.com/in/md-abdul-aziz-samrat-797738206/)
