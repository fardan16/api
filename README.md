# Praktikum 7 — Dokumentasi OpenAPI dan Pengujian API dengan Postman (Baseline)

## Deskripsi
Praktikum ini menyatukan dua pilar penting rekayasa API standar industri:
1. **Dokumentasi Terstruktur**: Menulis spesifikasi kontrak API menggunakan format **OpenAPI 3.0.3 (YAML)** yang memuat endpoint `/login`, `/v2/destinations`, `/v2/destinations/{id}`, `/v1/destinations` (deprecated), security schemes (API Key & Bearer JWT), dan skema komponen.
2. **Automated Testing**: Menyusun 8 test case otomatis di Postman (TC1 s.d. TC8) menggunakan `pm.test()`, verifikasi status code, header `Location`, body skema JSON, serta pengujian terangkai (*chaining*) token dan ID melalui Collection Runner.

## Berkas Praktikum
* `server.js`: Server API lengkap dari Praktikum 6.
* `openapi.yaml`: Kontrak formal OpenAPI 3.0.3.
* `Praktikum_7_Automated_Testing.postman_collection.json`: Koleksi Postman dengan skrip assertions otomatis.

## Cara Menjalankan
1. Jalankan server:
   ```bash
   node --watch --env-file=.env server.js
   ```
2. Buka Swagger Editor di browser (`https://editor.swagger.io`) dan tempel isi `openapi.yaml` untuk memverifikasi dokumentasi interaktif.
3. Import koleksi `Praktikum_7_Automated_Testing.postman_collection.json` ke Postman dan jalankan via **Collection Runner** (13 assertions lolos 100%).
