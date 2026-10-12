# OpenStock

A stock-market dashboard for exploring market data, company information, watchlists, and interactive charts.

## Features

- Email/password authentication
- Stock search, company profiles, and market news
- Personal watchlists
- Interactive TradingView charts and market widgets
- Market overview and heatmaps
- Optional AI-powered welcome messages and email workflows

## Tech Stack

- **Frontend:** Next.js 15, React 19, TypeScript, Tailwind CSS
- **UI:** shadcn/ui, Radix UI, Lucide
- **Authentication:** Better Auth
- **Database:** MongoDB, Mongoose
- **Market data:** Finnhub, TradingView
- **Workflows and email:** Inngest, Nodemailer

## Getting Started

### Requirements

- Node.js 20 or later
- npm or pnpm
- A MongoDB connection string
- A Finnhub API key

### Install

```bash
git clone <your-repository-url>
cd <your-project-folder>
npm install
```

### Configure environment variables

Create a `.env` file in the project root:

```env
NODE_ENV=development
MONGODB_URI=your_mongodb_connection_string
BETTER_AUTH_SECRET=your_random_secret
BETTER_AUTH_URL=http://localhost:3000
NEXT_PUBLIC_FINNHUB_API_KEY=your_finnhub_api_key
FINNHUB_BASE_URL=https://finnhub.io/api/v1
```

Add optional credentials only for the integrations you enable, such as Gemini, Adanos, Inngest, or email delivery. Never commit real secrets or your `.env` file.

### Run locally

```bash
npm run dev
```

Open [http://localhost:3000](http://localhost:3000).

### Production build

```bash
npm run build
npm start
```

## Deployment

Deploy as a **Node.js web service** on a platform that supports Next.js server-side features.

- **Build command:** `npm ci && npm run build`
- **Start command:** `npm start`
- Set the production environment variables in the hosting dashboard.
- Set `BETTER_AUTH_URL` to the deployed HTTPS URL.
- Configure MongoDB Atlas network access to allow the deployed service to connect.

## Notes

- Market-data availability and delays depend on the provider and API plan.
- TradingView may restrict some markets or symbols.
- This project is for informational purposes and is not a brokerage or financial advice.

## Credits and License

This project is based on the open-source **OpenStock** project by [Open Dev Society](https://github.com/Open-Dev-Society/OpenStock). It also acknowledges [JavaScript Mastery](https://www.youtube.com/@javascriptmastery) for the stock-market app tutorial that helped inspire the project.

Licensed under **GNU AGPL-3.0**. If you modify or deploy this project, follow the license's source-code disclosure and attribution requirements. See [LICENSE](./LICENSE) for details.
