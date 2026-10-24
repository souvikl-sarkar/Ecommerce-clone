# Ecommerce Clone

A full-stack ecommerce learning project with a React storefront and a Node.js/Express API. The main app supports browsing products, adding and updating cart items, choosing delivery options, reviewing totals, placing orders, and viewing order and delivery tracking pages.

## Repository contents

- `ecommerce-project/` — main React + Vite frontend (JavaScript).
- `ecommerce-backend/` — Express API, product images and data, and database setup.
- `ecommerce-project-ts/` — separate React + Vite + TypeScript starter project.
- `react.basics/` — small React learning examples.

Follow the setup below for the main ecommerce app. The TypeScript starter is separate and is not required to run it.

## Run this project on your computer

These steps are for a first-time setup on a computer that does not already have this project. Install Node.js 22 or newer first; npm is included with Node.js. Keep the backend and frontend running in separate terminal windows.

### 1. Download the project

Open Terminal and enter these commands. Wait until `git clone` finishes before continuing:

```bash
cd ~
git clone https://github.com/Lalganguly/Ecommerce-clone.git Ecommerce-clone-setup
```

This creates the project folder `Ecommerce-clone-setup` inside your home folder. If Git says the destination folder already exists, the project may already be downloaded; use that existing folder instead of cloning again. If you want a fresh copy, choose a different destination name in the clone command.

### 2. Start the backend (Terminal 1)

In the same terminal, run:

```bash
cd ~/Ecommerce-clone-setup/ecommerce-backend
npm install
npm run dev
```

Wait for the message that the server is running on port 3000. Leave this terminal open while you use the app.

### 3. Start the frontend (Terminal 2)

Open a second terminal window and run:

```bash
cd ~/Ecommerce-clone-setup/ecommerce-project
npm install
npm run dev
```

Wait for Vite to print a local address, then open it in a browser. The default is [http://localhost:5173](http://localhost:5173). Keep both terminal windows running. The frontend sends API and image requests to the backend at `http://localhost:3000`.

If you chose a different clone folder name, replace `Ecommerce-clone-setup` in the `cd` commands with that folder name. Copy only the shell commands inside each code block into Terminal; do not type the Markdown code fence labels such as ```bash.

### Get updates after cloning

To update an existing copy later, run this from a terminal:

```bash
cd ~/Ecommerce-clone-setup
git pull
```

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

- If Git reports that the clone destination already exists, use the existing project folder or choose a different destination name; do not run the same clone command into a non-empty folder.
- If a `cd` command says the directory does not exist, check that cloning completed and that the folder name matches the one used in the clone command.
- If the storefront cannot load products or cart data, make sure the backend terminal is still running on port 3000.
- If port 3000 is already in use, stop the other process or configure a different backend port and update the Vite proxy in `ecommerce-project/vite.config.js` to match.
- For backend details, see [`ecommerce-backend/README.md`](ecommerce-backend/README.md) and [`ecommerce-backend/troubleshooting.md`](ecommerce-backend/troubleshooting.md).

## Disclaimer

This is a learning project and is not affiliated with Amazon. It does not process real payments or provide production account security.
