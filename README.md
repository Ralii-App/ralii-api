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
#### 🔐 RL-100 — Identity & Access
Handles authentication, user identity, and role-based access.

**RL-101: User Authentication**
*   Sign up / sign in
*   Token validation (Firebase Auth / JWT)

**RL-102: User Profiles**
*   Personal details
*   Skills and interests

**RL-103: Roles & Permissions**
*   Volunteer
*   Charity / Organisation
*   Admin (future)

**Example Tables**
*   `rl101_users`
*   `rl103_user_roles`

---

#### 🤝 RL-200 — Community Jobs
Supports the creation and participation of local, community-driven jobs.

**RL-201: Create Community Job**
*   Job details (title, description, category)
*   Location and time

**RL-202: Browse & Join Jobs**
*   View nearby jobs
*   Join or leave a job

**RL-203: Participation Tracking**
*   Track volunteers per job
*   Basic status management

**Example Tables**
*   `rl201_community_jobs`
*   `rl203_job_participants`

---

#### 💬 RL-300 — Group Join Requests & Communication
Routes volunteers to charity-managed communication channels without hosting chats.

**RL-301: Charity Contact Channels**
*   WhatsApp
*   Discord
*   Instagram
*   Email

**RL-302: Join Requests**
*   "Request to join" submissions
*   Message templates

**RL-303: Join Request History (optional)**
*   Audit trail for charities

**Example Tables**
*   `rl301_charity_contacts`
*   `rl302_join_requests`

---

#### 💰 RL-400 — Fundraisers & Donations
Manages fundraising initiatives while keeping financial transactions outside the platform.

**RL-401: Create Fundraiser**
*   Cause description
*   Goals and deadlines

**RL-402: Monetary Donations (Informational)**
*   Bank details
*   QR code data

**RL-403: Item-Based Donations**
*   Food, blankets, clothing, pet supplies

**RL-404: Fundraiser Status & Updates**

**Example Tables**
*   `rl401_fundraisers`
*   `rl403_donation_items`

> **Note:** The API does not process payments directly.

---

#### 📍 RL-500 — Discovery & Location
Supports location-aware discovery of charities, jobs, and fundraisers.

**RL-501: Location Services**
*   Coordinates and regions

**RL-502: Nearby Search**
*   Radius-based queries

**RL-503: Filters & Categories**

**Example Tables**
*   `rl501_locations`
*   `rl502_entity_locations`

---

#### 🛡️ RL-600 — Trust, Safety & Moderation (Planned)
Ensures platform integrity and user safety as the project grows.

**RL-601: Reporting**
*   Flag inappropriate content

**RL-602: Verification**
*   Trusted charities

**RL-603: Moderation Tools**

**Example Tables**
*   `rl601_reports`
*   `rl602_verification_status`

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
