# Inventory Master

Inventory Master is a lightweight inventory tracking and ordering application that uses QR codes to streamline restocking. Built with Node.js, MongoDB, and Vercel serverless functions, it ships with a responsive HTML/Bootstrap interface for desktop and mobile devices.

## Features

- **QR code catalog** – Create QR codes with product details and vendor assignments, then search, delete, or print them for labeling items
- **Order management** – Add orders from QR codes or mobile scans, view active or historical orders, and mark or delete fulfilled items
- **Vendor management** – Register vendors with daily, weekly, every-X-weeks, or monthly email cadences and remove vendors when necessary
- **Automated vendor emails** – A scheduled endpoint aggregates each vendor’s active orders and sends them via Microsoft Graph, then marks orders inactive once notified
- **Mobile ordering** – A phone-friendly page lets staff scan a product’s QR code, review its info, and submit an order on the spot

## Project structure
api: Serverless API routes
lib: Shared utilities (e.g., MongoDB client)
public: Static HTML, JS, and assets
.vercel: Vercel deployment configuration
package.json

## Environment variables

Create a `.env` file with the following settings:

- `MONGODB_URI` – MongoDB connection string
- `AZURE_TENANT_ID`, `AZURE_CLIENT_ID`, `AZURE_CLIENT_SECRET` – Azure credentials for Microsoft Graph API
- `SMTP_USER` – Sender address used for outbound vendor emails

## Getting started

1. Install dependencies
   
2. Start a local dev server (requires the Vercel CLI)
   
3. Visit `http://localhost:3000` to access the UI.

## Deployment

Deploy using the Vercel CLI
