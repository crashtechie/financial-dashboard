# Financial Dashboard

Dashboard with data visualizations for the Financial Analysis Application - Phase 2 enhancement featuring charts, analytics, and spending insights.

## Overview

This repository contains the dashboard and analytics visualization features for the [Financial Analysis Application](https://github.com/crashtechie/finacial-analysis-app). It extends the base CRUD application with rich data visualizations and analytical insights.

## Planned Features

### Phase 1: Core Dashboard (Home Page Enhancement)

**Visual Components:**
- 📊 **Total Balance Summary** - Aggregate view of all account balances
- 📈 **Monthly Spending Trend** - Line chart showing spending over time
- 🥧 **Top 5 Categories** - Pie/doughnut chart of spending distribution
- 📝 **Recent Transactions** - Quick view of last 10 transactions
- 💰 **Quick Stats Cards** - Income, expenses, and net change metrics

**Technical Implementation:**
- React components with TypeScript
- Recharts library for charting
- Integration with existing analytics API endpoints
- Responsive grid layout with Tailwind CSS
- Real-time data fetching with Zustand state management

### Phase 2: Detailed Analytics Page

**Advanced Features:**
- 📊 **Spending Trends** - Interactive charts with daily/weekly/monthly toggle
- 🎯 **Category Breakdown** - Deep dive with comparison periods
- 🏪 **Top Merchants** - Bar chart showing merchants by spending
- 💹 **Income vs Expenses** - Stacked area chart for cash flow analysis
- 🗓️ **Date Range Filters** - Customizable time period selection
- 📤 **Export Capabilities** - Download charts as images or data as CSV

### Phase 3: Advanced Analytics (Future)

- Budget tracking and alerts
- Spending predictions (ML-based)
- Anomaly detection for unusual transactions
- Recurring transaction identification
- Custom report builder
- Multiple dashboard views (personal, business, investment)

## Tech Stack

### Frontend
- **React 18.2** - UI framework
- **TypeScript** - Type safety
- **Recharts** - Charting library (responsive, composable)
- **Tailwind CSS** - Styling
- **Zustand** - State management
- **date-fns** - Date manipulation
- **Vite** - Build tool

### Backend (Existing)
Uses analytics endpoints from the main application:
- `GET /api/analytics/spending-trends/` - Time-series data
- `GET /api/analytics/category-breakdown/` - Category aggregates
- `GET /api/analytics/merchants/` - Merchant statistics

## Project Structure

```
financial-dashboard/
├── src/
│   ├── components/
│   │   ├── charts/
│   │   │   ├── SpendingTrendChart.tsx
│   │   │   ├── CategoryPieChart.tsx
│   │   │   ├── MerchantBarChart.tsx
│   │   │   └── CashFlowChart.tsx
│   │   ├── dashboard/
│   │   │   ├── BalanceSummary.tsx
│   │   │   ├── QuickStats.tsx
│   │   │   ├── RecentTransactions.tsx
│   │   │   └── DashboardGrid.tsx
│   │   └── filters/
│   │       ├── DateRangeFilter.tsx
│   │       └── PeriodSelector.tsx
│   ├── pages/
│   │   ├── DashboardPage.tsx
│   │   └── AnalyticsPage.tsx
│   ├── api/
│   │   └── analytics.ts  # API client for analytics endpoints
│   ├── hooks/
│   │   └── useAnalytics.ts  # Custom hooks for data fetching
│   └── types/
│       └── analytics.ts  # TypeScript types for analytics data
├── tests/
│   └── components/  # Component tests
└── docs/
    ├── IMPLEMENTATION.md  # Detailed implementation guide
    └── DESIGN.md  # UI/UX design decisions
```

## Getting Started

### Prerequisites

This dashboard requires the main Financial Analysis Application to be running:
1. Clone the [main application](https://github.com/crashtechie/finacial-analysis-app)
2. Start the backend API server (Django on port 8000)
3. Ensure you have transaction data imported

### Installation

```bash
# Clone this repository
git clone https://github.com/crashtechie/financial-dashboard.git
cd financial-dashboard

# Install dependencies
npm install

# Configure API endpoint (if different from default)
echo "VITE_API_URL=/api" > .env.local

# Start development server
npm run dev
```

The dashboard will be available at `http://localhost:5173/`

### Integration

This dashboard can be:
1. **Standalone**: Run as a separate application (current approach)
2. **Integrated**: Merged into the main app's frontend as new pages/components
3. **Embedded**: Included as an iframe or web component

## Design Principles

1. **Data-Driven**: All visualizations backed by real transaction data
2. **Responsive**: Mobile-first design that adapts to all screen sizes
3. **Performant**: Lazy loading, data caching, and optimized renders
4. **Accessible**: WCAG 2.1 compliant charts and controls
5. **Intuitive**: Clear visual hierarchy and self-explanatory charts

## Development Roadmap

### Week 1: Foundation
- [ ] Set up project with Vite + React + TypeScript
- [ ] Install and configure Recharts
- [ ] Create analytics API client
- [ ] Build reusable chart wrapper components

### Week 2: Core Dashboard
- [ ] Balance summary card
- [ ] Quick stats cards (income, expenses, net)
- [ ] Spending trend line chart
- [ ] Category pie chart
- [ ] Recent transactions list
- [ ] Responsive grid layout

### Week 3: Analytics Page
- [ ] Full spending trends with period toggle
- [ ] Detailed category breakdown
- [ ] Merchant analysis bar chart
- [ ] Income vs expense area chart
- [ ] Date range filter controls

### Week 4: Polish & Testing
- [ ] Loading states and skeletons
- [ ] Error handling and retry logic
- [ ] Comprehensive testing
- [ ] Performance optimization
- [ ] Documentation

## Contributing

Contributions are welcome! Please:
1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-chart`)
3. Commit your changes (`git commit -m 'Add amazing chart'`)
4. Push to the branch (`git push origin feature/amazing-chart`)
5. Open a Pull Request

## Related Projects

- [Financial Analysis App](https://github.com/crashtechie/finacial-analysis-app) - Main application (backend + frontend CRUD)

## License

MIT License

## Author

**crashtechie**

---

**Status**: 🚧 In Development - Phase 1

**Next Milestone**: Core Dashboard Components (ETA: March 11, 2026)
