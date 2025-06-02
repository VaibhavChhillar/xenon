# 🧠 Xeno Mini CRM Platform – SDE Internship Assignment 2025

Welcome to my submission for the Xeno SDE Internship Assignment! This project demonstrates a Mini CRM Platform designed to enable **customer segmentation**, **personalized campaign delivery**, and **AI-powered insights** using modern, scalable tools.

---

## 🚀 Features Implemented

### ✅ 1. Data Ingestion APIs
- RESTful APIs built using **Express.js** with secure validation layers.
- Endpoints for ingesting:
  - Customer data
  - Orders data
- Swagger UI for API documentation and testing.
- Bonus: Implemented **Redis Streams** for pub-sub:
  - API layer handles validation only.
  - Async data persistence via background consumers.

### ✅ 2. Campaign Creation UI
- Built using **React.js** with **Shadcn** and **TailwindCSS**.
- Users can:
  - Define audience segments with a dynamic **rule builder** (AND/OR logic).
  - Preview matching audience size in real-time.
  - View campaign history with:
    - Campaign details
    - Delivery stats (Sent/Failed)
    - Reverse-chronological order

- Bonus: Intuitive UX with visual logic blocks.

### ✅ 3. Campaign Delivery & Logging
- Upon saving a segment, a campaign is created:
  - Logged into a `communication_log` table.
  - Sends personalized messages to each customer via a dummy vendor API.
- **Vendor API** simulates real-world message delivery:
  - 90% SENT, 10% FAILED responses
- Delivery receipt API updates logs with status.
- Bonus: Batch-based consumer updates delivery statuses from async queue.

### ✅ 4. Authentication
- Integrated **Google OAuth 2.0** using `passport-google-oauth20`.
- Only authenticated users can create/view campaigns.

### ✅ 5. AI-Powered Features

#### 💬 Natural Language to Rule Conversion
- Users can write prompts like:
  > “People who haven’t shopped in 6 months and spent over ₹5K”
- Automatically parsed into logical conditions using **OpenAI GPT-4 API**.

#### ✉️ Message Suggestions
- Given a campaign goal, AI suggests 2–3 message variants.
- Example:
  > Campaign: "Bring back inactive users"  
  > AI Messages:
  - "Hey! We've missed you. Here’s 15% off just for you."
  - "Come back and enjoy a special reward—your next order is discounted!"

#### 📊 Campaign Summary Generator
- AI summarizes campaign performance into human-friendly insights.
  - Example:
    > "Your campaign reached 1,284 users. 1,140 messages were delivered. Customers with > ₹10K spend had a 95% delivery rate."

---

## 🛠 Tech Stack

| Layer         | Tech Used                          |
|---------------|------------------------------------|
| Frontend      | React.js, Vite, Tailwind, Shadcn   |
| Backend       | Node.js (Express.js)               |
| Database      | PostgreSQL (hosted on Neon)        |
| Auth          | Google OAuth 2.0                   |
| Pub-Sub       | Redis Streams                      |
| AI Integration| OpenAI GPT-4 API                   |
| API Docs      | Swagger + Postman Collection       |

---

## 📸 Screenshots

- [ ] Campaign Rule Builder
- [ ] Audience Preview
- [ ] Campaign History Page
- [ ] AI Message Suggestion Modal
- [ ] Authenticated Dashboard

---

## ⚙️ Installation & Setup

### 1. Clone the Repo
```bash
git clone https://github.com/your-username/xeno-crm.git
cd xeno-crm
