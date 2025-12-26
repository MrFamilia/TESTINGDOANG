# GitHub Actions Windows RDP via Tailscale

Repository ini menyediakan workflow GitHub Actions untuk membuat akses **Remote Desktop Protocol (RDP)** ke runner Windows secara aman menggunakan **Tailscale**.

Workflow ini cocok untuk:
- Debugging aplikasi Windows
- Pengujian GUI
- Eksperimen environment Windows sementara

---

## Fitur

- Windows runner (`windows-latest`)
- RDP otomatis aktif
- Pembuatan user administrator lokal
- Password acak dengan keamanan tinggi
- Akses privat menggunakan Tailscale
- Koneksi dipertahankan hingga workflow dihentikan manual

---

## Cara Kerja

1. Workflow dijalankan manual (`workflow_dispatch`)
2. RDP diaktifkan dan firewall port `3389` dibuka
3. User lokal `Skyro` dibuat dengan password acak
4. Tailscale di-install dan dihubungkan ke network privat
5. IP Tailscale ditampilkan
6. Koneksi RDP diverifikasi
7. Runner dijaga tetap aktif

---

## Persyaratan

### Akun Tailscale
Wajib memiliki akun Tailscale aktif.

### GitHub Secret
Tambahkan secret berikut di repository:

- **Name:** `TAILSCALE_AUTH_KEY`
- **Value:** Auth Key dari dashboard Tailscale

---

## Informasi Login RDP

Saat workflow berjalan, detail login akan muncul di log:
