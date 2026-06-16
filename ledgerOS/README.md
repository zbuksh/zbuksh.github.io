# LedgerOS Education Registry

A complete front-end-only browser demo of a futuristic blockchain-based education provider registry operating system. It is visually inspired by Linux desktop concepts, glassmorphism OS interfaces, macOS-style docks/windows, and enterprise permissioned-ledger dashboards.

## How to run

1. Download and unzip the project.
2. Open `index.html` directly in a modern browser.
3. No server, backend, package manager, Node.js, build tool, database, or blockchain node is required.

## First-load setup behavior

On first load, LedgerOS checks browser `localStorage` for the `ledgerOSData` object.

- If no login profile exists, the setup screen asks you to create a preferred password.
- The password is saved inside the localStorage JSON object for demo purposes only.
- After setup, the login screen is shown.
- On future loads, the app skips setup and opens the login screen directly.

## Login behavior

Use the password created during setup. If successful, the OS desktop unlocks. If incorrect, an audit log entry is created.

You can change the password from:

`Settings > Account > Change password`

## Browser search behavior

The Browser app includes an address/search bar.

- Text queries open Google Search in a new browser tab.
- URLs starting with `http://` or `https://` open directly in a new tab.
- External websites are not embedded in iframes because many sites block iframe loading.

## Demo-only localStorage data

All app data is stored under one browser localStorage key:

```text
ledgerOSData
```

The data includes:

- Auth profile
- Settings
- Registered providers
- Licenses
- Blockchain blocks
- Transactions
- Audit logs
- Registry metadata

## Simulated blockchain disclaimer

This project simulates blockchain behavior in JavaScript. It creates transactions, blocks, fake SHA-style hashes, previous-hash links, consensus status, node confirmations, smart contract validation results, and ledger integrity checks.

There is no real blockchain, no real Hyperledger Fabric network, no cryptographic signing, and no backend service.

> “This project is a front-end-only prototype. Authentication, blockchain, smart contract validation, consensus, and neural network features are simulated in browser localStorage for demonstration purposes only. Do not use this as a production security, compliance, or registry system.”

## No real Hyperledger connection

LedgerOS uses Hyperledger-style terminology and UI concepts such as permissioned ledger, validators, PBFT, Raft, smart contract validation, block height, and consensus. These are simulated for demonstration only.

## Reset data

Options:

- `Settings > Data > Clear all local data`
- Terminal command: `reset demo`
- Browser DevTools: clear localStorage for the site

## Export/import JSON

Export options:

- Settings: export full `ledgerOS-export.json`
- Blockchain Explorer: export `blockchain-export.json`
- Registry Search: export selected registry result as `registry-search-export.json`
- Audit Logs: export `audit-logs-export.json`
- Terminal command: `export json`

Import:

- Go to `Settings > Data`
- Select a JSON file
- The app validates that the expected structure exists
- If valid, it replaces the current localStorage data after confirmation

## Load sample data

Sample data is not auto-loaded. To load demo records:

`Settings > Data > Load sample demo data`

This creates at least 8 providers and additional blockchain transactions/blocks.

## File structure

```text
LedgerOS-Education-Registry/
├── index.html
├── styles.css
├── script.js
├── demo-data.json
└── README.md
```

## Main apps

- Browser
- Provider Registry
- Registry Search
- Blockchain Explorer
- Neural Network Viewer
- Bash Terminal
- File Explorer
- Settings
- System Monitor
- Audit Logs

## Notes

- The project works offline except for external searches opened from the Browser app.
- No external icon libraries are required.
- All UI is implemented with HTML, CSS, and vanilla JavaScript.
