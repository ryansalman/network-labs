# Firewall Policy & Access Control Test

## 🚀 Gambaran Proyek
Proyek ini mensimulasikan skenario **Real-World Attack Vector** di mana kontrol akses administratif (RBAC) gagal, namun aset kritikal tetap aman berkat lapisan pertahanan ganda (**Dual-Layer Defense**).

## 🖼️ Network Topology
<img width="827" height="417" alt="Role-Based Access Control and Active Directory" src="https://github.com/user-attachments/assets/9a6106a5-a102-4a0f-b67b-03146c380673" />

## 🛡️ Keamanan Berlapis (Dual-Layer Defense)
Dalam lab ini, saya menguji ketahanan jaringan terhadap skenario pencurian kredensial (*Stolen Credentials*):
1.  **Layer 1 (CLI RBAC)**: Mengatur hak akses command-line (Privilege levels).
2.  **Layer 2 (Network ACL)**: Mengatur izin akses antar-perangkat di jaringan.

## ⚠️ Skenario Serangan: "CLI Takeover"
*   **Insiden**: Hacker mendapatkan kredensial Admin (Priv 15) di VLAN Staff.
*   **Dampak**: Hacker berhasil masuk ke CLI Router (**Full Config Exposed**).
*   **Pertahanan**: Meskipun menguasai Router, Hacker tetap **GAGAL** mengakses **Server AD-DC** karena diblokir oleh Network ACL.

## 🧪 Hasil Simulasi (Proof of Concept)


| Skenario Pengujian | Hasil CLI | Akses ke Server | Status Keamanan |
| :--- | :--- | :--- | :--- |
| **Legit Admin** | Full Access | ✅ Allowed | **Secure** |
| **Legit Staff** | Limited Access | ❌ Blocked | **Secure** |
| **Hacker (Stolen Creds)** | **Full Takeover** ⚠️ | ❌ **Blocked** ✅ | **Mitigated** |

> **Lesson Learned:** *"CLI Access ≠ Network Access"*. Pertahanan berlapis mencegah *Total Compromise*.

---
*Dibuat untuk portofolio Network Security Engineer.*
