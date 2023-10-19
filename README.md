# Photocell (Light Dependent Resistor) Library for Arduino

## Apa itu?

Pustaka ini (dengan contoh) dirancang untuk diintegrasikan dalam proyek-proyek menggunakan segala jenis fotosel untuk mengambil intensitas cahaya (dalam Lux atau footcandles). Ini menangani seri fotosel GL55xx tetapi fotosel lainnya juga dapat dikonfigurasi juga.

## Cara menginstall

1. Unduh terbaru https://github.com/QuentinCG/Arduino-Light-Dependent-Resistor-Library/releases
2. Pada Arduino IDE Anda, klik menu "Sketch" dan kemudian "Include Library > Add .ZIP Libraries"
3. Anda sekarang dapat menggunakan pustaka untuk projek Anda atau meluncurkan contoh ("Contoh File >")

## Cara mengbungkan photocell ke Arduino kita

Anda memerlukan resistor selain sensor untuk membuat "jembatan tegangan". Tegangan yang dibutuhkan dapat berupa 5V atau 3.3V.

## Contoh

Salah satu contoh disediakan dengan perpustakaan ini:

## Menunjukkan intensitas cahaya setiap detik dengan GL5528 photocell.
https://github.com/QuentinCG/Arduino-Light-Dependent-Resistor-Library/blob/master/examples/GL5528BasicExample/GL5528BasicExample.ino

## Cara menggunakan library

## Memakai GL55xx photocells

Jika fotosel Anda berada dalam seri GL55x, Anda hanya perlu menginisialisasi kelas fotosel dengan elemen yang tepat:

Photocell	    Dan     Init value
- GL5516	          LightDependentResistor::GL5516
- GL5528	          LightDependentResistor::GL5528
- GL5537-1	        LightDependentResistor::GL5537_1
- GL5537-2	        LightDependentResistor::GL5537_2
- GL5539           	LightDependentResistor::GL5539
- GL5549	          LightDependentResistor::GL5549

## Dengan photocell yang lain

Untuk menggunakan fotosel lain, Anda harus menyediakan perpustakaan kurva semacam ini: I[lux]=constant_1/(R[Ω]^constant_2).

Sebagian besar waktu, kurva adalah kurva logaritmik yang berarti Anda harus mengubah dan menyelesaikan persamaan Link: https://github.com/QuentinCG/Arduino-Light-Dependent-Resistor-Library/blob/master/LightDependentResistor.h#L67. 

Penjelasan lengkap tentang cara melakukannya langkah demi langkah ditampilkan di file header. Anda juga akan menemukan bagaimana persamaan GL55xx diselesaikan di lembar Excel Link: https://github.com/QuentinCG/Arduino-Light-Dependent-Resistor-Library/blob/master/doc/GL55_calculation.xls.

## Lisensi

Proyek ini berada di bawah lisensi MIT. Ini berarti Anda dapat menggunakannya sesuai keinginan (hanya saja, jangan hapus header pustaka).
