# 🚀 Amazon Listing Optimizer (AI-Powered with ASIN Fetch & SEO Enhancements)

> **AI-driven tool to fetch Amazon product data using ASIN, optimize listings (Title, Bullets, Description, Keywords), and track improvements with history storage.**
> **Developed by *Aditya Walia***

---

### 🏴‍☠️ Tech Stack & Tools

![Node.js](https://img.shields.io/badge/Node.js-000?style=for-the-badge\&logo=node.js)
![React](https://img.shields.io/badge/React-000?style=for-the-badge\&logo=react)
![MySQL](https://img.shields.io/badge/MySQL-000?style=for-the-badge\&logo=mysql)
![LLM](https://img.shields.io/badge/AI_LLM-000?style=for-the-badge\&logo=openai)
![Amazon](https://img.shields.io/badge/Amazon_ASIN_Fetch-000?style=for-the-badge\&logo=amazon)

---

## 🧭 Project Overview

E-commerce sellers often struggle with **poorly optimized Amazon listings** that affect ranking and conversions.
This application solves that by:

✅ Fetching real Amazon listing data using **ASIN**
✅ Using **LLM (OpenAI/Gemini)** to generate optimized title, bullets & description
✅ Displaying **Original vs Optimized** content
✅ Saving every optimization in **MySQL History**

---

## 🎯 Core Features

| Feature                 | Description                                                  |
| ----------------------- | ------------------------------------------------------------ |
| 🔍 ASIN Fetch           | Extract product title, bullets, description using custom API |
| 🤖 AI Optimization      | Rewrite content using LLM (SEO-focused + readable)           |
| 🖥 React UI             | Side-by-side comparison of original vs optimized listing     |
| 💾 History Storage      | Track all edits & timestamps in MySQL                        |
| 🌍 Multi-Market Support | US, IN, UK, DE, FR, etc.                                     |
| 🧪 Ready for Scaling    | Bulk ASIN, Templates, A/B testing (future)                   |

---

## 🏗 System Architecture

```
User (React UI)
      ↓
Enter ASIN
      ↓
Backend (Node.js / Express)
  ├── Fetch ASIN Data (Amazon API)
  ├── Send to AI (OpenAI/Gemini)
  └── Store in MySQL
      ↓
Frontend Comparison View
```

---

## 🧱 Folder Structure (Planned)

```
/amazon-listing-optimizer
 ├─ /client        # React Frontend
 ├─ /server        # Node.js Backend
 │   ├─ routes
 │   ├─ controllers
 │   └─ services   # asinService.js / aiService.js
 ├─ /database      # SQL Schema / Migrations
 └─ README.md
```

---

## ⚙️ Backend Setup

```bash
cd server
npm install
npm start
```

Configure `.env`:

```
DB_HOST=localhost
DB_USER=root
DB_PASS=1234
DB_NAME=asin_history
LLM_API_KEY=your_key_here
```

---

## 🗄 MySQL Schema Example

```sql
CREATE TABLE listing_history (
    id INT AUTO_INCREMENT PRIMARY KEY,
    asin VARCHAR(20),
    original_title TEXT,
    optimized_title TEXT,
    original_bullets TEXT,
    optimized_bullets TEXT,
    optimized_description TEXT,
    keywords TEXT,
    created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);
```

---

## 🤖 AI Prompt Example

```
You are an Amazon SEO optimization expert.
Improve the provided product listing:
- Rewrite the title with SEO keywords and clarity.
- Refine bullet points to be benefit-driven.
- Enhance the product description persuasively.
- Add 5 new relevant keywords.
```

---

## 📡 API Endpoints

| Method | Endpoint             | Purpose                     |
| ------ | -------------------- | --------------------------- |
| `GET`  | `/api/asin/:id`      | Fetch original product data |
| `POST` | `/api/optimize`      | AI-based content rewrite    |
| `GET`  | `/api/history/:asin` | Retrieve past optimizations |

---

## 🖥 Frontend (React UI)

| Screen                 | Purpose                       |
| ---------------------- | ----------------------------- |
| 🟦 **ASIN Input Page** | User enters ASIN              |
| 🟨 **Comparison View** | Original vs Optimized Listing |
| 🟩 **History Page**    | Shows all saved revisions     |

---

## 🖼 Screenshots (from Base ASIN Fetch Module)

### 🔍 Product List Fetch (Original Data Source)

![Product List](https://i.imgur.com/ES5M4Rx.png)

### 🗣 Review List Fetch (Reference for Review Capability)

![Review List](https://i.imgur.com/HuBW3rl.png)

> These are sample visual references from the underlying ASIN fetch integration. Final UI will include custom React pages.

---

## 🔮 Future Enhancements

* 🔁 Bulk ASIN Support
* 🧪 A/B Testing between AI versions
* 🌐 Multi-language listings (DE/FR/ES)
* 📦 Export CSV / JSON ready drafts

---

## 🧾 License

MIT – Free to modify & build upon.

---

## 🧑‍💻 Developer Credit

**Built & Engineered by *Aditya Walia***
E-commerce • AI • Full Stack Innovation

