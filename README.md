🌐✨ FuelEU Maritime Compliance Suite

🧭 Smart · Modular · Compliant
A next-generation platform transforming FuelEU Maritime compliance into a data-driven, interactive experience — built on Clean Architecture and modern web technology.

⚙️ Tech Blueprint
Layer	Stack
🎨 Frontend	React · TypeScript · TailwindCSS · Vite
⚙️ Backend	Node.js · Express · PostgreSQL · TypeScript
🧱 Architecture	Hexagonal (Ports & Adapters / Clean Architecture)
🧪 Testing	Vitest (Unit & Integration)
📚 Docs	AGENT_WORKFLOW.md · REFLECTION.md
🌊 What It Does

FuelEU Maritime Compliance Suite unites regulation data, vessel insights, and energy efficiency metrics into a single elegant dashboard.

✨ Key Capabilities

🗺️ Map & analyze maritime routes

📊 Compare compliance performance

💰 Bank or apply surpluses

🤝 Create compliance pools

💡 Visualize fuel efficiency impact

Designed with clarity, modularity, and domain-driven logic at its heart.

🗂️ Project Structure
📁 Backend

🧱 Built with a Hexagonal Architecture, ensuring testability and clean separation of concerns.

core/ → 🧠 Domain entities & logic

application/ → ⚙️ Business rules (use-cases)

ports/ → 🔌 Interfaces for adapters

adapters/

inbound/http/ → 🌐 Express controllers

outbound/postgres/ → 🐘 PostgreSQL repositories

infrastructure/

db/ → 🧩 Migrations & seed data

server/ → 🚀 Composition root

shared/ → 🧭 Common constants & utilities

💻 Frontend

💅 Powered by React, TailwindCSS, and Vite, delivering a fast, responsive UI for compliance analytics.

core/ → 🧠 Pure domain types

adapters/

ui/ → 🎨 Pages & components (inbound)

infrastructure/ → 🔗 API client (outbound)

🧩 Clean separation ensures testing, replacing, or extending layers remains effortless.

🧰 Setup Guide
⚙️ Backend Setup

1️⃣ Configure Environment

cd backend
cp .env.example .env


➡️ Update DATABASE_URL and PORT.

2️⃣ Install Dependencies

npm install


3️⃣ Run Migration & Seed

npm run migrate
npm run seed


4️⃣ Start the Server

npm run dev


🚀 Runs at http://localhost:3001

💻 Frontend Setup

1️⃣ Install Dependencies

cd frontend
npm install


2️⃣ Launch Development Server

npm run dev


🌍 Runs at http://localhost:5173

⚡ Vite automatically proxies API requests to the backend.

🔗 Core API Endpoints
Method	Endpoint	Description
GET	/routes	Fetch all seeded routes
POST	/routes/:id/baseline	Set a baseline route
GET	/routes/comparison	Compare baseline with others
GET	/compliance/cb	Compute compliance balance
GET	/compliance/adjusted-cb	CB after applying banked records
GET	/banking/records	Retrieve banking ledger
POST	/banking/bank	Bank positive CB
POST	/banking/apply	Apply banked CB
POST	/pools	Create and validate a pool

🧮 Formula Used
CB = (Target(89.3368) − Actual) × (FuelConsumption × 41,000 MJ/t)

🧪 Testing Suite
cd backend
npm test


🧩 Covers:

ComputeCB

ComputeComparison

BankSurplus

ApplyBanked

CreatePool

✅ In-memory tests — no external DB required.

🖼️ Dashboard Highlights
🗺️ Routes

Explore all registered routes and set a baseline.
<img src="docs/screenshots/Routes.png" width="750"/>

📊 Compare

Visualize performance differences & efficiency metrics.
<img src="docs/screenshots/Compare.png" width="750"/>

🏦 Banking

Manage your compliance balance & surpluses.
<img src="docs/screenshots/Banking.png" width="750"/>

🤝 Pooling

Collaboratively balance compliance across fleets.
<img src="docs/screenshots/Pooling.png" width="750"/>

💼 Developer Notes

✅ TypeScript strict mode enabled

🧹 ESLint + Prettier ready

🐘 PostgreSQL via pg

🧱 Decoupled, domain-driven, and framework-agnostic design

🌟 Why It Stands Out

✨ Architected for change — easily swap adapters, UI, or databases
⚡ Performance-first — Vite + Tailwind = lightning-fast UI
🧠 Domain-driven — business logic isolated from frameworks
🔍 Testable — core logic runs standalone

🚀 Built for the Future of Maritime Compliance

Sail beyond regulations — with structure, precision, and innovation.

🛞 FuelEU Maritime Compliance Suite — Where Clean Architecture meets the open sea.