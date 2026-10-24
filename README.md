# Ecommerce Clone

A full-stack ecommerce learning project with a React storefront and a Node.js/Express API. The main app supports browsing products, adding and updating cart items, choosing delivery options, reviewing totals, placing orders, and viewing order and delivery tracking pages.

## Repository contents

- `ecommerce-project/` — main React + Vite frontend (JavaScript).
- `ecommerce-backend/` — Express API, product images and data, and database setup.
- `ecommerce-project-ts/` — separate React + Vite + TypeScript starter project.
- `react.basics/` — small React learning examples.

Follow the setup below for the main ecommerce app. The TypeScript starter is separate and is not required to run it.

## Download and run the project

Install [Node.js](https://nodejs.org/) (which includes npm). In a terminal, go to your home folder and clone the repository. Let `git clone` finish before entering the project directory; do not press `Ctrl+C` while it is downloading.

```bash
cd ~
git clone https://github.com/Lalganguly/Ecommerce-clone.git Ecommerce-clone-setup
```

The commands below assume the cloned folder is `~/Ecommerce-clone-setup`. Open **two terminal windows** and keep both running while using the app.

### Terminal 1: start the backend

```bash
cd ~/Ecommerce-clone-setup/ecommerce-backend
npm install
npm run dev
```

The API listens on `http://localhost:3000` by default. Leave this terminal running.

### Terminal 2: start the frontend

```bash
cd ~/Ecommerce-clone-setup/ecommerce-project
npm install
npm run dev
```

Open the local URL printed by Vite in your browser (usually [http://localhost:5173](http://localhost:5173)). The Vite development server forwards `/api` and `/images` requests to the backend on port 3000.

If you cloned the repository into a folder with a different name or location, replace `~/Ecommerce-clone-setup` in the commands with the path you chose. Run each `cd` command from any directory; it uses the full path to the project, so you do not need to navigate from your home folder manually.

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
- If `cd ~/Ecommerce-clone-setup/ecommerce-project` says the directory does not exist, first make sure `git clone` completed successfully and that the folder is named `Ecommerce-clone-setup`.
- If you interrupted cloning, remove or rename the incomplete `Ecommerce-clone-setup` folder before cloning again. Only remove it if it contains no work you need to keep.
- If port 3000 is already in use, stop the other process or configure a different backend port and update the Vite proxy in `ecommerce-project/vite.config.js` to match.
- For backend setup details, see [`ecommerce-backend/README.md`](ecommerce-backend/README.md) and [`ecommerce-backend/troubleshooting.md`](ecommerce-backend/troubleshooting.md).

## Disclaimer

This is a learning project and is not affiliated with Amazon. It does not process real payments or provide production account security.
