# GitHub Actions Windows RDP + MCSManager

Repository ini menyediakan **dua workflow RDP Windows berbasis GitHub Actions**.

Salah satu workflow **khusus untuk setup MCSManager + Java 21** sehingga **panel web bisa dibuka dari HP**.

---

## 🔹 Workflow 1 — RDP Basic

**Nama:** `RDP`

### Fungsi
- Akses RDP Windows
- Cocok untuk debugging manual
- Tidak ada panel web

---

## 🔹 Workflow 2 — RDP + MCSManager Panel

**Nama:** `RDP + MCSManager Panel`

### Fungsi
- RDP Windows
- Install Java 21
- Download & menjalankan MCSManager
- Web panel bisa diakses via HP
- Akses aman via Tailscale

---

## 🔐 Persyaratan

Tambahkan GitHub Secret:

| Name | Value |
|-----|------|
| `TAILSCALE_AUTH_KEY` | Auth Key dari Tailscale |

---

## 🖥️ Akses RDP

- IP       : `Tailscale IP`
- Username : `Skyro`
- Password : lihat log workflow

---

## 🌐 Akses Web MCSManager (HP)

Pastikan HP sudah login ke Tailscale.
Panel akan muncul otomatis setelah workflow berjalan.

---

## ☕ Java

- Java 21 (Temurin / setara Oracle)
- Siap untuk Minecraft server modern

---

## ⚠️ Catatan Penting

- GitHub Actions **bukan VPS**
- Runtime terbatas
- Semua data hilang setelah workflow berhenti
- Gunakan hanya untuk testing / edukasi

---

## Rekomendasi

| Kebutuhan | Workflow |
|---------|---------|
| RDP saja | Workflow 1 |
| Panel MC + HP | Workflow 2 |

---

## Disclaimer

Digunakan untuk edukasi & eksperimen teknis.
