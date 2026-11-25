# Laporan uji

Construct 2 Free Edition membuka proyek dan mengekspor HTML5. Pengujian otomatis menjalankan runtime ekspor dalam Chrome headless dengan canvas 2D. Salinan uji memasang pengendali input mouse, memajukan tick pada 60 Hz dan membaca state runtime. Uji batas memindahkan proyektil aktif ke titik tumbukan yang ditentukan. Enam PNG merekam canvas asli.

| No. | Skenario | Hasil | Bukti |
|---:|---|---|---|
| 1 | Buka proyek di Construct 2 | PASS | Editor membuka salinan byte-identik dari CAPX akhir. |
| 2 | Tampilan menu | PASS | Tangkapan 01-menu. |
| 3 | Play | PASS | Transisi ke pemilihan. |
| 4 | How to Play | PASS | Panduan dan Back. |
| 5 | Pilih Cat | PASS | PlayerSide +1. |
| 6 | Pilih Dog | PASS | PlayerSide −1. |
| 7 | Mulai dengan 100 HP | PASS | Kedua angka diperiksa saat masuk. |
| 8 | Posisi kedua karakter | PASS | Tangkapan 03-battle. |
| 9 | Pagar di tengah | PASS | Tangkapan arena dan koordinat layout. |
| 10 | Bidikan mouse | PASS | Bidikan 45° dipakai dalam uji tembak. |
| 11 | Pengisian daya | PASS | Diperiksa saat mouse ditahan. |
| 12 | Batas daya 100 | PASS | Ditahan 200 tick. |
| 13 | Cat melempar ke kanan | PASS | Damage pada Dog. |
| 14 | Dog melempar ke kiri | PASS | Damage pada Cat. |
| 15 | Percepatan gravitasi | PASS | Perubahan VY selama enam tick. |
| 16 | Angin ke kiri | PASS | Perubahan VX pada −72. |
| 17 | Angin ke kanan | PASS | Perubahan VX pada +72. |
| 18 | Tulang melewati pagar | PASS | Tembakan dari kedua sisi mencapai lawan. |
| 19 | Benturan pagar | PASS | Penempatan terkontrol di pagar. |
| 20 | Benturan tanah | PASS | Penempatan terkontrol tepat di permukaan. |
| 21 | Benturan lawan | PASS | HP lawan turun. |
| 22 | Keluar arena | PASS | Penempatan di luar batas, lalu giliran berlanjut. |
| 23 | Damage satu kali | PASS | Perubahan HP per tembakan tercatat. |
| 24 | HP minimum nol | PASS | Ronde berakhir pada nol. |
| 25 | Pembaruan bar HP | PASS | Lebar bar diverifikasi setelah damage. |
| 26 | AI melakukan lemparan | PASS | AI berpikir dan membalas. |
| 27 | AI mengenai lawan | PASS | HP pemain turun. |
| 28 | AI bisa meleset | PASS | Ronde berisi balasan tanpa damage. |
| 29 | AI menunggu giliran | PASS | Fase awal pemain dipakai selama membidik. |
| 30 | Input pemain selama giliran AI | PASS | Input saat AIThinking tidak membuat tulang. |
| 31 | Satu proyektil aktif | PASS | Klik ulang selama penerbangan. |
| 32 | Pergantian giliran | PASS | Dua ronde penuh. |
| 33 | Game over | PASS | Kedua hasil dicapai. |
| 34 | Victory | PASS | Tangkapan 05-victory. |
| 35 | Defeat | PASS | Tangkapan 06-defeat. |
| 36 | Rematch | PASS | Kedua HP kembali 100, giliran pemain. |
| 37 | Kembali ke menu | PASS | Tombol Main Menu setelah kalah. |
| 38 | Semua aset runtime | PASS | PNG didekode, OGG diperiksa, editor membuka paket revisi. |
| 39 | Batas event Free Edition | PASS | 63 pada status bar editor. |
| 40 | Batas layer | PASS | 2 / 2 / 2 / 4 dari file layout. |
| 41 | Fitur kompatibel Free Edition | PASS | Preview dan ekspor berhasil di Free Edition. |
| 42 | Ekspor dapat dimuat dari aset lokal | PASS | Chrome memuat salinan lokal hasil ekspor selama pengujian. |

## Perbaikan

Editor menolak atan2. Ekspresi diganti dengan fungsi angle bawaan. Empat OGG semula terkemas di Sounds; semuanya dipindah ke Files sesuai jalur yang diminta editor. Proyek dibuka ulang sebelum ekspor.

## Batas hasil

NOT TESTED untuk persepsi volume secara manual, sesi bermain anak usia 7–10, performa FPS pada perangkat lain, dan pemuatan ulang via cache service worker setelah server dihentikan. Uji aset lokal memakai izin akses file khusus Chrome pada salinan QA. Untuk penggunaan biasa, jalankan melalui HTTP lokal seperti pada README.
