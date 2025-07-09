# 🍔 Food Delivery App

A modern, responsive food delivery web application built with React.js and Firebase. This application provides a complete food ordering experience with user authentication, shopping cart functionality, and an admin panel for managing food items.

## ✨ Features

### User Features

- 🏠 **Home Page** - Browse featured food items and categories
- 🍕 **Food Menu** - Comprehensive food catalog with categories
- 🔍 **Food Details** - Detailed view of individual food items
- 🛒 **Shopping Cart** - Add, remove, and manage food items
- 💳 **Checkout** - Complete order with customer details
- 👤 **User Authentication** - Register and login functionality
- 📞 **Contact** - Get in touch with the restaurant

### Admin Features

- ⚙️ **Admin Panel** - Add new food items to the catalog
- 📊 **Product Management** - Manage food inventory

### Technical Features

- 📱 **Responsive Design** - Works on all device sizes
- 🔄 **Real-time Updates** - Firebase integration for live data
- 🎨 **Modern UI** - Built with Material-UI and Bootstrap
- 🛡️ **Secure Authentication** - Firebase Auth integration
- 🗄️ **Cloud Storage** - Firebase Firestore and Storage

## 🛠️ Technology Stack

- **Frontend**: React.js 18.3.1
- **State Management**: Redux Toolkit & React Redux
- **Routing**: React Router DOM
- **Styling**:
  - Bootstrap 5.3.3
  - Material-UI (MUI)
  - Reactstrap
  - Custom CSS
- **Backend**: Firebase
  - Firestore (Database)
  - Authentication
  - Cloud Storage
- **UI Components**:
  - React Slick (Image carousels)
  - React Paginate (Pagination)
  - React Toastify (Notifications)
  - Remixicon (Icons)

## 🚀 Getting Started

### Prerequisites

Before running this project, make sure you have:

