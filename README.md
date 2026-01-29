# Ralii — API

This repository contains the backend API for **Ralii**, an open-source platform designed to support volunteering, community action, and fundraising.

The API provides the data, authentication, and business logic used by the Ralii Android application and future clients.

---

## 🎯 Purpose

The Ralii API is responsible for:
- User authentication and role management
- Charity and organisation data
- Community jobs and volunteer participation
- Fundraisers (monetary and item-based)
- Join request routing and contact handling
- Location-based discovery support

The API is designed to be **modular, secure, and scalable**, while remaining simple enough for community-driven development.

---

## 🧱 Domain-Based Organisation

The API mirrors the same module structure used by the Android app to keep frontend and backend aligned.

### Domain Modules
- **RL-100** — Identity & Access
- **RL-200** — Community Jobs
- **RL-300** — Group Join Requests
- **RL-400** — Fundraisers & Donations
- **RL-500** — Discovery & Location
- **RL-600** — Trust & Moderation (planned)

Each domain owns its routes, services, and database tables.

---

## 🗄️ Data Ownership

Database tables are organised by module to maintain clarity and separation of concerns.

Example:
- `rl101_users`
- `rl201_community_jobs`
- `rl401_fundraisers`

This approach supports future scaling and easier maintenance.

---

## 🛠 Tech Stack (Planned / TBC)

- RESTful API
- Authentication (Firebase Auth / JWT)
- Relational database (PostgreSQL / MySQL)
- Container-ready architecture

Exact implementation details will evolve as the project grows.

---

## 🔐 Security & Trust Principles

- The API does **not** process payments directly
- Sensitive actions are role-protected
- Join requests never auto-add users to groups
- Reporting and moderation features are planned

---

## 🚀 Getting Started

Setup instructions will be added once the initial API scaffold is complete.

Contributors are encouraged to:
- Review the module documentation
- Pick an open issue
- Propose improvements via pull requests

---

## 🤝 Contributing

This is a community-driven project.

Please read `CONTRIBUTING.md` before submitting:
- Issues
- Pull requests
- Architectural changes

---

## 🔗 Related Repositories

- **Ralii Android App**  
  👉 https://github.com/<your-org-or-username>/ralii-android

---

## 📄 Licence

This project is licensed under the **MIT Licence**.
