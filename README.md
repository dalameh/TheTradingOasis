
<p align="center">
  <img width="205" height="205" alt="Oasis" src="https://github.com/user-attachments/assets/789d6b79-fb0e-4996-83ab-7558d274f1c7" />
</p>

# The Trading Oasis 🌊📈 (MVP)


Welcome to **The Trading Oasis**, a comprehensive trading and portfolio management app for investors and traders to explore market insights, track holdings, and log trades — all in one polished, interactive platform.  

While optimized for laptop/desktop, the app is fully **responsive and compatible with tablets and smartphones**, providing a seamless experience across devices.  

This project was built from scratch on a **$0 budget**, so you may notice a slight cold start or slow processing (as a result of low allocated CPU compute power) from frontend and backend deployed APIs, but everything is ready to explore and enjoy. Don’t be shy — click around, try the features, and see what the app can do!  

---

## Overview

The Trading Oasis is designed for **active traders and investors**, combining real-time market data, sentiment analysis, and trade journaling.  

Leveraging a **modern full-stack architecture**, the frontend uses **Next.js (React + Node.js), TypeScript, and Tailwind CSS** for a responsive, dynamic interface, while the backend employs **FastAPI (Python) with Supabase (PostgreSQL)** for reliable and scalable data management.  

This project serves as both a **working demo** and a **template** for developers interested in building full-stack financial apps.

<p align="center">
  <img src="https://github.com/user-attachments/assets/2e16a550-8bd0-4ed9-bef3-a5c3be76ac9b" width="47%" />
  <img src="https://github.com/user-attachments/assets/fde24d92-5d28-4bbb-83fa-08edd8693a61" width="45%" />
</p>

---

## Features

### 1. **Admin Dashboard**
- Manage and monitor all aspects of the app  
- Quick overview of user activity, trades, and portfolios  
- Central hub for key analytics

<img width="1919" height="820" alt="image" src="https://github.com/user-attachments/assets/9e1daf9a-ddfe-4844-8911-0b2e970805d8" />

### 2. **Market Charts**
- Interactive TradingView Lightweight Charts  
- Visualize price trends 
- Supports candlestick and area chart views

<img width="1919" height="820" alt="image" src="https://github.com/user-attachments/assets/b3632739-54eb-46d4-9211-9c3e567a2d88" />

### 3. **News & Headlines**
- View real-time market headlines and updates  
- Quickly assess market sentiment
- Headline Sentiment RESTful API built with **FastAPI**  
- Endpoints for Headline Sentiment Analysis (CRUD Operations)

<img width="1919" height="820" alt="image" src="https://github.com/user-attachments/assets/4dbfc0ea-8d0d-45f3-bade-586b38fd51e8" />

### 4. **Watchlist**
- View real-time market data using Websocket 
- Personalized stock list
- Spaklines, % Change, Quick Actions

<img width="1919" height="820" alt="image" src="https://github.com/user-attachments/assets/d9ad7efe-34bd-48f4-be35-5681dea83558" />

### 5. **Trade Diary**
- Record trades with details like quantity, price, and PnL  
- Organize trades by date, symbol, or portfolio  
- Add notes and photos for reference

<img width="1917" height="819" alt="image" src="https://github.com/user-attachments/assets/a5c57bb3-e8eb-4680-8800-04962ff22073" />
&nbsp;
<img width="1919" height="824" alt="image" src="https://github.com/user-attachments/assets/776e7d4c-399c-4b6d-a89f-b09898c8ee83" />

### 6. **Playbook / Setup Checklist**
- Create step-by-step trading guides or personal checklists  
- Helps structure strategies and recurring tasks

<img width="1919" height="820" alt="image" src="https://github.com/user-attachments/assets/7d935d3f-bcd4-438f-b9f0-f17f490c5157" />

### 7. **Technical Scans**
- Extracting, transforming, and loading financial timeseries data
- Utilizing a Hidden Markov Model with a KMeans initialization, providing a probabilistic sequence of market regime shifts
  (bullish, neutral, bearish) within the market of a given company
- Displays simple moving averages, providing an alternative to market trend shift detection (SMA-50 & SMA-200 crossovers)

<img width="1919" height="826" alt="image" src="https://github.com/user-attachments/assets/78d28e05-4d3b-49fb-ad66-aa9310b93754" />

---

## Frontend / Backend Architecture

- **Frontend:** Next.js + TypeScript + Tailwind CSS  
  - Responsive, fast, and interactive UI  
  - Communicates with backend via REST API
  - Deployed on **Vercel**

<img width="1477" height="661" alt="image" src="https://github.com/user-attachments/assets/6b842bab-4348-4015-897b-11cd9bf8653a"/>
&nbsp;
<img width="1605" height="569" alt="image" src="https://github.com/user-attachments/assets/042035c3-466f-4167-922a-ee79ff299487" />
&nbsp;
<img width="1571" height="816" alt="image" src="https://github.com/user-attachments/assets/b9dc131d-dcdc-44be-864d-c93d122d5ead" />
&nbsp;


- **Backend: (RESTful API for Sentiment Analysis)** 
  - Architected and deployed highly performant, asynchronous RESTful APIs using FastAPI paired with Uvicorn/Gunicorn for optimized concurrency and request handling.
  - Streamlined continuous deployment for microservices by leveraging AWS ECR and AWS App Runner (public endpoint) to automate service delivery and minimize operational overhead (Serverless Containers).
  - Engineered robust Docker build workflows with automated image tagging and implemented secure IAM-based repository authentication using the AWS CLI to AWS ECR, ensuring image integrity and auditability.
  - Optimized production service health and resource utilization by configuring API routing, managing sensitive environment variables, and defining concurrency-based autoscaling policies within App Runner.

<img width="814" height="124" alt="Screenshot 2026-04-21 100647" src="https://github.com/user-attachments/assets/65f4d83d-6e60-4b1b-9db3-01140a202cd1" />
&nbsp;

<img width="950" height="139" alt="Screenshot 2026-04-21 095346" src="https://github.com/user-attachments/assets/238ab15a-8b07-4e26-8551-b2e9d353e428" />
&nbsp;
<img width="1089" height="860" alt="image" src="https://github.com/user-attachments/assets/f6589850-73aa-4ddd-aa9e-56a23393a789" />

&nbsp;

[▶ Press to See API Swagger Doc Video](https://github.com/dalameh/TheTradingOasis/releases/download/API/Financial.Sentiment.API.Swagger.Doc.Video.mp4)

&nbsp;
- **Database:** Supabase (PostgreSQL)  
  - Persistent storage for trades, watchlists, setups, tickers and user info & preferences
&nbsp;
<img width="1080" height="670" alt="image" src="https://github.com/user-attachments/assets/5b1ba3e6-d4e3-4945-a7e8-b39135b30e68" />

---

## Want the UI? Go ahead!

### 🚀 Getting Started

### Prerequisites
- Node.js 18+

### Installation
1. **Clone the repo**
```bash
   git clone https://github.com/dalameh/TheTradingOasis.git
   cd TheTradingOasis/frontend
```
2. **Install dependencies**
```bash
   npm install
```
3. **Set up environment variables**

   Create a `.env.local` file:
```bash
   touch .env.local
```

4. **Run the development server**
```bash
   npm run dev
   Note: APIs are deeply ingrained into the framework, so compiling without the APIs will likely not work on your end.
         So please feel free to extract UI code for your own projects (all located in /app and /components)
```

5. Open [http://localhost:3000](http://localhost:3000)

---

Made with ❤️ by **David A.**

