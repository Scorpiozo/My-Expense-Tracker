# My-Expense-Tracker
# 🏦 Earthy Pro | Total Vault v4
**A high-performance, private expense intelligence dashboard.**

Total Vault is a luxury-themed financial tracking application built with Vue.js and Tailwind CSS. It allows users to manage their burn rate and financial health using a "Bring Your Own Database" (BYOD) model via the Stein API and Google Sheets.

![Status](https://img.shields.io/badge/Status-Live-2df5b1?style=for-the-badge)
![Security](https://img.shields.io/badge/Security-Client--Side-d4a373?style=for-the-badge)

## ✨ Key Features
* **Intelligence Overhaul:** Real-time financial health scoring and category heatmaps.
* **Vault Lock:** Zero hard-coded API keys. Your data connection is stored securely in your browser's local storage.
* **Automated Analytics:** Doughnut charts for category distribution and merchant frequency tracking.
* **Mobile-First Design:** A sleek, glass-morphism interface designed for quick entries on the go.

## 🚀 Deployment Guide

### 1. Prepare your Database
1.  Create a **Google Sheet** with the following headers in the first row:
    `Date`, `Description`, `Amount`, `Category`
2.  Go to [SteinHQ.com](https://steinhq.com/) and create a new API using your Google Sheet URL.
3.  Copy your **Stein API Endpoint URL** and add '/sheetname'.

### 2. Connect the App
1.  Open the [Live Demo of the site](https://scorpiozo.github.io/My-Expense-Tracker/).
2.  When the **Vault Lock** screen appears, paste your Stein API URL.
3.  The app will securely save this link in your browser and sync your data.

## 🛠️ Built With
* **Vue.js 3** - Reactive UI Framework
* **Tailwind CSS** - Modern styling and layout
* **Chart.js** - Financial data visualization
* **Stein API** - Google Sheets as a REST API

## 🔒 Security & Privacy
* **Zero Backend:** This app has no server. Your data flows directly from your browser to your Google Sheet.
* **Local Secret Storage:** Your API key is never pushed to GitHub. It stays on your device using `localStorage`.
* **Multi-User:** Because no API key is hard-coded, anyone can fork this repo and use it with their own Stein URL.

## 🛠️ Technical Architecture

This project leverages a modern **Serverless Stack** designed for speed and privacy:

* **Logic:** [Vue.js 3](https://vuejs.org/) (Options API) for reactive state management.
* **Design:** [Tailwind CSS](https://tailwindcss.com/) for the custom glass-morphism UI.
* **Data Visualization:** [Chart.js](https://www.chartjs.org/) for real-time expenditure analytics.
* **Backend-as-a-Service:** [Stein](https://steinhq.com/) to interface with Google Sheets.
* **Storage:** Google Sheets (acting as a NoSQL-style database).
---
*Created by a well wisher*
