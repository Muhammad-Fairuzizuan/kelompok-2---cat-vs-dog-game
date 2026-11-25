# Cat vs Dog – Bone Battle

Game artileri satu pemain untuk Kelompok 2. Buka CatVsDog.capx di Construct 2 r280 Free Edition, pilih L_MainMenu, lalu tekan F5.

## Bermain dari hasil ekspor

Ekstrak paket ZIP. Buka terminal di direktori yang berisi README ini dan jalankan:

```powershell
python -m http.server 8000 --bind 127.0.0.1 --directory HTML5
```

Buka http://127.0.0.1:8000 di browser desktop. Server lokal hanya membutuhkan Python dan dapat dihentikan dengan Ctrl+C.

## Kontrol

Klik Play, pilih kartu Cat atau Dog, lalu klik Start Battle. Gerakkan mouse ke atas dan ke arah lawan, tahan tombol kiri untuk mengisi daya, lalu lepaskan. Sebagai percobaan pertama saat angin tenang, gunakan sudut sekitar 45° dan daya 73%. Lima lemparan tepat sasaran menghabiskan 100 HP.

## Isi paket

- CatVsDog.capx berisi proyek yang dapat diedit beserta semua aset runtime.
- HTML5 berisi ekspor asli editor dengan jalur aset relatif.
- assets memuat master SVG, PNG dan audio.
- screenshots memuat tangkapan canvas saat hasil ekspor dijalankan.
- GAME_DESIGN, EVENT_SHEET_GUIDE, ASSET_MANIFEST dan TEST_REPORT mendokumentasikan desain, implementasi, aset dan pengujian.
