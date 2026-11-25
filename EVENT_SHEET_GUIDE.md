# Panduan Event Sheet

Editor Free Edition menghitung 63 event, termasuk 11 deklarasi variabel global. XML berisi 52 blok event. Empat layout dan empat sheet memakai plugin bawaan Mouse, Audio, Text dan Sprite.

| Layout | Layer | Blok event |
|---|---|---:|
| L_MainMenu | Background, Menu | 5 |
| L_HowToPlay | Background, Guide | 5 |
| L_CharacterSelect | Background, Cards | 8 |
| L_Battle | Background, Gameplay, HUD, Overlay | 34 |

## Alur E_Battle

Phase mengendalikan satu siklus. Nilai 0 menerima bidikan, 1 mengisi daya, 2 menunggu keputusan AI, 3 membuat Bone, 4 menggerakkan Bone, 5 menyelesaikan benturan, dan 6 menampilkan hasil. Side bernilai +1 untuk Cat dan −1 untuk Dog. PlayerSide menyimpan pilihan pemain selama pindah layout.

Saat mouse dilepas, kecepatan awal diinterpolasi dari daya. Komponen horizontal adalah Side × Speed × cos(Elevation), sedangkan komponen vertikal adalah −Speed × sin(Elevation). Posisi bergerak sebesar v × dt + ½a × dt². Kecepatan kemudian bertambah sebesar a × dt. Untuk menyetel keseimbangan, buka kelompok komentar keputusan AI dan event peluncuran bersama.

Owner menghindari serangan ke diri sendiri. Benturan mengenai lawan mengurangi HP 20 dan memicu efek Pop. Benturan pagar, tanah, keluar batas dan batas umur enam detik mengakhiri lemparan. Setiap resolusi mengubah Phase sebelum proyektil dihancurkan. Setelah jeda 0,55 detik, sistem memeriksa HP, menampilkan hasil atau mengganti giliran.

## Object types

Garden, Cat, Dog, Fence, Bone, Aim, Play, Help, Back, Start, Again, Home, Panel, Card, HudPlate, Footer, Meter, Logo, Puff, CatBar, DogBar, PowerBar, Caption, PickText, CatText, DogText, WindText, TurnText, PowerText, AngleText, ResultText, Mouse, Audio
