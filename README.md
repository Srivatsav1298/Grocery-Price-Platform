# MATPRIS - Grocery Price Intelligence

A production-quality web application for comparing grocery prices across Norwegian supermarket chains without manually opening individual flyers.

## Overview

MATPRIS collects, normalizes, and compares grocery offers from Norwegian supermarkets, presenting them in an elegant, fast dashboard inspired by premium financial analytics tools.

## Features

- **Overview Dashboard** - Snapshot of current offers, retailers, and best deals
- **All Offers** - Sortable, filterable table of all current offers
- **Product Comparison** - Compare equivalent products across retailers
- **Shopping Basket** - Calculate basket totals across different stores
- **Deals** - Find best unit-price deals and promotions
- **Data Status** - Monitor data quality and freshness

## Tech Stack

- **Frontend:** React, TypeScript, Vite, Tailwind CSS, shadcn/ui
- **Data Pipeline:** Python, Pandas, Pydantic
- **Visualization:** TanStack Table, Recharts
- **Deployment:** GitHub Pages (static)

## Quick Start

### Prerequisites

- Node.js 18+ and npm
- Python 3.9+

### Installation

```bash
# Install dependencies
npm install

# Generate synthetic test data
python scripts/generate_fixtures.py

# Start development server
npm run dev
```

The app will be available at `http://localhost:5173`

### Build for Production

```bash
npm run build
```

The built files will be in the `dist/` directory.

## Data Sources

This application is designed to work with data from [Mattilbud.no](https://www.mattilbud.no/) via patterns from the [kundeavis-mcp](https://github.com/donadelicc/kundeavis-mcp) project.

**Important Notes:**
- The Tjek API (used by Mattilbud.no) is undocumented and not an officially published open API
- Permission to use live data should be verified
- Currently uses synthetic test data by default
- No offer data is redistributed

## Development

### Scripts

```bash
npm run dev          # Start dev server
npm run build        # Build for production
npm run test         # Run tests
npm run lint         # Lint code
python scripts/generate_fixtures.py  # Generate test data
```

## License

MIT License - see LICENSE file for details

## Disclaimer

This project is not affiliated with, endorsed by, or connected to Tjek, mattilbud.no, or any retailer. All trademarks belong to their owners.
