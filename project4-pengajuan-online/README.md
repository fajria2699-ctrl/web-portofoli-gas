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
### BigQuery
Dataset: `app_pengajuan2`
Table: `data_mahasiswa`
| Field | Type |
|-----|-----|
| nim | INTEGER |
| nama | STRING |
| prodi | STRING |

https://script.google.com/macros/s/AKfycbwO8ps_zfmrF8EfE5xwMO3agQISGaoUTotESEyYgmPvvBEFpMSqJwSgMn8GuZCe5ACW/exec

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
Edit di `Kode.gs`:
```js
const PROJECT_ID = 'project-id-anda';
const DATASET_ID = 'app_pengajuan';
const SPREADSHEET_ID = 'spreadsheet-id';
