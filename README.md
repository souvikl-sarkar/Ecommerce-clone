# Ecommerce Clone

A full-stack ecommerce learning project with a React storefront and a Node.js/Express API. The main app supports browsing products, adding and updating cart items, choosing delivery options, reviewing totals, placing orders, and viewing order and delivery tracking pages.

## Repository contents

- `ecommerce-project/` — main React + Vite frontend (JavaScript).
- `ecommerce-backend/` — Express API, product images and data, and database setup.
- `ecommerce-project-ts/` — separate React + Vite + TypeScript starter project.
- `react.basics/` — small React learning examples.

Follow the setup below for the main ecommerce app. The TypeScript starter is separate and is not required to run it.

## Download the project

Install [Node.js](https://nodejs.org/) (which includes npm), then clone this repository and enter its folder:

```bash
git clone https://github.com/Lalganguly/Ecommerce-clone.git
cd Ecommerce-clone
```

Then follow **Run the app locally** below. It installs the frontend and backend dependencies and starts both parts of the app.

## Requirements

- Node.js and npm installed.
- Two terminal windows: one for the backend and one for the frontend.

## Run the app locally

### 1. Start the backend

In the first terminal, from the repository root:

```bash
cd ecommerce-backend
npm install
npm run dev
```

The API listens on `http://localhost:3000` by default.

### 2. Start the frontend

In a second terminal, from the repository root:

```bash
cd ecommerce-project
npm install
npm run dev
```

Open the local URL printed by Vite in your browser (usually [http://localhost:5173](http://localhost:5173)). Keep both terminals running while using the app. The Vite development server forwards `/api` and `/images` requests to the backend on port 3000.

## Main features

- Product catalog with search and product details.
- Add products to the cart, change quantities, and remove items.
- Select delivery options and calculate shipping, tax, and order totals.
- Place orders, view order history, and track deliveries.
- Backend API routes for products, delivery options, cart items, orders, payment summary, and resetting demo data.

## Useful commands

Run these from `ecommerce-project/`:

```bash
npm run dev       # Start the frontend development server
npm run build     # Create a production build
npm run preview   # Preview the production build locally
npm run lint      # Run ESLint
```

Run these from `ecommerce-backend/`:

```bash
npm run dev       # Start the backend with nodemon
npm start         # Start the backend with Node.js
```

The frontend includes a Vitest configuration and some component tests. The backend package currently has no configured test suite.

## Troubleshooting

- If the storefront cannot load products or cart data, check that the backend is running on port 3000.
- If port 3000 is already in use, stop the other process or configure a different backend port and update the Vite proxy in `ecommerce-project/vite.config.js` to match.
- For backend setup details, see [`ecommerce-backend/README.md`](ecommerce-backend/README.md) and [`ecommerce-backend/troubleshooting.md`](ecommerce-backend/troubleshooting.md).

## Disclaimer

This is a learning project and is not affiliated with Amazon. It does not process real payments or provide production account security.
