# Panduan Deployment & Cara Penggunaan: SOS for Motor Riders

## Step 1: Deploy BackEnd Google Apps Script (GAS)
1. Buka [Google Sheets](https://sheets.google.com) dan buat dokumen baru bernama `Database SOS Riders`.
2. Klik **Extensions > Apps Script**.
3. Hapus kode bawaan di `Code.gs` dan salin seluruh isi dari file **`Code.gs`** di atas.
4. Sesuaikan `TELEGRAM_BOT_TOKEN` dan `TELEGRAM_CHAT_ID` pada objek `CONFIG` di bagian atas file.
5. Klik **Deploy > New Deployment**. Pilih tipe **Web App**.
6. Set **Execute as**: `Me`, dan **Who has access**: `Anyone`.
7. Klik **Deploy** dan salin **Web App URL** yang didapat.

## Step 2: Deploy FrontEnd ke GitHub Pages
1. Buat repository baru di GitHub (misal: `sos-motor-riders`).
2. Upload file **`index.html`**, **`manifest.json`**, dan **`sw.js`** ke dalam repository tersebut.
3. Masuk ke menu **Settings > Pages** pada repository GitHub Anda.
4. Pada opsi **Branch**, pilih `main` / `master` lalu klik **Save**.
5. Tunggu hingga tautan GitHub Pages Anda aktif (misal: `https://username.github.io/sos-motor-riders/`).

## Step 3: Generator Kode C++ ESP32 via Dashboard
1. Buka Web App GitHub Pages yang sudah dipublikasikan.
2. Klik tombol **ESP32 Config Generator** di pojok kanan atas.
3. Masukkan **URL Web App GAS** yang disalin pada Step 1.
4. Isikan nama **Wi-Fi SSID** dan **Password** tempat ESP32 akan terhubung.
5. Klik **Generate Kode C++ Firmware** lalu tekan **Salin Kode**.
6. Buka **Arduino IDE**, paste kode tersebut, dan upload langsung ke ESP32 Anda.