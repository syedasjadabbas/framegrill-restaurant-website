# 🍖 FrameGrill Restaurant Website

<p align="center">
  <img src="https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB" alt="React" />
  <img src="https://img.shields.io/badge/TypeScript-007ACC?style=for-the-badge&logo=typescript&logoColor=white" alt="TypeScript" />
  <img src="https://img.shields.io/badge/Tailwind_CSS-38B2AC?style=for-the-badge&logo=tailwind-css&logoColor=white" alt="Tailwind CSS" />
  <img src="https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=nodedotjs&logoColor=white" alt="Node.js" />
  <img src="https://img.shields.io/badge/Express.js-000000?style=for-the-badge&logo=express&logoColor=white" alt="Express" />
  <img src="https://img.shields.io/badge/MongoDB-47A248?style=for-the-badge&logo=mongodb&logoColor=white" alt="MongoDB" />
  <img src="https://img.shields.io/badge/Gemini_2.5_Flash-8E75C2?style=for-the-badge&logo=google&logoColor=white" alt="Gemini" />
</p>

A premium, full-stack, AI-powered restaurant web application designed for a luxury dining experience. Built with a sleek, responsive design featuring a rich Maroon & Gold aesthetic, interactive animations, and a seamless flow from menu selection to checkout and live customer support.

---

## ✨ Features

### 🤖 AI-Powered Experience
- **Interactive AI Chatbot**: Powered by Google's `gemini-2.5-flash`, providing real-time answers about our menu, special items, location, and hours.
- **Smart Menu Recommendations**: Dynamic AI recommendations tailoring meals directly to customer preferences and dietary requirements.

### 🛒 Modern Ordering Flow
- **Interactive Food Menu**: Browse food categories (Appetizers, Steaks, Burgers, Desserts, Beverages) with gorgeous card layouts and smooth hover effects.
- **Seamless Cart & Checkout**: Easily add items, manage quantities, calculate taxes, dynamic delivery fees, and place orders.
- **WhatsApp Ordering Integration**: Convert digital cart details directly into a formatted WhatsApp order message for immediate fulfillment.

### 🎨 Visual & Technical Excellence
- **Luxury Theme**: Implements a curated dark and light mode color palette with soft cream backgrounds, rich charcoal elements, deep wine primary colors, and gold accents.
- **Responsive Layout**: Pixel-perfect presentation from mobile screens up to wide desktop monitors.
- **Smooth Transitions**: Incorporates *Animate on Scroll (AOS)* and custom micro-interactions for a fluid browsing experience.

---

## 🛠️ Tech Stack

### Frontend
- **Framework**: React 18 (Vite + TypeScript)
- **Styling**: Tailwind CSS
- **Routing**: React Router DOM (v6)
- **Animations**: AOS (Animate on Scroll)
- **State Management**: React Context (Cart & Theme)
- **Icons**: Lucide React
- **Notifications**: Sonner & Radix UI Tooltips

### Backend
- **Runtime**: Node.js & Express.js
- **Database**: MongoDB Atlas (via Mongoose)
- **Authentication**: JWT & BcryptJS (Secure Admin Panel)
- **Deployment-Ready**: Environment configuration via Dotenv, CORS support

---

## 📂 Directory Structure

```bash
├── public/                 # Static assets (logos, pictures)
├── src/                    # Frontend React code
│   ├── assets/             # Images and styles
│   ├── components/         # Reusable UI components (Hero, Footer, AIChat, etc.)
│   ├── context/            # React context providers (Cart, Theme)
│   ├── data/               # Static menu items and fallback details
│   ├── hooks/              # Custom React hooks
│   ├── lib/                # API configurations (Gemini client helper)
│   ├── pages/              # Main routing views (Home, Menu, Cart, Contact, NotFound)
│   ├── App.tsx             # Root page router and setup
│   └── main.tsx            # App entrypoint
├── server/                 # Backend API codebase
│   ├── middleware/         # Auth & admin guard middlewares
│   ├── models/             # Mongoose schemas (Admin, Order, Product)
│   ├── routes/             # REST endpoints (auth, products, orders)
│   ├── seed.js             # Data seeding script for menu items
│   └── index.js            # Server entrypoint and MongoDB connection
```

---

## 🚀 Getting Started

### Prerequisites
- Node.js (v18 or higher)
- NPM or Bun package manager
- MongoDB Atlas account (or local MongoDB database)
- Gemini API key from [Google AI Studio](https://aistudio.google.com/)

### Frontend Installation & Setup

1. From the root directory, install dependencies:
   ```bash
   npm install
   ```

2. Create a `.env.local` file in the root directory and add your Gemini API Key:
   ```env
   VITE_GEMINI_API_KEY=your_gemini_api_key_here
   ```

3. Launch the development server:
   ```bash
   npm run dev
   ```

### Backend Installation & Setup

1. Navigate to the `server/` directory:
   ```bash
   cd server
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

3. Create a `.env` file inside the `server/` folder:
   ```env
   PORT=5000
   MONGODB_URI=mongodb+srv://<username>:<password>@cluster.mongodb.net/framegrill
   JWT_SECRET=your_jwt_secret_token_here
   ```

4. Seed the database with menu items (optional but recommended):
   ```bash
   node seed.js
   ```

5. Start the backend server:
   ```bash
   npm run dev
   ```

---

## 📊 Database Models (Mongoose)

### 🍔 Product Schema
Defines the structure for all culinary items available on the platform:
- `id` (String, Unique): Custom alphanumeric item identifier.
- `name` (String): Display name of the dish.
- `description` (String): Appetizing details.
- `price` (Number): Price in local currency.
- `image` (String): URL or file path of the product image.
- `badge` (String): Special tags like "Best Seller", "New", "Chef's Special".
- `category` (String): Product classification.

### 📝 Order Schema
Saves checkout details to the backend:
- `items`: Array of product items (id, name, price, quantity, image).
- `customerDetails`: Object containing customer name, phone, address, and email.
- `subtotal` & `totalAmount`: Price summaries.
- `status`: Order status state machine (`pending`, `confirmed`, `completed`, `cancelled`).

---

## 📞 WhatsApp Message Formatting
When checking out, FrameGrill generates a professionally structured message:
```text
🍖 *New Order - FrameGrill* 🍖
-----------------------------
👤 *Customer:* John Doe
📞 *Phone:* +92 300 1234567
📍 *Address:* Street 4, F-8, Islamabad

*Order Items:*
- 2x T-Bone Steak Premium ($48.00)
- 1x Chocolate Lava Cake ($8.50)

-----------------------------
*Subtotal:* $56.50
*Delivery Fee:* $2.00
*Total Amount:* $58.50
```

---

## 📝 License
Distributed under the MIT License. See [LICENSE](file:///e:/WEBS%20&%20APPS/framegrill-restaurant/LICENSE) for more information.

---
<p align="center">Made with ❤️ for FrameGrill Restaurant</p>
