<h1 align="center">
  <img src="public/logo.png" width="160" />
  <br />
  Nexus POS
</h1>

<p align="center">
  <strong>Point of Sale and business management system by Nexus Core Systems</strong><br />
  Offline-first • Multi-branch • Touchscreen friendly
</p>

---

## Features

- **Point of sale** – fast product search and barcode scanning, split payments, pay-later (credit), coupons, automatic discounts, loyalty points, printable receipts with a receipt designer.
- **Sales documents** – quotations, customer orders with deposits, customer balances, returns and refunds (with or without restocking).
- **Inventory** – multiple warehouses, stock transfers, adjustments and stock counts, purchases and purchase returns, suppliers, categories, brands, barcode labels.
- **Finance** – expenses, cash/bank accounts with balances, taxes, configurable currency.
- **People** – employees, attendance (clock in/out), payroll and commissions.
- **Operations** – recipes and production batches, riders and deliveries.
- **Reports** – daily sales, by branch, by cashier, products, expenses, returns, stock, payroll and more; export to CSV or print.
- **Administration** – users, roles and permissions, branches, backup and restore, audit trail.

## Development

### Stack
- **Frontend**: React 19, TypeScript, Vite, Tailwind CSS, Chart.js
- **Desktop**: Electron, Node.js
- **Database**: SQLite + TypeORM

### Run from source

```bash
npm install
npm run dev
```

### Scripts

| Script | Description |
|--------|-------------|
| `npm run dev` | Vite + Electron with hot reload |
| `npm run build` | Production build |
| `npm run dist:win` | Windows installer |
| `npm run seed` | Load sample data |
| `npm run lint` | Lint the code |

### Project structure

```
├── src/
│   ├── main/         # Electron main process (DB, IPC)
│   ├── renderer/     # React frontend (UI, routing, hooks)
│   ├── services/     # Business logic
│   └── entities/     # Database entities
├── public/           # Logo and static assets
└── build/            # App icons
```

Product name, logo and contact details shown in the app are set in `src/renderer/branding.ts`.

### Troubleshooting

- **Database errors**: make sure the app can write to its data folder. Try `npm run rebuild` for the SQLite native module.
- **Build errors**: use Node.js 18+, then clear `node_modules` and `dist`.

## License

© Nexus Core Systems. All rights reserved.

Nexus POS is based on [Tillify](https://github.com/CyberArcenal/Tillify) by CyberArcenal, used under the Apache License 2.0 (see [LICENSE](./LICENSE) and [NOTICE](./NOTICE)).
