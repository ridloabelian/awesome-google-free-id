<div align="center">

<img src="https://www.gstatic.com/devrel-devsite/prod/v0e0f589edd85502a40d78d7d0825db8ea5ef3b99ab4070381ee86977c9168730/cloud/images/cloud-logo.svg" alt="Google Logo" width="280" />

<h1 align="center">Kitab Google ✨ 🇮🇩<br><sub>(Stack Nol Rupiah)</sub></h1>

<p align="center">
  <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=500&size=20&pause=1000&color=4285F4&center=true&vCenter=true&width=600&lines=Bangun+SaaS+Modal+Rp+0;Apps+Script+%3D+Backend+Gratis;Sheets+%3D+Database+Gratis;Automasi+Bisnis+Tanpa+Server" alt="Typing SVG" />
</p>

Kumpulan alat, *template*, panduan, dan proyek *open-source* terbaik yang berjalan di atas ekosistem gratis Google — **Apps Script, Google Sheets, Firebase, Gemini API, dan Google Cloud Free Tier**.
Dibangun untuk membantu solopreneur, operator bisnis, dan *indie hacker* Indonesia membangun automasi, CRM, dan produk SaaS mikro dengan biaya server Rp 0.

[![Awesome](https://awesome.re/badge.svg)](https://awesome.re)
[![Stars](https://img.shields.io/github/stars/ridloabelian/awesome-google-free-id?style=flat&color=4285F4)](https://github.com/ridloabelian/awesome-google-free-id/stargazers)
[![Last Commit](https://img.shields.io/github/last-commit/ridloabelian/awesome-google-free-id?style=flat&color=4285F4)](https://github.com/ridloabelian/awesome-google-free-id/commits/main)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg?style=flat)](CONTRIBUTING.md)
[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg?style=flat)](LICENSE)

</div>

> 🔗 **Repo saudara:** Kalau Anda lebih ke *developer* dan butuh *edge/serverless*, lihat juga [**Kitab Cloudflare (awesome-cloudflare-id)**](https://github.com/ridloabelian/awesome-cloudflare-id). Ekosistem Google ini lebih cocok untuk **automasi bisnis & operator non-coder**, sedangkan Cloudflare untuk **web app skalabel**. Keduanya saling melengkapi.

Ekosistem Google punya rahasia yang jarang dimanfaatkan maksimal: **Apps Script**. Ini adalah *runtime* JavaScript gratis milik Google yang bisa jadi *backend*, *cron scheduler*, API, dan *middleware* — semuanya tanpa server, tanpa kartu kredit. Digabung dengan Sheets (database), Firebase (auth & realtime), dan Gemini (AI), Anda bisa membangun sistem bisnis lengkap dengan modal Rp 0.

**Kriteria Kurasi:**
- Berjalan di *free tier* ekosistem Google (Apps Script / Firebase Spark / GCP Free).
- Membantu automasi bisnis, SaaS, atau produktivitas.
- *Open-source* dan (idealnya) masih aktif di-*maintain*.
- Cocok untuk konteks solopreneur & UMKM Indonesia.

---

## 💰 Batas Gratis (Free Tier) Google

Kenali dulu batas gratisnya sebelum membangun. Angka di bawah adalah acuan umum akun gratis — selalu cek [kuota Apps Script](https://developers.google.com/apps-script/guides/services/quotas) dan [Firebase Pricing](https://firebase.google.com/pricing) karena kebijakan bisa berubah.

| Layanan | Batas Gratis | Catatan |
|---------|--------------|---------|
| **Apps Script** | ~20.000 eksekusi/hari, 90 menit runtime/hari | Backend, cron (*trigger*), & API gratis total. |
| **Google Sheets** | 10 juta sel/spreadsheet | Database gratis untuk data kecil-menengah. |
| **Gmail (via Apps Script)** | 100 email/hari (akun gratis), 1.500/hari (Workspace) | Untuk notifikasi & email blast ringan. |
| **Firebase Firestore** | 1 GB storage, 50rb baca & 20rb tulis/hari | NoSQL realtime database (paket Spark). |
| **Firebase Hosting** | 10 GB storage, 360 MB/hari transfer | Hosting web statis + SSL gratis. |
| **Firebase Auth** | Unlimited (email/Google), 10rb verifikasi SMS/bln | Sistem login siap pakai. |
| **Gemini API** | ~1.500 request/hari (Flash), gratis di [AI Studio](https://aistudio.google.com) | AI/LLM gratis dalam kuota harian. |
| **Google Drive** | 15 GB (dibagi dgn Gmail & Photos) | Storage + CDN gambar/file sederhana. |
| **Looker Studio** | Gratis penuh | Dashboard & visualisasi data. |
| **Google Colab** | GPU/TPU gratis (sesi terbatas) | Compute untuk eksperimen ML. |

> ⚠️ **Penting:** Firebase punya 2 paket — **Spark (gratis)** dan **Blaze (bayar per pemakaian)**. Beberapa fitur seperti *Cloud Functions* butuh Blaze (tapi tetap ada kuota gratis di dalamnya). Kuota Apps Script berbeda antara akun **Gmail gratis** vs **Google Workspace**.

---

## Daftar Isi
- [💰 Batas Gratis (Free Tier) Google](#-batas-gratis-free-tier-google)
- [🛠️ Tooling & CLI (clasp)](#️-tooling--cli-clasp)
- [🗄️ Sheets sebagai Database & API](#️-sheets-sebagai-database--api)
- [🚀 Web App & CRUD (Apps Script)](#-web-app--crud-apps-script)
- [🤖 Bot & Chat (Telegram/WA)](#-bot--chat-telegramwa)
- [🧠 AI & Gemini](#-ai--gemini)
- [🔥 Firebase (SaaS Starter)](#-firebase-saas-starter)
- [🖼️ Drive sebagai CDN & Storage](#️-drive-sebagai-cdn--storage)
- [📊 Data & Notebook (Colab)](#-data--notebook-colab)
- [📚 Referensi & Library](#-referensi--library)
- [📄 Template Siap Pakai](#-template-siap-pakai)

---

## 🛠️ Tooling & CLI (clasp)
Kembangkan Apps Script layaknya proyek modern: pakai TypeScript, Git, dan editor lokal Anda.

| Nama | Deskripsi |
|------|-----------|
| [google/clasp](https://github.com/google/clasp) ![](https://img.shields.io/github/stars/google/clasp?style=flat&label=%E2%98%85&color=4285F4) | CLI resmi Google untuk mengembangkan Apps Script dari lokal (VS Code). Mendukung *push/pull*, versioning, dan deploy. Wajib punya. |
| [howdy39/gas-clasp-starter](https://github.com/howdy39/gas-clasp-starter) ![](https://img.shields.io/github/stars/howdy39/gas-clasp-starter?style=flat&label=%E2%98%85&color=4285F4) | *Starter template* Apps Script dengan clasp yang siap pakai untuk memulai proyek dengan struktur rapi. |
| [iansan5653/gas-ts-template](https://github.com/iansan5653/gas-ts-template) ![](https://img.shields.io/github/stars/iansan5653/gas-ts-template?style=flat&label=%E2%98%85&color=4285F4) | Template untuk menulis Apps Script menggunakan TypeScript, lengkap dengan *type definitions*. |

## 🗄️ Sheets sebagai Database & API
Ubah Google Sheets menjadi database dan REST API tanpa setup server sama sekali.

| Nama | Deskripsi |
|------|-----------|
| [SteinHQ/Stein](https://github.com/SteinHQ/Stein) ![](https://img.shields.io/github/stars/SteinHQ/Stein?style=flat&label=%E2%98%85&color=4285F4) | Ubah Google Sheets menjadi REST API instan tanpa perlu *coding*. Cocok untuk *prototype*, *no-setup database*, dan aplikasi kecil. |
| [dklimok/google-apps-script-sheets-to-front-end-crud](https://github.com/dklimok/google-apps-script-sheets-to-front-end-crud) ![](https://img.shields.io/github/stars/dklimok/google-apps-script-sheets-to-front-end-crud?style=flat&label=%E2%98%85&color=4285F4) | Contoh lengkap menjadikan Sheets sebagai database dan Apps Script sebagai backend untuk *front-end* web. |
| [sanket-vekariya/GoogleAppsScriptWithFlutter](https://github.com/sanket-vekariya/GoogleAppsScriptWithFlutter) ![](https://img.shields.io/github/stars/sanket-vekariya/GoogleAppsScriptWithFlutter?style=flat&label=%E2%98%85&color=4285F4) | Operasi CRUD dasar menggunakan Apps Script (Google Sheet) sebagai backend untuk aplikasi Flutter. |

## 🚀 Web App & CRUD (Apps Script)
Bangun aplikasi web lengkap (frontend + backend) yang di-*hosting* gratis oleh Google.

| Nama | Deskripsi |
|------|-----------|
| [danielemiller/fullstack-gas-sheets-react-template](https://github.com/danielemiller/fullstack-gas-sheets-react-template) ![](https://img.shields.io/github/stars/danielemiller/fullstack-gas-sheets-react-template?style=flat&label=%E2%98%85&color=4285F4) | Template *fullstack* untuk aplikasi web: React sebagai *front-end* dan Apps Script + Sheets sebagai *backend*. |

## 🤖 Bot & Chat (Telegram/WA)
Jalankan bot Telegram/WhatsApp 24 jam gratis, ditenagai Apps Script sebagai *webhook* — tanpa VPS.

| Nama | Deskripsi |
|------|-----------|
| [telegrambotindonesia/GAS-Lib-v3](https://github.com/telegrambotindonesia/GAS-Lib-v3) ![](https://img.shields.io/github/stars/telegrambotindonesia/GAS-Lib-v3?style=flat&label=%E2%98%85&color=4285F4) | Library Apps Script untuk Telegram Bot API buatan komunitas Indonesia. Memudahkan bikin bot Telegram gratis di Apps Script. |
| [xiaomaoJT/TgBot](https://github.com/xiaomaoJT/TgBot) ![](https://img.shields.io/github/stars/xiaomaoJT/TgBot?style=flat&label=%E2%98%85&color=4285F4) | Bot Telegram fitur lengkap (manajemen grup, filter kata, query data) yang seluruhnya berjalan di Google Apps Script. |
| [sudo-eugene/Connect-Telegram-Bot-to-Google-Sheets-ChatGPT-OpenAI](https://github.com/sudo-eugene/Connect-Telegram-Bot-to-Google-Sheets-ChatGPT-OpenAI) ![](https://img.shields.io/github/stars/sudo-eugene/Connect-Telegram-Bot-to-Google-Sheets-ChatGPT-OpenAI?style=flat&label=%E2%98%85&color=4285F4) | Hubungkan Bot Telegram ke Google Sheets & OpenAI via Apps Script. Cocok untuk CRM chat & logging otomatis. |
| [abdiu34567/telesun.js](https://github.com/abdiu34567/telesun.js) ![](https://img.shields.io/github/stars/abdiu34567/telesun.js?style=flat&label=%E2%98%85&color=4285F4) | Framework Telegram Bot API modern yang didesain khusus untuk berjalan di Apps Script. |
| [ocordova/gas-telegram-bot](https://github.com/ocordova/gas-telegram-bot) ![](https://img.shields.io/github/stars/ocordova/gas-telegram-bot?style=flat&label=%E2%98%85&color=4285F4) | Contoh sederhana Bot Telegram di Apps Script yang membalas dengan kutipan acak. Bagus untuk belajar. |

## 🧠 AI & Gemini
Manfaatkan Gemini API gratis untuk automasi cerdas langsung dari dalam ekosistem Google.

| Nama | Deskripsi |
|------|-----------|
| [nghianguyen98/gemini-finance-bot](https://github.com/nghianguyen98/gemini-finance-bot) ![](https://img.shields.io/github/stars/nghianguyen98/gemini-finance-bot?style=flat&label=%E2%98%85&color=4285F4) | Pelacak keuangan pribadi berbasis AI untuk Telegram, dibangun dengan Apps Script + Gemini API + Google Sheets. Contoh *stack* Google Rp 0 yang lengkap. |
| [fabriceb/GMailAIReplier](https://github.com/fabriceb/GMailAIReplier) ![](https://img.shields.io/github/stars/fabriceb/GMailAIReplier?style=flat&label=%E2%98%85&color=4285F4) | Sekretaris AI untuk Gmail — otomatis membuat draf balasan email Anda. Kompatibel dengan Apps Script. |

## 🔥 Firebase (SaaS Starter)
Kerangka SaaS siap pakai dengan Auth, database realtime, dan hosting dari Firebase (paket Spark gratis).

| Nama | Deskripsi |
|------|-----------|
| [kefranabg/bento-starter](https://github.com/kefranabg/bento-starter) ![](https://img.shields.io/github/stars/kefranabg/bento-starter?style=flat&label=%E2%98%85&color=4285F4) | Solusi *full-stack* untuk membangun aplikasi PWA dengan cepat menggunakan Vue.js dan Firebase. |
| [CreateThrive/react-firebase-admin](https://github.com/CreateThrive/react-firebase-admin) ![](https://img.shields.io/github/stars/CreateThrive/react-firebase-admin?style=flat&label=%E2%98%85&color=4285F4) | *Starter kit* React + Firebase + Bulma untuk membangun dasbor admin yang sangat lengkap. |
| [milliorn/nextjs-firebase-starter](https://github.com/milliorn/nextjs-firebase-starter) ![](https://img.shields.io/github/stars/milliorn/nextjs-firebase-starter?style=flat&label=%E2%98%85&color=4285F4) | Template *production-ready* untuk aplikasi *full-stack* dengan Next.js dan Firebase. |
| [firebase-studio/templates](https://github.com/firebase-studio/templates) ![](https://img.shields.io/github/stars/firebase-studio/templates?style=flat&label=%E2%98%85&color=4285F4) | Pustaka *starter template* resmi dari tim Firebase Studio. |
| [iamraf/ChatApp](https://github.com/iamraf/ChatApp) ![](https://img.shields.io/github/stars/iamraf/ChatApp?style=flat&label=%E2%98%85&color=4285F4) | Aplikasi chat *open-source* yang ditenagai oleh Firebase. Contoh implementasi realtime database & auth. |

## 🖼️ Drive sebagai CDN & Storage
Manfaatkan 15 GB Google Drive sebagai penyimpanan file dan CDN gambar sederhana.

| Nama | Deskripsi |
|------|-----------|
| [tas33n/Google-drive-cdn-worker](https://github.com/tas33n/Google-drive-cdn-worker) ![](https://img.shields.io/github/stars/tas33n/Google-drive-cdn-worker?style=flat&label=%E2%98%85&color=4285F4) | Ubah Google Drive menjadi CDN cepat. Upload file via API, lalu sajikan sebagai URL publik. |
| [selcukusta/simple-image-server](https://github.com/selcukusta/simple-image-server) ![](https://img.shields.io/github/stars/selcukusta/simple-image-server?style=flat&label=%E2%98%85&color=4285F4) | Host server gambar Anda sendiri dengan pilihan penyimpanan MongoDB, Azure Blob, atau Google Drive. |

## 📊 Data & Notebook (Colab)
Compute gratis (GPU/TPU) dan koleksi notebook untuk eksperimen data & ML.

| Nama | Deskripsi |
|------|-----------|
| [amrzv/awesome-colab-notebooks](https://github.com/amrzv/awesome-colab-notebooks) ![](https://img.shields.io/github/stars/amrzv/awesome-colab-notebooks?style=flat&label=%E2%98%85&color=4285F4) | Koleksi besar notebook Google Colab untuk eksperimen cepat dan mudah di berbagai bidang. |
| [firmai/awesome-google-colab](https://github.com/firmai/awesome-google-colab) ![](https://img.shields.io/github/stars/firmai/awesome-google-colab?style=flat&label=%E2%98%85&color=4285F4) | Kurasi notebook & repositori Google Colab, banyak fokus ke data science & finance. |

## 📚 Referensi & Library
Pustaka pendukung dan referensi teknis untuk memperkuat proyek Apps Script Anda.

| Nama | Deskripsi |
|------|-----------|
| [tanaikech/DocsServiceApp](https://github.com/tanaikech/DocsServiceApp) ![](https://img.shields.io/github/stars/tanaikech/DocsServiceApp?style=flat&label=%E2%98%85&color=4285F4) | Library Apps Script canggih untuk manipulasi Google Docs, Docs API, dan Spreadsheet. Dibuat oleh Kanshi Tanaike (kontributor GAS paling produktif). |
| [oshliaer/google-apps-script-awesome-list](https://github.com/oshliaer/google-apps-script-awesome-list) ![](https://img.shields.io/github/stars/oshliaer/google-apps-script-awesome-list?style=flat&label=%E2%98%85&color=4285F4) | *Awesome list* rujukan utama (berbahasa Inggris) untuk seluruh sumber daya Google Apps Script. |

## 📄 Template Siap Pakai
Cuplikan kode Apps Script siap tempel untuk kebutuhan paling umum. Buka [script.google.com](https://script.google.com), tempel, deploy sebagai *Web App*.

### 1. Sheets sebagai REST API (GET & POST)
```javascript
// Deploy: Extensions > Apps Script > Deploy > Web App (Execute as: Me, Access: Anyone)
const SHEET_ID = 'GANTI_DENGAN_ID_SPREADSHEET';
const SHEET_NAME = 'Sheet1';

function doGet(e) {
  const sheet = SpreadsheetApp.openById(SHEET_ID).getSheetByName(SHEET_NAME);
  const data = sheet.getDataRange().getValues();
  const headers = data.shift();
  const rows = data.map(r => Object.fromEntries(headers.map((h, i) => [h, r[i]])));
  return ContentService.createTextOutput(JSON.stringify({ ok: true, data: rows }))
    .setMimeType(ContentService.MimeType.JSON);
}

function doPost(e) {
  const sheet = SpreadsheetApp.openById(SHEET_ID).getSheetByName(SHEET_NAME);
  const body = JSON.parse(e.postData.contents);
  sheet.appendRow(Object.values(body));
  return ContentService.createTextOutput(JSON.stringify({ ok: true }))
    .setMimeType(ContentService.MimeType.JSON);
}
```

### 2. Cron / Scheduler Otomatis (Time-driven Trigger)
```javascript
// Jalankan fungsi ini SEKALI untuk memasang jadwal. Setelah itu berjalan otomatis tiap hari 08:00.
function pasangJadwalHarian() {
  ScriptApp.newTrigger('tugasHarian')
    .timeBased().everyDays(1).atHour(8).create();
}

function tugasHarian() {
  // Contoh: kirim rekap harian ke email
  MailApp.sendEmail('email@anda.com', 'Rekap Harian', 'Tugas otomatis berjalan ✅');
}
```

### 3. Webhook Bot Telegram (Balas Pesan)
```javascript
const TOKEN = 'TOKEN_BOT_DARI_BOTFATHER';
const API = 'https://api.telegram.org/bot' + TOKEN;

function doPost(e) {
  const update = JSON.parse(e.postData.contents);
  const chatId = update.message.chat.id;
  const text = update.message.text || '';
  UrlFetchApp.fetch(API + '/sendMessage', {
    method: 'post',
    payload: { chat_id: chatId, text: 'Anda mengirim: ' + text }
  });
  return ContentService.createTextOutput('ok');
}

// Jalankan sekali untuk mendaftarkan webhook (ganti URL dengan URL Web App deploy Anda):
function setWebhook() {
  const url = 'URL_WEB_APP_ANDA';
  UrlFetchApp.fetch(API + '/setWebhook?url=' + encodeURIComponent(url));
}
```

### 4. Panggil Gemini API (AI) dari Apps Script
```javascript
// Dapatkan API key gratis di https://aistudio.google.com/app/apikey
const GEMINI_KEY = 'API_KEY_ANDA';

function tanyaGemini(prompt) {
  const url = 'https://generativelanguage.googleapis.com/v1beta/models/gemini-2.0-flash:generateContent?key=' + GEMINI_KEY;
  const res = UrlFetchApp.fetch(url, {
    method: 'post',
    contentType: 'application/json',
    payload: JSON.stringify({ contents: [{ parts: [{ text: prompt }] }] })
  });
  const json = JSON.parse(res.getContentText());
  return json.candidates[0].content.parts[0].text;
}

function contohPakai() {
  Logger.log(tanyaGemini('Tuliskan 1 kalimat motivasi untuk solopreneur.'));
}
```

---

## 🤝 Kontribusi
Jika Anda menemukan *tools* menarik lainnya atau sedang membangun *side project* di ekosistem Google, silakan buat *Pull Request*! Baca dulu [panduan kontribusi](CONTRIBUTING.md) kami.

<a href="https://github.com/ridloabelian/awesome-google-free-id/graphs/contributors">
  <img src="https://contrib.rocks/image?repo=ridloabelian/awesome-google-free-id" alt="Contributors" />
</a>

## 📜 Lisensi
Lisensi MIT - [Ridlo Abelian](https://github.com/ridloabelian)

---

<div align="center">

<a href="#kitab-google--">⬆️ Kembali ke Atas</a>

</div>