- **Node.js** (v14 or higher) - [Download here](https://nodejs.org/)
- **npm** (comes with Node.js) or **yarn**
- **Git** (for cloning) - [Download here](https://git-scm.com/)
- **Firebase account** (free) - [Sign up here](https://firebase.google.com/)

### 📋 Step-by-Step Installation

#### Step 1: Clone the Repository

```bash
git clone <repository-url>
cd Food-Delivery
```

#### Step 2: Install Dependencies

```bash
npm install
```

_This installs all required packages from package.json_

#### Step 3: Firebase Configuration

**Option A: Use Existing Configuration (Quick Start)**

- The project already has Firebase configured
- You can run it immediately with the existing setup

**Option B: Set Up Your Own Firebase Project**

1. Go to [Firebase Console](https://console.firebase.google.com/)
2. Click "Create a project" or "Add project"
3. Enter project name and continue
4. Enable Google Analytics (optional)
5. In your project dashboard:
   - Go to **Authentication** → **Get Started** → **Sign-in method** → Enable **Email/Password**
   - Go to **Firestore Database** → **Create database** → Start in **test mode**
   - Go to **Storage** → **Get started** → Start in **test mode**
6. Go to **Project Settings** → **General** → **Your apps** → **Web app** → Copy config
7. Replace the config in `src/firebase.js` with your credentials

#### Step 4: Start the Application

```bash
npm start
```

#### Step 5: Open in Browser

- Automatically opens: `http://localhost:3000`
- If not, manually navigate to: **http://localhost:3000**

### ✅ Verification Steps

After running `npm start`, you should see:

1. Development server starting on port 3000
2. Browser opens automatically
3. Food Delivery app loads with navigation header
4. No error messages in the console

### 🔧 Available Commands

```bash
# Start development server (default port 3000)
npm start
```

### 🚨 Troubleshooting

**Problem: Port 3000 already in use**

```bash
# Option 1: Kill process on port 3000
npx kill-port 3000
npm start

# Option 2: Use different port
PORT=3001 npm start
```

**Problem: Module not found errors**

```bash
# Clear cache and reinstall
npm cache clean --force
rm -rf node_modules package-lock.json
npm install
```

**Problem: Firebase connection issues**

- Check internet connection
- Verify Firebase config in `src/firebase.js`
- Ensure Firebase services are enabled in console

**Problem: Build fails**

```bash
# Check for syntax errors
npm run build

# If issues persist, check browser console for detailed errors
```

### 🎯 What You'll See

Once running successfully:

- **Home Page** (`/home`) - Landing page with food categories
- **Food Menu** (`/food`) - Browse available food items
- **Login/Register** (`/login`, `/register`) - User authentication
- **Shopping Cart** (`/cart`) - Manage orders
- **Admin Panel** (`/admin`) - Add new food items (admin access)
- **Contact** (`/contact`) - Contact information

### 📱 Testing the App

1. Browse food items on the home page
2. Click on a food item to view details
3. Add items to cart using the "Add to Cart" button
4. View cart by clicking the cart icon
5. Register a new account or login
6. Test the checkout process

## 📁 Project Structure

```
Food-Delivery/
├── public/                 # Static files
├── src/
│   ├── assets/            # Images and fake data
│   │   ├── images/        # Product and UI images
│   │   └── Fakedata/      # Sample data and Firebase fetch functions
│   ├── components/        # Reusable UI components
│   │   ├── UI/            # Specific UI components
│   │   │   ├── cart/      # Cart-related components
│   │   │   ├── category/  # Category components
│   │   │   ├── common-section/ # Common sections
│   │   │   ├── product-card/   # Product card component
│   │   │   └── slider/    # Slider components
│   │   ├── Footer.jsx     # Footer component
│   │   ├── header.jsx     # Header component
│   │   └── Helmet/        # Helmet for SEO
│   ├── context/           # React Context for state management
│   ├── pages/             # Page components
│   │   ├── home.jsx       # Home page
│   │   ├── food.jsx       # Food menu page
│   │   ├── food_details.jsx # Food details page
│   │   ├── cart.jsx       # Shopping cart page
│   │   ├── checkout.jsx   # Checkout page
│   │   ├── login.jsx      # Login page
│   │   ├── register.jsx   # Registration page
│   │   ├── contact.jsx    # Contact page
│   │   └── add_item_page.jsx # Admin panel
│   ├── routing/           # Application routing
│   ├── store/             # Redux store configuration
│   │   └── shopping-cart/ # Cart state management
│   ├── styles/            # CSS stylesheets
│   ├── firebase.js        # Firebase configuration
│   ├── formInputs.js      # Form input configurations
│   ├── App.js             # Main application component
│   └── index.js           # Application entry point
└── package.json           # Project dependencies and scripts
```

## 🌟 Quick Start Summary

**For experienced developers:**

```bash
git clone <repository-url>
cd Food-Delivery
npm install
npm start
# Open http://localhost:3000
```

## 🔥 Firebase Configuration

The app uses Firebase for:

- **Authentication**: User login and registration
- **Firestore**: Storing food items, user data, and orders
- **Storage**: Uploading and storing food images

### Firestore Collections

- `products` - Food items with details like name, price, image, category
- `users` - User profiles and authentication data
- `orders` - Order history and details

## 🎨 Key Components

### Pages

- **Home**: Landing page with featured items and categories
- **Food Menu**: Browse all available food items with filtering
- **Food Details**: Detailed view of selected food item
- **Cart**: Shopping cart with quantity management
- **Checkout**: Order completion with customer information
- **Authentication**: Login and registration forms
- **Admin Panel**: Add new food items (admin only)

### UI Components

- **Header**: Navigation with cart icon and user menu
- **ProductCard**: Reusable card for displaying food items
- **Cart**: Sliding cart panel with item management
- **Category**: Food category filter component
- **Slider**: Testimonial and image carousels

## 🛒 Shopping Cart Features

- Add items to cart with quantity selection
- Update item quantities
- Remove items from cart
- Persistent cart state using Redux
- Real-time cart total calculation
- Slide-out cart panel

## 👥 User Authentication

- Register new accounts
- Login with email and password
- Firebase Authentication integration
- Protected routes for authenticated users
- User session management

## 📱 Responsive Design

The application is fully responsive and optimized for:

- Desktop computers
- Tablets
- Mobile phones
- All screen sizes

## 🔐 Security

- Firebase Authentication for secure user management
- Firestore security rules for data protection
- Input validation and sanitization
- Protected admin routes

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 🔮 Future Enhancements

- Payment gateway integration
- Order tracking system
- Restaurant management dashboard
- Push notifications
- Multi-language support
- Advanced filtering and search
- User reviews and ratings
- Delivery tracking

---

Built with ❤️ using React and Firebase
