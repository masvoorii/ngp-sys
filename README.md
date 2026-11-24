# Nathan Game Palembang — Admin Dashboard & Catalog CMS (`ngp-sys`) 🛠️🎮

![HTML5](https://img.shields.io/badge/HTML5-Single_File_Panel-E34F26?style=flat-square&logo=html5&logoColor=white)
![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-CDN-06B6D4?style=flat-square&logo=tailwindcss&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-Vanilla_ES6+-F7DF1E?style=flat-square&logo=javascript&logoColor=black)
![Google Apps Script](https://img.shields.io/badge/Backend-Google_Apps_Script-4285F4?style=flat-square&logo=google&logoColor=white)

The companion **Admin Dashboard & Headless CMS Panel** for the **[Nathan Game Palembang Public Catalog](https://masvoorii.github.io)**. Built as a zero-build single-page web panel backed by **Google Apps Script**, **Google Sheets**, and **Google Drive**, it enables PIN-authenticated catalog management, automated cover art scraping, client-side image compression, and dynamic platform configuration.

---

### ✨ Key Features

- **🔒 PIN Lock Screen & Session Auth:** Protects all write operations (`add`, `edit`, `delete`, `uploadCover`, `updateWA`) via server-side PIN verification and `sessionStorage` state persistence.
- **🔍 Automated Cover Art & Metadata Scraper:** Searches **Wikidata**, **Wikimedia Commons**, and **Wikipedia APIs** to automatically fetch official game titles and vertical cover art—complete with smart poster fallback.
- **📤 Client-Side Image Compression & Google Drive Upload:** Resizes custom cover uploads (`max-width: 600px`, JPEG quality `0.88`) in the browser using HTML5 `<canvas>` before encoding to Base64 and uploading directly to Google Drive via Apps Script.
- **📦 Full Inventory CRUD & Dynamic Sorting:** Create, update, filter, and delete catalog entries with instant sorting by **Newest**, **Oldest**, **Alphabetical (A–Z / Z–A)**, or **File Size (Smallest / Largest)**.
- **⚙️ Dynamic Platform & WhatsApp Settings:** Add or remove console platforms (`PS4`, `PS2 Classic`, `Switch`, etc.) and update the active customer checkout WhatsApp number on the fly.

---

### 🛠️ Tech Stack

- **Frontend:** Semantic HTML5, Vanilla JavaScript (ES6+), Tailwind CSS
- **Serverless Backend & Storage:** Google Apps Script (REST Webhook), Google Sheets (Database), Google Drive (Cover Hosting)
- **External Metadata APIs:** Wikidata API, Wikimedia Commons, Wikipedia Action API

---

### 🚀 Local Usage

1. **Clone the repository:**
   ```bash
   git clone https://github.com/masvoorii/ngp-sys.git
   cd ngp-sys
   ```

2. **Configure API Endpoint:**
   Ensure `API_URL` in `index.html` points to your deployed Google Apps Script Web App URL.

3. **Launch the Panel:**
   Open `index.html` in any modern web browser and enter your configured Admin PIN to unlock the dashboard.
