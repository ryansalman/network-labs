# Firewall Policy & Access Control Test

## 🏗️ Topologi Jaringan
<img width="827" height="417" alt="Role-Based Access Control and Active Directory" src="https://github.com/user-attachments/assets/e97e7eed-3cdd-48c8-bbc5-05e6023a64e1" />

## 🚀 Ringkasan Proyek
Proyek ini memvalidasi efektivitas kebijakan **Firewall (ACL)** dan **Access Control (RBAC)** dalam menghadapi skenario serangan nyata. Fokus utamanya adalah membuktikan bahwa pertahanan berlapis (*Defense-in-Depth*) dapat mencegah kegagalan total sistem meskipun kredensial admin telah dikompromi.

## ⚠️ Skenario Pengujian: "The Hacker Analysis"
Simulasi ini menggunakan pendekatan **RBAC Failure Mode Analysis**:
1. **Insiden**: Hacker di VLAN Staff berhasil mencuri kredensial admin (`admin/Admin123`).
2. **Eskalasi**: Hacker mendapatkan akses **Privilege 15 (Full CLI)** ke Router Utama (R1).
3. **Hasil Akhir**: Meskipun konfigurasi router terekspos, akses ke **Server AD-DC** tetap **GAGAL (Blocked)** karena proteksi pada lapisan Network ACL.

## 🧪 Tabel Verifikasi Keamanan



| Entitas | Hak Akses CLI | Akses ke Server | Hasil Uji |
| :--- | :--- | :--- | :--- |
| **Legit IT-Admin** | Full Access | ✅ Allowed | **PASSED** |
| **Legit Staff** | Limited Access | ❌ Blocked | **PASSED** |
| **Hacker (Stolen Credentials)** | **Full Takeover** ⚠️ | ❌ **Blocked** ✅ | **MITIGATED** |

## 🛡️ Kesimpulan Strategis
> **"CLI Takeover ≠ Total Compromise"**
> Pengujian ini membuktikan bahwa pemisahan antara **Manajemen Akses (RBAC)** dan **Kontrol Jaringan (ACL)** sangat krusial. Keamanan data server tetap terjaga berkat *Network Level Blocking* meskipun pertahanan di level *Administrative Access* telah ditembus.

---
*Dibuat untuk portofolio Network Security Engineer.*
