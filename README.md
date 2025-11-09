DratVPN Proxy Config
====================

Konfigurasi Clash/OpenClash modular dan otomatis untuk routing VPN multi-negara, pemblokiran iklan, dan navigasi internet yang lebih bersih dan cepat.

Fitur Utama
-----------
- Proxy Group Dinamis: Pilih server dari berbagai negara Asia dan Amerika.
- Health Check Otomatis: Tes koneksi setiap 120 detik untuk memastikan stabilitas.
- Pemblokiran Iklan: Integrasi rule adblock dan oisd_big untuk pengalaman bebas gangguan.
- Modular Proxy Provider: Setiap negara punya sumber proxy terpisah, mudah diperbarui.
- Routing Cerdas: Grup ADS otomatis arahkan trafik iklan ke VPN atau REJECT.

Proxy Group
-----------
| Group    | Tipe     | Isi Proxy |
|----------|----------|-----------|
| DratVPN  | select   | Indonesia, Malaysia, Singapore, Thailand, Japan, Korea, India, Amerika, DIRECT |
| ADS      | select   | DratVPN, REJECT |
| Regional | url-test | Proxy dari masing-masing provider regional |

Proxy Providers
---------------
Setiap negara memiliki provider proxy yang diambil dari GitHub dan diperbarui setiap 3 jam:

- provider-id: Indonesia
- provider-my: Malaysia
- provider-sg: Singapore
- provider-th: Thailand
- provider-jp: Japan
- provider-kr: Korea
- provider-in: India
- provider-us: Amerika

Rule Providers
--------------
| Nama     | Sumber GitHub | Fungsi             |
|----------|----------------|--------------------|
| adblock  | ros3xbot       | Blokir iklan umum  |
| oisd_big | hillz2         | Blokir iklan besar |

Rules
-----
- RULE-SET,adblock,ADS
- RULE-SET,oisd_big,ADS
- MATCH,DratVPN

Instalasi
---------
1. Salin konfigurasi ini ke file config.yaml Clash/OpenClash kamu.
2. Pastikan URL provider dapat diakses dan tidak diblokir ISP.
3. Jalankan Clash/OpenClash dan pilih proxy dari grup DratVPN.

Tips Tambahan
-------------
- Gunakan url-test untuk otomatis memilih proxy tercepat.
- Tambahkan rule tambahan sesuai kebutuhan (misal: streaming, game, sosial media).
- Gunakan menu 88 untuk integrasi tema Rich preview (jika kamu pakai CLI interaktif).

Kontribusi
----------
Pull request dan issue sangat diterima! Kamu bisa bantu:
- Menambah provider baru
- Menyempurnakan rule
- Membuat dokumentasi tambahan

Lisensi
-------
MIT License. Bebas digunakan dan dimodifikasi.

Dibuat dengan ❤️ oleh komunitas open-source. Optimalkan koneksi, bersihkan iklan, dan jelajahi internet dengan kendali penuh.
