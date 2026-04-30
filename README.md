# BusinessFinder Pro

**Intelligent Local Lead Generation & Business Intelligence Platform**

## Overview

BusinessFinder Pro is a production-ready SaaS platform that transforms how businesses discover, analyze, and connect with local prospects. Search any location, filter by 13+ business categories, and instantly identify high-value leads using a proprietary scoring engine. One-click WhatsApp outreach templates make contacting prospects effortless.
# Intelligent-Local-Lead-Generation-Business-Intelligence-Platform
BusinessFinder Pro is a full-stack SaaS platform that discovers, scores, and connects you with local businesses. Search any location, filter by 13+ categories, and instantly identify high-value leads using the built-in scoring engine. One-click WhatsApp outreach templates make contacting prospects effortless.

Designed for marketing agencies, freelancers, and sales teams who need to find and qualify local business leads at scale.

## Features

### Business Discovery
- Search by city, address, or postal code with customizable radius (1–50 km)
- 13 pre-configured business categories: Restaurants, Hotels, Salons, Gyms, Cafés, Banks, Pharmacies, Schools, Clothing Stores, Electronics Shops, Bakeries, Fast Food, Doctor Clinics
- Real-time results rendered on an interactive map and sortable list view
- Detailed business profiles with address, phone, website, rating, and coordinates

### Lead Scoring Engine
- Automated 0–100 scoring for every discovered business
- Six weighted scoring factors: Sales Opportunity (35), Contactability (20), Recognition (15), Category Fit (12), Proximity (8), Rating Bonus (10)
- Three priority tiers with visual indicators: Hot (70–100), Medium (40–69), Low (0–39)
- Transparent score breakdown available per business

### WhatsApp Outreach
- One-click messaging via WhatsApp Web API
- Four pre-built message templates adaptable to each business category
- Templates cover value introduction, free audit offers, case study approaches, and direct benefit questions
- No third-party tools required

### Interactive Mapping
- Leaflet.js integration with OpenStreetMap tiles
- Color-coded markers based on lead score tier
- Click-on-pin to view business summary
- Responsive map with zoom and pan controls

### Analytics Dashboard
- Rating distribution visualization
- Lead score distribution chart
- Category breakdown analysis
- Summary metrics: Average Rating, Average Distance, Total Hot Leads Found

### Lead Management
- Save businesses to personal collection
- Track outreach status: New, Contacted, Interested, Not Interested
- Add private notes to each saved lead
- Filter views by status and lead score tier

### Advanced Filtering
- Minimum rating threshold
- Minimum review count threshold
- Business category selection
- Distance radius control
- Hot Leads Only toggle

### User Interface
- Dark mode by default with consistent color palette
- Fully responsive design for desktop, tablet, and mobile
- Professional SaaS layout with sidebar navigation
- Smooth transitions and hover states throughout

---

## Tech Stack

| Layer | Technology |
|-------|------------|
| Frontend Framework | React.js / Next.js |
| Styling | Tailwind CSS |
| Maps | Leaflet.js + OpenStreetMap |
| Charts | Recharts |
| Icons | Lucide React |
| Backend Framework | Python FastAPI |
| Database | SQLite (upgradable to PostgreSQL) |
| Business Data | Google Places API |
| Geocoding | OpenStreetMap Nominatim |
| Deployment | Vercel (frontend), Railway (backend) |

---

## Quick Start

### Prerequisites

- Node.js 18 or later
- Python 3.9 or later
- Google Places API key

### Installation

**Clone the repository**
git clone https://github.com/yourusername/businessfinder-pro.git
cd businessfinder-pro

Backend setup

cd backend
python -m venv venv
source venv/bin/activate
pip install -r requirements.txt
cp .env.example .env
Edit .env and add your credentials:

### env
GOOGLE_PLACES_API_KEY=your_api_key_here
DATABASE_URL=sqlite:///businessfinder.db
SECRET_KEY=your_secret_key

### Start the backend server:
uvicorn app.main:app --reload --port 8000

### Frontend setup

cd ../frontend
npm install
cp .env.example .env.local
npm run dev
Open http://localhost:3000 in your browser.

### Project Structure

### businessfinder-pro/
├── frontend/
│   ├── components/
│   │   ├── Dashboard/
│   │   ├── Map/
│   │   ├── Leads/
│   │   ├── Filters/
│   │   ├── Outreach/
│   │   └── Charts/
│   ├── pages/
│   ├── hooks/
│   ├── utils/
│   └── styles/
├── backend/
│   ├── app/
│   │   ├── api/
│   │   ├── models/
│   │   ├── services/
│   │   └── main.py
│   ├── requirements.txt
│   └── .env.example
├── database/
│   └── schema.sql
├── docs/
│   ├── SETUP.md
│   ├── API.md
│   └── DEPLOYMENT.md
├── README.md
└── LICENSE

### Environment Variables
### Backend

### Variable	Description	Required
 GOOGLE_PLACES_API_KEY	Google Places API key	Yes
 DATABASE_URL	Database connection string	Yes
 SECRET_KEY	Application secret key	Yes

### Frontend
 Variable	Description	Required
 NEXT_PUBLIC_API_URL	Backend API base URL	Yes
 NEXT_PUBLIC_MAP_TILE_URL	Map tile server URL	No

### API Reference
 GET /api/places/search

### Lead Scoring Methodology
 Each business receives an automated score calculated from six weighted factors:

### Factor	Weight	Criteria

 Sales Opportunity	35%	Missing website, incomplete listing, low digital presence
 Contactability	20%	Availability of phone, email, or social media profiles
 Recognition	15%	Brand signals, operating hours completeness, address accuracy
 Category Fit	12%	Market demand level for the specific business category
 Proximity	8%	Distance from the search center point
 Rating Bonus	10%	Verified Google rating of 4.0 or higher

### Score Tiers:

 Tier	Range	Label	Recommended Action
 Hot	70–100	Green	Contact within 24 hours
 Medium	40–69	Yellow	Add to outreach pipeline
 Low	0–39	Red	Monitor for changes

