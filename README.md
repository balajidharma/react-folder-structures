# React Folder Structures
This document outlines the React folder structure and explains the purpose of each directory.

## 🗂️Feature-Based Structure
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
