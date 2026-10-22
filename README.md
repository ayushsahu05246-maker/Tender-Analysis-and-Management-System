# Tender Analysis and Management System (TAMS)

A modern, enterprise-grade tender analysis and lifecycle management system with intelligent automated bid evaluation, multi-stage tender processing, vendor portal, and comprehensive procurement analytics.

![Version](https://img.shields.io/badge/version-1.0.0-blue)
![License](https://img.shields.io/badge/license-MIT-green)
![Python](https://img.shields.io/badge/python-3.11+-blue)
![FastAPI](https://img.shields.io/badge/FastAPI-0.100+-green)
![React](https://img.shields.io/badge/react-19-blue)

---

## 🌟 Key Capabilities

### 🏛️ Complete Tender Lifecycle
- **End-to-End Processing**: Draft → Approval → Publish → Bid Submission → Technical & Financial Evaluation → Award → Contract → Closure.
- **Flexible Stages**: Single-stage, two-stage (technical + financial), and multi-stage tender workflows.
- **Tender Categories & Types**: Open National/International, Limited Tenders, Single Source, and Expressions of Interest (EOI).
- **Document Management**: Encrypted uploads, PDF generation, version tracking, and automated document extraction.

### 🧠 Intelligent Analysis & Evaluation
- **Eligibility Compliance Screening**: Automated verification of eligibility requirements, turnover thresholds, and statutory documents.
- **Technical Bid Scoring**: Configurable weighted matrix scoring for transparent technical review.
- **L1 / L2 Financial Comparison**: Automated financial bid comparative chart generation with tax breakdown.
- **RFP Document Generation**: Dynamic RFP document creation adhering to procurement standards.

### 💼 Post-Award & Contract Management
- **Letter of Intent (LoI) & Acceptance (LoA)**: Seamless generation and acceptance workflows.
- **Purchase Order & Milestone Tracking**: Progress-linked milestone management and payment schedule tracking.
- **Invoice & EMD / Bank Guarantee**: Track Earnest Money Deposits, Performance Bank Guarantees, expiry reminders, and releases.

### 📊 Real-Time Analytics & Reporting
- **Executive Dashboard**: Real-time KPI summaries, active tender counts, financial volume, and stage distribution.
- **Department & Category Spend**: Visual insights into procurement spend and vendor participation.
- **Export Formats**: Instant export to PDF, Excel, and CSV formats.

---

## 🛠️ Technology Stack

| Layer | Technology |
|---|---|
| **Frontend** | React 19, TypeScript, Vite, Lucide Icons, Modern Responsive Design |
| **Backend** | Python 3.11+, FastAPI, SQLAlchemy, Pydantic v2 |
| **Database** | SQLite (Default / Lightweight) / PostgreSQL (Production) |
| **Security** | JWT Authentication, Role-Based Access Control (RBAC), Password Hashing |

---

## 🚀 Getting Started

### 1. Clone the Repository

```bash
git clone https://github.com/ayushsahu05246-maker/Tender-Analysis-and-Management-System.git
cd Tender-Analysis-and-Management-System
```

### 2. Backend Setup

```bash
cd backend

# Create and activate virtual environment
python -m venv venv
# On Windows:
.\venv\Scripts\activate
# On Linux/macOS:
# source venv/bin/activate

# Install dependencies
pip install -r requirements.txt

# Run the backend server
uvicorn app.main:app --reload --port 3399
```

The backend API will be live at `http://localhost:3399` and API docs at `http://localhost:3399/docs`.

### 3. Frontend Setup

```bash
cd ../frontend

# Install dependencies
npm install

# Start the development server
npm run dev
```

Open `http://localhost:5173` in your browser.

---

## 👥 Default Roles & Credentials

| Role | Email | Password |
|---|---|---|
| **Administrator** | `admin@gov.in` | `Password@123` |
| **Tender Officer** | `officer1@meity.gov.in` | `Password@123` |
| **Evaluator** | `eval1@gov.in` | `Password@123` |
| **Bidder / Vendor** | `procurement@tcs.com` | `Password@123` |

---

## 📁 Repository Structure

```
Tender-Analysis-and-Management-System/
├── backend/
│   ├── app/
│   │   ├── api/v1/endpoints/    # REST endpoints (auth, tenders, bids, analytics)
│   │   ├── core/                # Security, JWT, hashing
│   │   ├── models/              # SQLAlchemy database models
│   │   ├── schemas/             # Pydantic schemas
│   │   ├── services/            # Business & export services
│   │   ├── config.py            # System configuration
│   │   └── main.py              # FastAPI entry point
│   ├── tams.db                  # Pre-seeded database
│   ├── seed_data.py             # Database seed script
│   └── requirements.txt         # Python dependencies
├── frontend/
│   ├── src/
│   │   ├── components/          # Reusable UI components & layouts
│   │   ├── pages/               # Tenders, bids, analytics, auth pages
│   │   ├── services/            # API client services
│   │   └── App.tsx              # Application root
│   ├── index.html
│   └── package.json
├── docker-compose.yml           # Container orchestration
└── README.md
```

---

## 📄 License

This project is licensed under the MIT License.
