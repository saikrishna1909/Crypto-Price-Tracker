# 📈 CryptoDash – Real-Time Asset Tracker

CryptoDash is a responsive React application that simulates real-time tracking of 5 cryptocurrencies using Redux Toolkit. It features live updates, Redux state management, and a responsive table layout. This project demonstrates frontend state management using Redux Toolkit, dynamic UI updates, and architectural planning in React.

---

📚 **Table of Contents**

- [⚙️ Tech Stack](#️-tech-stack)  
- [🚀 Features](#-features)  
- [💻 Installation and Setup](#-installation-and-setup)  
- [🗂️ Project Structure](#️-project-structure)  
- [🔁 App Flow](#-app-flow)  
- [🎨 Styling](#-styling)  
- [🌐 Deployment](#-deployment)  
- [📜 License](#-license)  
- [🤝 Contributing](#-contributing)  
- [📬 Contact](#-contact)

---

## ⚙️ Tech Stack

- **React.js** – Frontend framework  
- **Redux Toolkit** – State management (with `createSlice`, `configureStore`)  
- **Axios** – HTTP client (for future API integration)  
- **CSS** – Styling and responsiveness  
- **Mock Data** – Used instead of live crypto API  
- **React-Redux** – Redux bindings for React components  

---

## 🚀 Features

### ✅ Level 1: Asset Table Display  
- Displays 5 predefined crypto assets (e.g., BTC, ETH, USDT, BNB, ADA) in a table format.
- Columns include:
  - Logo, Name, Symbol, Price, % Changes (1h, 24h, 7d), Market Cap, 24h Volume, Circulating & Max Supply, 7D Chart (SVG/Image).
- Uses mock data for initial render.

### ✅ Level 2: Color-Coded % Changes  
- % change columns are dynamically colored:
  - **Green** for positive values
  - **Red** for negative values
- Helps users quickly identify trends.

### ✅ Level 3: Simulated Real-Time Updates  
- Simulates WebSocket behavior using `setInterval`.
- Every 1–2 seconds:
  - Randomly changes `price`, `% changes`, and `24h volume`.
- Dispatches Redux actions to update the global store.
- No local state used in components for data.

### ✅ Level 4: Redux State Management  
- Asset data is stored in the Redux store via a `cryptoSlice`.
- Components use `useSelector` to access data and re-render only on relevant changes.
- `useDispatch` is used to trigger updates to the state.

---

## 💻 Installation and Setup

```bash
git clone https://github.com/your-username/crypto-dash.git
cd crypto-dash
npm install
npm start
🗂️ Project Structure
pgsql
Copy
Edit
crypto-dash/
├── public/
│   └── index.html
├── src/
│   ├── App.js
│   ├── index.js
│   ├── assets/
│   │   └── coin-icons/
│   ├── components/
│   │   ├── AssetTable.js
│   │   ├── AssetRow.js
│   │   └── Chart.js
│   ├── redux/
│   │   ├── cryptoSlice.js
│   │   └── store.js
│   ├── utils/
│   │   ├── mockData.js
│   │   └── simulateUpdates.js
│   └── styles/
│       └── components.css
├── package.json
└── README.md
```

## 🔁 App Flow
## 1. Load & Display
App loads mock crypto data from mockData.js into Redux store on app mount.

Table is rendered using this Redux data via selectors.

## 2. Real-Time Simulation
simulateUpdates.js contains a function using setInterval that:

Randomly updates the price, % changes, and volume of each asset.

Dispatches Redux actions to update the global state.

## 3. Render Updates
React components automatically re-render on Redux state changes, reflecting real-time values.

### 🎨 Styling
Responsive design using regular CSS (no Tailwind or Bootstrap).

Table layout adapts to mobile and desktop screens.

Positive/negative % change coloring for user clarity.

Includes static 7D SVG charts (placeholders) per asset.

### 🌐 Deployment
You can deploy this app using any static site hosting platform:

Netlify

Vercel

GitHub Pages

✅ Netlify Deployment Steps:
Push your code to GitHub

Login to Netlify

Click "New Site from Git"

Connect your GitHub repo

Set Build Command: npm run build

Set Publish Directory: build/

Deploy your site 🎉

### 📜 License
This project is licensed under the MIT License.
Feel free to use, modify, and distribute.

### 🤝 Contributing
Contributions are welcome!

Fork the repository

Create a new feature branch

Make your changes

Test thoroughly

Submit a pull request

### 📬 Contact
📧 Email: kondasaikrishna13@gmail.com

💻 GitHub: saikrishna1909
