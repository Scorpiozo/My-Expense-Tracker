# Earthy Pro | Total Vault v4

A modern, luxurious expense tracker designed to help you master your monthly budget with intelligent insights and real-time spending analytics.

## 🎯 Features

### **Vault Dashboard**
- Track daily expenses with semantic categorization (Food, Bills, Fun, Other)
- Real-time calculation of safe daily spending allowance
- Visual progress bar showing monthly budget consumption
- Sleek card-based transaction history with category icons

### **Intelligence Analytics**
- **Burn Rate** - Daily average spending velocity
- **Projected Total** - End-of-month spending forecast
- **Vault Health Score** - Efficiency percentage (0-100%)
- **Savings Integrity** - Progress toward monthly savings goal
- **Top Strainer** - Highest spending category at a glance
- **Executive Briefing** - AI-generated spending analysis with contextual recommendations

### **Visual Reports**
- **Category Distribution Chart** - Doughnut visualization of spending by category
- **Daily Spending Velocity** - Line graph tracking daily spend patterns across the entire month
- Advanced filtering by category, date range, and search terms

### **Reminders System**
- Create recurring monthly bill alerts
- Mark bills as paid with visual feedback
- Persistent local storage for all reminders

### **Premium UX**
- Dark luxury theme with mint and gold accents
- Glassmorphism UI components with backdrop blur effects
- Smooth animations and micro-interactions
- Fully responsive mobile-first design
- Bottom navigation with fixed FAB buttons

## 🚀 Getting Started

### **Installation**

No build process required! This is a pure vanilla HTML + Vue.js single-file application.

1. Clone or download the project
2. Open `index.html` in a web browser
3. Choose your login method:
   - **API Mode**: Enter your SteinHQ endpoint URL for cloud data sync
   - **Demo Mode**: Click "View Site Demo" for a read-only preview

### **Authentication**

The app uses **SteinHQ** (steinHQ.com) as the backend database:

```
Required API Endpoint Format:
https://api.steinhq.com/v1/storages/{YOUR_STORAGE_ID}/{SHEET_NAME}
```

**To set up your own vault:**
1. Create a free account at [SteinHQ](https://steinhq.com)
2. Create a storage with a sheet named after your tracking needs
3. Input the API endpoint when prompted on login

Data structure expected:
```json
[
  {
    "Date": "Mar 15, 2025",
    "Description": "Coffee Run",
    "Amount": 5.50,
    "Category": "Food"
  }
]
```

### **Local-Only Mode**

All data (bills, budget limits, savings goals) are stored in **LocalStorage**:
- No account required
- Data persists between sessions
- Works completely offline
- Demo mode provides sample transactions

## ⚙️ Configuration

### **Settings Panel**
Access via the ⚙️ button in the top-right corner:

- **Total Budget Limit** - Your monthly spending ceiling (default: $5,000)
- **Monthly Savings Goal** - Amount to reserve (default: $500)

Formula for safe daily spend:
```
Daily Allowance = (Budget Limit - Savings Goal - Current Month Total) / Days Remaining
```

## 📊 Dashboard Metrics Explained

| Metric | Description |
|--------|------------|
| **Safe Daily Spend** | Maximum daily budget without breaching savings goal |
| **Burn Rate** | Average daily spending (Total Spent ÷ Days Elapsed) |
| **Projected End** | Estimated month-end total based on current burn rate |
| **Vault Health** | Efficiency score (100% = on budget, <0% = over budget) |
| **Savings Integrity** | Progress toward savings goal (100% = goal met) |
| **Top Strainer** | Category with highest spending this month |

## 🎨 Theme & Customization

### **Color Palette**
- **Dark Base**: `#0f0b09`
- **Mint Accent**: `#2df5b1`
- **Gold Accent**: `#d4a373`
- **Text**: `#f2e9e4`

### **Font**
- **Family**: Plus Jakarta Sans (Google Fonts)
- **Weights**: 400, 600, 700, 800 for hierarchy

To customize colors, edit the CSS variables in the `<style>` section.

## 📱 Browser Compatibility

- ✅ Chrome/Chromium (latest)
- ✅ Firefox (latest)
- ✅ Safari (latest)
- ✅ Mobile browsers (iOS Safari, Chrome Android)
- ✅ PWA-capable (can be installed as app)

## 🔐 Privacy & Security

- **No personal data sent** when using LocalStorage-only mode
- **SteinHQ API** is encrypted via HTTPS
- **Client-side processing** - all calculations happen in your browser
- **No tracking or analytics** embedded
- Open source - review the code for transparency

## 📦 Dependencies

```html
<!-- Vue.js 3 (CDN) -->
<script src="https://unpkg.com/vue@3/dist/vue.global.js"></script>

<!-- Tailwind CSS (CDN) -->
<script src="https://cdn.tailwindcss.com"></script>

<!-- Chart.js (CDN) -->
<script src="https://cdn.jsdelivr.net/npm/chart.js"></script>

<!-- Google Fonts -->
<link href="https://fonts.googleapis.com/css2?family=Plus+Jakarta+Sans..." />
```

All dependencies loaded via CDN - no npm installation needed.

## 🎯 Use Cases

- **Personal budgeting** - Track discretionary spending
- **Shared household expenses** - Monitor family burn rate
- **Freelancer cash flow** - Track client payments and expenses
- **Travel budgeting** - Set limits and forecast spending by category
- **Savings tracking** - Visualize progress toward financial goals

## 💡 Tips for Best Results

1. **Set realistic budgets** - Include all monthly expenses (rent, utilities, etc.)
2. **Categorize consistently** - Use the same categories for easier analysis
3. **Check daily** - The app works best with daily expense logging
4. **Review analytics weekly** - Spot trends before month-end
5. **Adjust goals** - Use historical data to refine monthly targets

## 🐛 Troubleshooting

### **API Connection Failed**
- Verify SteinHQ endpoint URL is correct
- Check internet connection
- Ensure CORS is enabled on your SteinHQ storage

### **Data Not Syncing**
- Try refreshing the page
- Clear browser cache (Ctrl+Shift+Del)
- Re-enter your API key in settings

### **Charts Not Displaying**
- Ensure you have expense data in the current month
- Try clicking the "Intel" tab again
- Check browser console for JavaScript errors

## 📄 License

Open source - feel free to fork, modify, and redistribute.

## 🤝 Contributing

Found a bug or have a feature idea? 
- Review the Vue.js logic in the `<script>` section
- Test changes in your browser (F12 Developer Tools)
- Share improvements via pull request

## 📞 Support

For issues with:
- **This app**: Check the code comments and Intelligence Lexicon (? button)
- **SteinHQ integration**: Visit [SteinHQ Docs](https://steinhq.com/docs)
- **Vue.js**: See [Vue 3 Guide](https://vuejs.org)

---

**Version**: v4.0 | **Last Updated**: March 2025  
**Theme**: Earthy Luxury | **Built with**: Vue.js + Tailwind + Chart.js