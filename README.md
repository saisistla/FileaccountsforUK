# APPLICAT-1 — Application to Prepare and File Accounts for Small Limited Companies in England

## Intent

This application is designed specifically for small limited companies registered in England, primarily targeting farm and packhouse teams. It aims to simplify the preparation and filing of company accounts in compliance with HMRC regulations.

## Features

- Guided data collection including bank transactions and other financial inputs.
- Preparation of draft and final accounts as per HMRC requirements.
- User review and approval workflow for final accounts.
- Electronic filing of returns following HMRC procedures.

## Out of Scope

- Accounting services for companies outside England.
- Manual bookkeeping or bank transaction processing.
- Tax advice beyond general efficiency suggestions.
- Support for complex corporate structures or audits.

## System Context

The system consists of a Web UI used by staff, communicating with an HTTP API backend. The API interacts with fixture JSON data stores and exposes a health check endpoint.

## Components

- **Data Collection Module** (Node.js): Handles guided input of financial data.
- **Accounts Preparation Module** (Python): Prepares draft and final accounts compliant with HMRC rules.
- **User Workflow Module** (Node.js): Manages review and approval workflows.
- **Filing Module** (Python): Manages electronic submission of accounts to HMRC.

## APIs

| Method | Path                                   | Purpose                                               |
|--------|----------------------------------------|-------------------------------------------------------|
| GET    | `/health`                             | Deployment verification endpoint, returns 'ok'       |
| GET    | `/api/simplify-accounts-preparatio`  | Simplify accounts preparation for small limited companies |
| GET    | `/api/ensure-compliance-with-engla`  | Ensure compliance with England HMRC accounting and filing standards |
| GET    | `/api/provide-clear-user-friendly-`  | Provide clear, user-friendly guidance throughout the process |
| GET    | `/api/help-users-optimize-tax-mana`  | Help users optimize tax management efficiently        |

## Usage

1. Staff access the Web UI.
2. The UI calls the API endpoints to retrieve guidance, compliance checks, and optimization tips.
3. Data is collected and stored in fixture JSON files.
4. Accounts are prepared and reviewed through the workflow module.
5. Final accounts are electronically filed with HMRC.

## Technologies

- Node.js for API and UI modules.
- Python for accounts preparation and filing modules.
- Fixture JSON files for data storage.

## Deployment

The application is deployed using existing infrastructure pipelines. After linting, unit, and integration tests, and deploy approval, the pipeline runs targeting the dev environment.

## License

MIT

---

For detailed architecture and development notes, refer to the approved architecture.md file included in the repository.