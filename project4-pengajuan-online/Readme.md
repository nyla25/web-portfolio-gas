# Sistem Pengajuan Online
Aplikasi web sederhana berbasis Google Apps Script untuk pengajuan izin mahasiswa.
## Fitur
- Login mahasiswa menggunakan NIM (BigQuery)
- Submit pengajuan izin
- Riwayat pengajuan realtime
- Notifikasi sukses/gagal
- Tanpa database server (hemat biaya)
## Arsitektur
- **Login**: BigQuery
- **Insert & Riwayat**: Google Sheets
- **Frontend**: HTML + JS (Apps Script)
## Struktur Data
## Demo
https://script.google.com/macros/s/AKfycbzk4V0L-1l1zv7RAyIodFStoLeY0UZ__ta9WlSZ1uweZGqor7Bhd5ZtMuYBPH5fDFtdHA/exec
### BigQuery
Dataset: `app_pengajuan`
Table: `data_mahasiswa`
| Field | Type |
|-----|-----|
| nim | INTEGER |
| nama | STRING |
| prodi | STRING |
### Google Sheet
Sheet: `data_pengajuan`
| Kolom |
|------|
| id |
| nim |
| jenis |
| keterangan |
| status |
| created_at |
## Konfigurasi
Edit di `Code.gs`:
```js
const PROJECT_ID = 'project-id-anda';
const DATASET_ID = 'app_pengajuan';
const SPREADSHEET_ID = 'spreadsheet-id';
