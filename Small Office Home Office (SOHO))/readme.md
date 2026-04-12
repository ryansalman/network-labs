# Inter-VLAN Routing Simulation (Router-on-a-Stick)

Proyek ini mensimulasikan infrastruktur jaringan kantor tiga lantai dengan segmentasi jaringan menggunakan **VLAN** dan **Inter-VLAN Routing** menggunakan metode **Router-on-a-Stick** di Cisco Packet Tracer.

## 📋 Fitur Utama
*   **Network Segmentation**: Memisahkan traffic antar departemen (Admin, Marketing, Financial) untuk meningkatkan performa dan keamanan.
*   **Inter-VLAN Routing**: Memungkinkan komunikasi antar-VLAN melalui sub-interface pada Router Utama.
*   **DHCP Server**: Alokasi IP Address secara dinamis untuk semua end-device (PC, Laptop, Printer).
*   **Wireless Connectivity**: Akses jaringan nirkabel untuk pengguna laptop di setiap lantai.

## 🏗️ Topologi Jaringan
![Topology Diagram]([link-foto-screenshot-kamu-disini.png](https://github.com/ryansalman/network-labs/blob/6c148b07f61e003515978f29e2b002ea6d0ad921/Small%20Office%20Home%20Office%20(SOHO))/SOHO.png))

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

