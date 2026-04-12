# Inter-VLAN Routing Simulation (Router-on-a-Stick)

Proyek ini mensimulasikan infrastruktur jaringan kantor tiga lantai dengan segmentasi jaringan menggunakan **VLAN** dan **Inter-VLAN Routing** menggunakan metode **Router-on-a-Stick** di Cisco Packet Tracer.

## 📋 Fitur Utama
*   **Network Segmentation**: Memisahkan traffic antar departemen (Admin, Marketing, Financial) untuk meningkatkan performa dan keamanan.
*   **Inter-VLAN Routing**: Memungkinkan komunikasi antar-VLAN melalui sub-interface pada Router Utama.
*   **DHCP Server**: Alokasi IP Address secara dinamis untuk semua end-device (PC, Laptop, Printer).
*   **Wireless Connectivity**: Akses jaringan nirkabel untuk pengguna laptop di setiap lantai.

## 🏗️ Topologi Jaringan
<img width="967" height="472" alt="SOHO" src="https://github.com/user-attachments/assets/72504b3e-0396-41eb-9201-d748eda5f0e2" />

## 🛠️ Detail Konfigurasi

| Dept / Floor | VLAN ID | Network Subnet | Gateway |
| :--- | :--- | :--- | :--- |
| Admin (Floor 1) | 10 | 192.168.10.0/24 | 192.168.10.1 |
| Marketing (Floor 2) | 20 | 192.168.20.0/24 | 192.168.20.1 |
| Financial (Floor 3) | 30 | 192.168.30.0/24 | 192.168.30.1 |

## 🛡️ Standar Keamanan (ISO 27001 Compliance)
Simulasi ini menerapkan prinsip **ISO 27001 Control A.13.1.1 (Network Segmentation)**. Dengan memisahkan departemen ke dalam VLAN yang berbeda, risiko penyebaran ancaman (seperti malware) antar divisi dapat diminimalisir, serta memudahkan penerapan kebijakan akses (Access Control) terpusat pada router.

## 🚀 Cara Menjalankan
1. Download file `topology.pkt` di repositori ini.
2. Buka menggunakan **Cisco Packet Tracer** (versi terbaru direkomendasikan).
3. Tunggu hingga semua indikator port berwarna hijau.
4. Lakukan pengujian ping antar perangkat di VLAN yang berbeda.

