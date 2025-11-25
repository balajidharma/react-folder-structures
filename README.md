# React Folder Structures
This document outlines the React folder structure and explains the purpose of each directory.

## 🗂️Component-Based Structure
A component-based (type-based) folder structure in React organises files based on their type or role within the application, promoting modularity and reusability.

```bash
src/
├── components/           // Reusable, generic components used throughout the application
│   ├── Button/
│   │   ├── Button.jsx
│   │   └── Button.module.css
│   ├── Card/
│   │   ├── Card.jsx
│   │   └── Card.module.css
│   └── ...
├── layout/               // Components specifically for application layout
│   ├── MainLayout/
│   │   ├── MainLayout.jsx
│   │   └── MainLayout.module.css
│   ├── Header/
│   │   ├── Header.jsx
│   │   └── Header.module.css
│   ├── Footer/
│   │   ├── Footer.jsx
│   │   └── Footer.module.css
│   └── ...
├── menu/                 // Components specifically for navigation menus
│   ├── MainMenu/
│   │   ├── MainMenu.jsx
│   │   └── MainMenu.module.css
│   ├── UserMenu/
│   │   ├── UserMenu.jsx
│   │   └── UserMenu.module.css
│   └── ...
├── pages/                // Top-level components representing distinct application pages/views
│   ├── HomePage/
│   │   ├── HomePage.jsx
│   │   └── HomePage.module.css
│   ├── AboutPage/
│   │   ├── AboutPage.jsx
│   │   └── AboutPage.module.css
│   └── ...
├── hooks/                // Custom React hooks
│   ├── useAuth.js
│   └── useDebounce.js
├── utils/                // Utility functions
│   ├── api.js
│   └── helpers.js
├── assets/               // Static assets (images, fonts, etc.)
│   ├── images/
│   └── fonts/
├── App.jsx               // Main application component
├── index.js              // Entry point of the application
└── styles/               // Global styles or theme variables
    ├── global.css
    └── variables.css
```
### 📌 Directory Overview

#### **components/**  
Houses small, independent, and reusable UI components that can be used across different parts of the application (e.g., Button, Card, Input)

#### **layouts/**  
Contains components responsible for the overall structure and arrangement of content on a page. This includes components like MainLayout (which might wrap the entire application content), Header, and Footer.

#### **pages/**  
Represents distinct views or screens of the application. These components often compose other smaller components to form a complete page (e.g., HomePage, ProductPage).

#### **hooks/**  
Stores custom React hooks for encapsulating reusable logic.

#### **App.jsx**  
The root component that defines routing and layout selection.

#### **index.js**  
Entry point of the React application where the React root is created and the app is mounted.

## 🗂️Feature-Based Structure
This approach groups all files related to a specific feature or domain into one self-contained folder. This is the recommended modern approach for medium-to-large applications.
```bash
src/
├── features/
│   ├── Auth/
│   │   ├── components/
│   │   │   ├── LoginForm.jsx
│   │   │   └── RegisterForm.jsx
│   │   ├── hooks/
│   │   │   └── useAuth.js
│   │   └── pages/
│   │       └── LoginPage.jsx
│   ├── Dashboard/
│   │   ├── components/
│   │   │   └── Widget.jsx
│   │   └── pages/
│   │       └── DashboardPage.jsx
│   └── ... (other features)
├── layouts/
│   ├── MainLayout.jsx
│   ├── AdminLayout.jsx
│   └── components/
│       ├── Header.jsx
│       ├── Sidebar.jsx
│       ├── Footer.jsx
│       └── Menu.jsx
├── shared/
│   ├── components/
│   │   ├── Button.jsx
│   │   └── Modal.jsx
│   ├── hooks/
│   │   └── useDebounce.js
│   └── utils/
│       └── helpers.js
├── App.jsx
├── index.js
```

### 📌 Directory Overview

#### **features/**  
Contains isolated feature modules. Each module may include:  
- Components  
- Hooks  
- Pages  
- API logic  
- Context or state management  

#### **layouts/**  
Houses global layout components that define structural UI for different app sections.  
- **MainLayout.jsx** — used for general/public sections  
- **AdminLayout.jsx** — used for admin-only sections  
- **layouts/components/** — structural UI elements shared across layouts (Header, Sidebar, Menu, etc.)

#### **shared/**  
Contains fully reusable, truly generic utilities and UI elements designed to be used anywhere in the app.  

#### **App.jsx**  
The root component that defines routing and layout selection.

#### **index.js**  
Entry point of the React application where the React root is created and the app is mounted.

---
