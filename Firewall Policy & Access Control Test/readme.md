# Firewall Policy & Access Control

Repositori ini berisi simulasi **Firewall** menggunakan Cisco Packet Tracer. Proyek ini bertujuan untuk memvalidasi kebijakan keamanan jaringan dalam melindungi aset kritikal (Server) dari akses tidak sah.

## 🛡️ Konsep Keamanan (Firewall)
Simulasi ini menerapkan fungsi **Packet Filtering Firewall** pada Layer 3. Router dikonfigurasi sebagai garda terdepan (Perimeter Defense) untuk menyaring lalu lintas data berdasarkan kebijakan akses perusahaan.

### Target Keamanan:
*   **Aset Kritikal**: `Server AD-DC` (Active Directory - Domain Controller).
*   **Tujuan**: Memastikan hanya pengguna internal yang sah (`IT-Admin` & `Staff`) yang dapat mengakses server, sementara entitas luar (`Hacker`) diblokir sepenuhnya.

## 🧪 Skenario Pengujian (Test Case)

Pengujian dilakukan dengan metode *Connectivity* (Ping/ICMP) untuk memverifikasi efektivitas **Access Control List (ACL)** yang diterapkan pada Router R1.


| Test ID | Source Device | Target Device | Expected Result | Actual Result | Status |
| :--- | :--- | :--- | :--- | :--- | :--- |
| TC-01 | IT-Admin | Server AD-DC | Connection Permitted | Reply Received | **PASSED** |
| TC-02 | Staff | Server AD-DC | Connection Permitted | Reply Received | **PASSED** |
| TC-03 | Hacker PC | Server AD-DC | **Connection Denied** | Destination Host Unreachable | **PASSED** |

## 🛠️ Detail Implementasi
Kebijakan firewall ini mengacu pada standar **ISO 27001 Control A.9 (Access Control)**:
*   **Identity-Based Filtering**: Pemblokiran dilakukan berdasarkan identitas IP Address perangkat yang dianggap sebagai ancaman.
*   **Inbound Filtering**: Router memeriksa setiap paket yang masuk dari arah jaringan luar sebelum diizinkan menyentuh area server internal.

## 📂 Cara Verifikasi Manual
1. Jalankan simulasi pada file `.pkt`.
2. Buka terminal pada `Hacker Tes Deny Server`.
3. Lakukan pengujian ping ke IP Server.
4. Hasil pengujian akan menunjukkan bahwa paket di-*drop* oleh Router (Firewall), membuktikan kebijakan keamanan telah aktif.

---
*Project ini dikembangkan sebagai bukti kompetensi dalam Network Security & Firewall Configuration.*

