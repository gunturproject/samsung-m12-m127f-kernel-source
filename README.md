# Samsung Galaxy M12 SM-M127F — Kernel Source

Repositori ini berisi pohon sumber kernel Samsung untuk Galaxy M12 **SM-M127F**, beserta sumber platform yang disertakan dalam paket Samsung Android 13.

Samsung Open Source mencantumkan firmware **M127FXXS9DXJ1** dan **M127FXXS9DXJ3** pada entri sumber yang sama, dengan berkas `SM-M127F_13_Opensource.zip`. Paket yang menjadi dasar repo ini memiliki nama tersebut. Rincian asal, cakupan, dan checksum ada di [`SOURCE_PROVENANCE.md`](SOURCE_PROVENANCE.md) dan [`CHECKSUMS.sha256`](CHECKSUMS.sha256).

## Isi repo

- Direktori akar: pohon sumber kernel Samsung (`Kernel.tar.gz` dari paket sudah diekstrak).
- [`platform/`](platform/): sumber modul/komponen platform Android yang juga disertakan Samsung (`Platform.tar.gz` sudah diekstrak).
- [`README_Kernel.txt`](README_Kernel.txt) dan [`README_Platform.txt`](README_Platform.txt): petunjuk build dari paket Samsung.

Repositori juga menyimpan ZIP sumber asli sebagai aset pada halaman [GitHub Releases](https://github.com/gunturproject/samsung-m12-m127f-kernel-source/releases), agar salinan arsip vendor tetap tersedia tanpa menaruh berkas biner besar di riwayat Git.

## Build kernel

Instruksi dari Samsung meminta toolchain AArch64 GCC dan Clang yang sesuai, lalu:

```sh
export PLATFORM_VERSION=13
export ARCH=arm64
make exynos850-m12nsxx_defconfig
make
```

Image keluaran disebut sebagai `arch/arm64/boot/Image`; modul kernel berada di `drivers/*/*.ko`. Rujuk [`README_Kernel.txt`](README_Kernel.txt) untuk detail toolchain. Toolchain dan Android build tree tidak disertakan di repo ini. Build belum dijalankan sebagai bagian dari penyiapan repo.

## Lisensi

Sumber ini memuat beberapa komponen dan lisensi. Pertahankan pemberitahuan lisensi yang ada pada berkas sumber, termasuk `COPYING` dan direktori `LICENSES/`, dan periksa lisensi tiap komponen sebelum redistribusi atau penggunaan. Syarat unduhan Samsung tidak menggantikan lisensi yang menyertai source code.
