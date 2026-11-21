<div align="center">

# 🛍️ Goodfinds — Next-Gen Omnichannel E-Commerce & Dropshipping Platform

<p align="center">
  <strong>Curated Daily Discoveries & Smart Lifestyle Finds</strong><br>
  A production-ready, full-stack e-commerce ecosystem featuring a Flipkart-grade web storefront, native mobile application, and operations hub.
</p>

[![Next.js](https://img.shields.io/badge/Next.js-16.1.4-black?style=for-the-badge&logo=next.js&logoColor=white)](https://nextjs.org/)
[![React Native](https://img.shields.io/badge/React_Native-0.81.5-61DAFB?style=for-the-badge&logo=react&logoColor=black)](https://reactnative.dev/)
[![Expo](https://img.shields.io/badge/Expo_SDK-54-000020?style=for-the-badge&logo=expo&logoColor=white)](https://expo.dev/)
[![TypeScript](https://img.shields.io/badge/TypeScript-5.0-3178C6?style=for-the-badge&logo=typescript&logoColor=white)](https://www.typescriptlang.org/)
[![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-3.4-38B2AC?style=for-the-badge&logo=tailwind-css&logoColor=white)](https://tailwindcss.com/)
[![Prisma](https://img.shields.io/badge/Prisma-5.22-2D3748?style=for-the-badge&logo=prisma&logoColor=white)](https://www.prisma.io/)
[![PostgreSQL](https://img.shields.io/badge/PostgreSQL-Neon_Serverless-4169E1?style=for-the-badge&logo=postgresql&logoColor=white)](https://neon.tech/)
[![Vercel](https://img.shields.io/badge/Deployed_on-Vercel-000000?style=for-the-badge&logo=vercel&logoColor=white)](https://goodfinds-vert.vercel.app)

<br/>

[🌐 Live Web Demo](https://goodfinds-vert.vercel.app) • [📱 Download Android APK](https://expo.dev/accounts/samah080/projects/goodfinds/builds/86fbc875-abe9-4966-97d7-09d16d63fb2b) • [📖 Dropshipping Master Plan](file:///C:/Users/afsal/.gemini/antigravity/brain/990f89db-690e-487a-8e1e-8f651ab568e9/master_plan.md) • [📊 Admin Dashboard](https://goodfinds-vert.vercel.app/admin)

</div>

---

## 🌟 Highlights & Key Differentiators

- **Dual-Platform Architecture**: Unified business logic between a **Next.js 16 App Router** responsive web app and a high-performance **React Native (Expo SDK 54)** native mobile app.
- **Flipkart-Grade UI/UX**:
  - Horizontal scrollable Category Strip with active URL synchronization.
  - Auto-rotating promotional Hero Carousel with hover-pause and gesture touch.
  - Real-time **Deals of the Day** countdown ticker with dynamic pricing.
  - Multi-faceted filter engine (Price brackets, Rating, Discount tier, Assured toggle, Stock status).
  - Split-screen Product Detail page with dual primary CTAs (**Add to Cart** & **Buy Now**), offers panel, and review sentiment metrics.
  - Interactive **Pincode Delivery Estimator** with localized cache and COD verification.
- **Engineered for Indian Dropshipping**:
  - **Zero-Inventory Cash Flow Engine**: Direct supplier dispatch routing (Roposo Clout, GlowRoad, CJ Dropshipping).
  - **RTO (Return to Origin) Defense**: Automated order verification workflow and instant ₹70 prepaid UPI discount incentives to minimize COD rejection rates.
  - Supplier cost and net margin analytics per SKU right in the Admin Operations Hub.
- **Bespoke Hardware-Grade Design System**:
  - Custom palette built on deep forest green (`#183d2f`), luminous mint (`#baf2cd`), warm paper surfaces (`#f5f6f1`), and crisp contrast typography.

---

## 📱 Mobile App (React Native + Expo SDK 54)

The cross-platform native app brings Flipkart-level responsiveness directly to mobile devices:

| Feature | Description |
| :--- | :--- |
| **Search-First Header** | Instant client-side search query filtering with clear button and sticky navigation. |
| **Category Capsule Strip** | Smooth horizontal category rail with active category detection. |
| **Deals Countdown Ticker** | Live countdown banner generating immediate urgency for time-limited offers. |
| **2-Column Flipkart Grid** | Product cards with discount tags, Goodfinds Assured badges, star ratings, and dual pricing. |
| **Product Detail Modal** | Split visual display, offers collapsible cards, and sticky dual CTA footer. |
| **Sort & Filter Bottom Sheet** | Native bottom drawer with sorting by Relevance, Price, and Discounts. |
| **Ready for Distribution** | Pre-compiled preview APK built via **Expo EAS** with automated build profiles. |

> 📲 **Download Latest Android Build**: [Expo EAS Build Artifact](https://expo.dev/accounts/samah080/projects/goodfinds/builds/86fbc875-abe9-4966-97d7-09d16d63fb2b)

---

## 🖥️ Web Storefront & Admin Operations

### Customer Experience (`/(store)`)
- **Home Page**: Dynamic promotional banners, curated discovery collections, and real-time deal counters.
- **Catalog Engine (`/products`)**: High-density 2-to-4 column responsive grid with toggleable Flipkart-style list view, dynamic category counts, and price range sliders.
- **Product Experience (`/products/[id]`)**: Sticky high-res media display, breadcrumb navigation, interactive pincode verification, and verified customer review breakdown.
- **Cart & Checkout (`/cart`, `/checkout`)**: Real-time subtotal calculation, instant UPI prepaid savings calculations, and door-to-door delivery form validation.

### Operations Hub (`/(admin)`)
- **Metrics Dashboard (`/admin`)**: Real-time revenue tracking, order count metrics, gross margin estimations, and inventory status.
- **Catalog Manager (`/admin/products`)**: Full CRUD operations for products with supplier URL tracking, wholesale cost tracking, and stock monitoring.
- **Order Pipeline (`/admin/orders`)**: Real-time order fulfillment workflow with payment status badges and customer shipping info.

---

## 🏗️ System Architecture

```mermaid
graph TD
    subgraph Clients
        Web[Next.js 16 Web Storefront]
        Mobile[React Native / Expo Mobile App]
        Admin[Operations & Admin Hub]
    end

    subgraph Application Tier [Next.js App Router]
        ServerActions[Server Actions: productActions, orderActions]
        APIRoutes[REST Endpoints: /api/products, /api/orders]
        AuthContext[NextAuth Session State]
        CartProvider[Cart Context & State Management]
    end

    subgraph Data Tier
        Prisma[Prisma ORM 5.22]
        Neon[(Neon Serverless PostgreSQL)]
    end

    subgraph Dropshipping & Logistics
        Payment[Razorpay / Cashfree UPI]
        Suppliers[Roposo Clout / GlowRoad / Baapstore]
        Courier[Shiprocket / Delhivery Courier Network]
    end

    Web --> ServerActions
    Admin --> ServerActions
    Mobile --> APIRoutes
    ServerActions --> Prisma
    APIRoutes --> Prisma
    Prisma --> Neon
    ServerActions --> Payment
    APIRoutes --> Payment
    Admin --> Suppliers
    Suppliers --> Courier
```

---

## 🛠️ Technology Stack

| Layer | Technologies |
| :--- | :--- |
| **Web Frontend** | Next.js 16.1.4 (App Router, Turbopack), React 19, Tailwind CSS 3.4, Lucide Icons |
| **Mobile Frontend** | React Native 0.81.5, Expo SDK 54, React Navigation 7, Expo Vector Icons |
| **Backend & APIs** | Next.js Server Actions, Next.js API Routes, NextAuth.js |
| **Database & ORM** | Neon Serverless PostgreSQL, Prisma ORM 5.22 |
| **Mobile Build System** | Expo Application Services (EAS Build), Android Gradle Plugin |
| **Hosting & CI/CD** | Vercel (Production Web Edge), GitHub Actions, Expo Cloud |

---

## 🗄️ Database Model (Prisma Schema)

```prisma
model User {
  id        String   @id @default(cuid())
  email     String   @unique
  name      String?
  role      Role     @default(USER) // USER, ADMIN
  orders    Order[]
  createdAt DateTime @default(now())
}

model Product {
  id           String      @id @default(cuid())
  name         String
  description  String
  price        Decimal
  costPrice    Decimal?    // Wholesale supplier cost
  supplierName String?     // e.g., Roposo, GlowRoad
  supplierUrl  String?
  image        String
  stock        Int         @default(0)
  categoryId   String
  category     Category    @relation(fields: [categoryId], references: [id])
  orderItems   OrderItem[]
  createdAt    DateTime    @default(now())
}

model Order {
  id          String      @id @default(cuid())
  userId      String?
  total       Decimal
  status      OrderStatus @default(PENDING) // PENDING, PROCESSING, SHIPPED, DELIVERED, CANCELLED
  isPrepaid   Boolean     @default(false)
  items       OrderItem[]
  createdAt   DateTime    @default(now())
}
```

---

## 🚀 Local Development Setup

### Prerequisites
- Node.js 18.x or 20.x
- Git & npm / pnpm
- Expo Go app on your smartphone (for mobile testing)

### 1. Clone the Repository
```bash
git clone https://github.com/samah3303/LuxeMart.git
cd LuxeMart
```

### 2. Web Storefront Setup
```bash
cd web
npm install

# Configure environment variables
# Create .env.local with your database URL
# DATABASE_URL="postgresql://user:password@host/dbname?sslmode=require"

# Sync Prisma Schema & Seed Catalog
npx prisma db push
node prisma/seed.js

# Launch Web Application with Turbopack
npm run dev
```
- Storefront will be live at `http://localhost:3000`
- Admin Operations Hub at `http://localhost:3000/admin`

### 3. Mobile App Setup
```bash
cd ../mobile
npm install

# Start Expo Development Server
npx expo start
```
- Scan the printed terminal QR code using **Expo Go** (Android/iOS) to run the live native app instantly on your device.

---

## 📦 Dropshipping Execution Roadmap

A complete strategic playbook for scaling from zero orders to ₹1,00,000+/month net profit is documented in our [Dropshipping Master Plan](file:///C:/Users/afsal/.gemini/antigravity/brain/990f89db-690e-487a-8e1e-8f651ab568e9/master_plan.md):

1. **Phase 1**: Supplier integration (Roposo Clout, GlowRoad) & 10+ viral winning product catalog curation.
2. **Phase 2**: Payment Gateway (Razorpay/Cashfree) & automated courier integration (Shiprocket).
3. **Phase 3**: Soft launch & first 10 orders validation loop.
4. **Phase 4**: Growth engine via viral product short-form reels & targeted Meta conversion ads.
5. **Phase 5**: RTO defense automation (WhatsApp confirmation bot & UPI instant discount).
6. **Phase 6**: Scaling to 15+ daily orders with ₹1L+ monthly net margins.

---

## 👨‍💻 Author & Contributions

- **Repository**: [samah3303/LuxeMart](https://github.com/samah3303/LuxeMart)
- **Live Deployment**: [goodfinds-vert.vercel.app](https://goodfinds-vert.vercel.app)
- **Built by**: Afsal Samah

---

<div align="center">
  <sub>Engineered with precision for modern Indian e-commerce. Star ⭐ this repository if you find it helpful!</sub>
</div>
