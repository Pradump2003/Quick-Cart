# 🛍️ ECommerce App

A full-featured e-commerce web application with both **Admin** and **User** views, built using **React**, **Redux Toolkit**, **Tailwind CSS**, **Express.js**, and **MongoDB**. It provides seamless shopping, product management, and secure authentication features.

## 🔥 Live Demo
# Quick-Cart

An e‑commerce web application (React + Vite frontend, Node + Express backend, MongoDB) with user and admin functionality: product browsing, cart & checkout, orders, reviews, and admin product/order management.

## 📋 Project Overview

Quick-Cart provides:
- Secure user accounts and authentication (JWT)
- Product listing, categories, and search
- Cart, checkout, and order management
- Product reviews and ratings
- Admin dashboard for product and order management

## 🌐 Live Demo
https://quick-cart-yvg6.vercel.app

## 🛠️ Tech Stack

### Frontend
- React 18, Vite, Tailwind CSS
- Redux Toolkit for state management
- Axios for API calls

### Backend
- Node.js, Express.js
- MongoDB with Mongoose
- JWT for authentication, bcrypt for password hashing
- Cloudinary for media uploads, PayPal SDK for payments

## 📁 Project Structure (high level)

```
Ecommerce-main/
├── client/                     # Frontend (Vite + React)
│   ├── package.json            # frontend scripts & deps
│   ├── vite.config.js
│   ├── tailwind.config.cjs
│   ├── postcss.config.js
│   ├── public/                 # static assets served by Vite
│   └── src/                    # application source
│       ├── main.jsx            # app entry
│       ├── App.jsx             # root component
│       ├── index.css / App.css
│       ├── assets/             # images & static assets
│       ├── components/         # UI & feature components
│       │   ├── admin-view/     # admin-specific UI (header, sidebar, orders...)
│       │   ├── auth/           # auth layouts and pages
│       │   ├── common/         # shared components (forms, auth checks, ratings)
│       │   ├── shopping-view/  # store/customer-facing components
│       │   └── ui/             # small generic UI primitives (button, input, card...)
│       ├── pages/              # top-level route pages
│       ├── routes/             # client routing & axios instance
│       ├── store/              # Redux store and slices
│       ├── config/             # client configuration (e.g. api endpoints)
│       ├── lib/                # small helpers (utils.js)
│       └── utilities/          # misc utilities
├── server/                     # Backend (Express + Node)
│   ├── package.json            # backend scripts & deps
│   ├── server.js               # entrypoint (express app)
│   ├── controllers/            # request handlers grouped by feature
│   │   ├── admin/              # admin controllers (products, orders)
│   │   ├── auth/               # auth controller (login/signup)
│   │   ├── common/             # common/feature controllers
│   │   └── shop/               # shop controllers (products, cart, orders, reviews, search)
│   ├── routes/                 # express route definitions mirroring controllers
│   │   ├── admin/
│   │   ├── auth/
│   │   └── shop/
│   ├── models/                 # Mongoose models (User, Product, Order, Cart, Review, Address, Feature)
│   ├── helpers/                # third-party integrations (cloudinary, paypal)
│   └── middlewares/            # express middlewares (auth, error handlers)
└── README.md
```

Descriptions:
- `client/src/components/` — Organised UI components; examples: `product-tile.jsx`, `header.jsx`, `orders.jsx`, `product-details.jsx`.
- `client/src/store/` — Redux store and feature slices used by the app (auth, shop, admin slices).
- `server/controllers/` — Business logic for each route (e.g., `products-controller.js`, `order-controller.js`).
- `server/models/` — Mongoose schemas: `User.js`, `Product.js`, `Order.js`, `Cart.js`, `Review.js`, `Address.js`, `Feature.js`.
- `server/helpers/` — Integrations such as `cloudinary.js` and `paypal.js` used for media and payments.
- `server/routes/` — Route definitions wired to controllers (example: `server/routes/shop/products-routes.js`).

Tip: open `client/src/components/` and `server/controllers/` in your editor to see the exact component and controller file names referenced above.

## ✨ Key Features

### Authentication
- User registration and login (JWT)
- Password hashing with bcrypt
- Protected routes for authenticated users and admin

### Shopping & Orders
- Product browsing, filtering, and details
- Add to cart and checkout flow
- Order creation and order history

### Admin
- Create/update/delete products
- Manage orders

### UX
- Responsive UI with Tailwind CSS
- Toast notifications for feedback

## 🚀 Installation & Setup

### Prerequisites
- Node.js v16+ recommended
- npm or yarn
- MongoDB (local or Atlas)

### Backend

1. Install dependencies

```bash
cd server
npm install
```

2. Create a `.env` file in `server/` with required keys (example below)

3. Run server (development)

```bash
npm run dev
```

Default backend port: `http://localhost:9000`

### Frontend

1. Install dependencies

```bash
cd client
npm install
```

2. Run frontend (development)

```bash
npm run dev
```

Default frontend port: `http://localhost:5173`

## 📡 API Examples (select endpoints)

### Auth
- POST `/api/auth/signup` — Register user
- POST `/api/auth/login` — Login user

### Products
- GET `/api/shop/products` — List products
- GET `/api/shop/products/:id` — Product details

### Cart & Orders
- POST `/api/shop/cart` — Add/update cart
- POST `/api/shop/orders` — Create order

Check `server/routes/` for full route definitions.

## 🎯 Available Scripts

### Frontend (client/package.json)
- `dev` — start Vite dev server
- `build` — build production assets
- `preview` — preview production build

### Backend (server/package.json)
- `dev` — start server with nodemon
- `start` — start server with node

## 📝 Environment variables (examples)

Create `server/.env` with:

```
MONGO_URI=<your_mongodb_connection_string>
JWT_SECRET=<your_jwt_secret>
CLOUDINARY_URL=<cloudinary_url_or_credentials>
PAYPAL_CLIENT_ID=<paypal_client_id>
PAYPAL_SECRET=<paypal_secret>
PORT=9000
```

Create `client/.env` (if needed):

```
VITE_API_URL=http://localhost:9000/api
```

## 🐛 Troubleshooting

- Ensure MongoDB is reachable and `MONGO_URI` is correct
- Confirm ports `9000` and `5173` are free
- Check server logs for stack traces when requests fail

## 👤 Contributing

1. Fork the repo
2. Create a feature branch: `git checkout -b feature/awesome`
3. Commit and push
4. Open a pull request

## 📄 License

Add license information here (e.g. MIT).

---

If you want the README to be an almost-exact copy of your Smart Issue Board example (sections, tables, and API docs), I can replace the text verbatim and add the demo/screenshots; tell me which demo link and images to use.


This will start the client on `http://localhost:5173` (default).

## 🤝 Contributing
Fork the repo

Create your feature branch (git checkout -b feature/AmazingFeature)

Commit your changes (git commit -m 'Add some AmazingFeature')

Push to the branch (git push origin feature/AmazingFeature)

Open a pull request
````
