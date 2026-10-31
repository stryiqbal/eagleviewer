# Myth Atlas — Eagle Viewer

Panduan lapangan interaktif untuk melihat model 3D Eagle di browser. Halaman dibuat dengan HTML, CSS, JavaScript modules, dan Three.js.

## Isi Proyek

- `index.html` — halaman dan logika viewer 3D.
- `Eagle.glb` — model Eagle yang dimuat oleh Three.js.
- `Eagle.png` — gambar thumbnail pada kartu dan tab.

Jaga nama file dan huruf besar-kecilnya tetap sama, serta letakkan aset di folder yang sama dengan `index.html`.

## Menjalankan Secara Lokal

Jangan buka `index.html` langsung dengan alamat `file://`. Jalankan server HTTP lokal dari folder proyek:

```powershell
py -m http.server 8000
```

Lalu buka [http://127.0.0.1:8000/](http://127.0.0.1:8000/) di browser. Biarkan terminal server tetap berjalan selama halaman digunakan.

Jika perintah `py` tidak tersedia, gunakan:

```powershell
python -m http.server 8000
```

## Kontrol Viewer

- Seret model untuk memutar.
- Gunakan roda mouse untuk zoom.
- Klik tombol zoom, expand, dan pencahayaan pada toolbar.
- Gunakan tombol panah kiri, `360°`, dan panah kanan untuk memutar model.
- Klik dua kali pada viewer atau tekan `0` untuk mengembalikan posisi dan zoom.
- Tekan `+` atau `=` untuk memperbesar, `-` untuk memperkecil, dan `Esc` untuk keluar dari mode expand.

## Teknologi dan Koneksi

Tidak diperlukan proses build atau instalasi package. Halaman mengambil Three.js, font, dan decoder Draco dari CDN, sehingga browser memerlukan koneksi internet. Model dan thumbnail dimuat dari file lokal di repositori.

## Deploy ke GitHub Pages

Push `index.html`, `Eagle.glb`, dan `Eagle.png` dalam folder yang sama. Aktifkan GitHub Pages pada branch dan folder yang berisi ketiga file tersebut. Buka URL GitHub Pages setelah deploy; jangan gunakan alamat `127.0.0.1` untuk situs publik.
