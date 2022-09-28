Halftoning
===============

Halftoning atau halftoning analog adalah proses yang mensimulasikan nuansa abu-abu dengan memvariasikan ukuran titik-titik hitam kecil yang diatur dalam pola yang teratur. Teknik ini digunakan dalam printer, serta industri penerbitan. Jika Anda memeriksa sebuah foto di koran, Anda akan melihat bahwa gambar itu terdiri dari titik-titik hitam meskipun tampaknya terdiri dari abu-abu. Hal ini dimungkinkan karena integrasi spasial yang dilakukan oleh mata kita. Mata kita memadukan detail halus dan merekam intensitas keseluruhan. Halftoning digital mirip dengan halftoning di mana gambar didekomposisi menjadi kotak sel halftone. Elemen (atau titik yang digunakan halftoning dalam mensimulasikan nuansa abu-abu) dari sebuah gambar disimulasikan dengan mengisi sel halftone yang sesuai. Semakin banyak jumlah titik hitam dalam sel halftone, semakin gelap sel tersebut. Misalnya, pada Gambar 1.1, sebuah titik kecil yang terletak di tengah disimulasikan dalam halftoning digital dengan mengisi sel halftone tengah; demikian juga, titik ukuran sedang yang terletak di sudut kiri atas disimulasikan dengan mengisi empat sel di sudut kiri atas. Titik besar yang menutupi sebagian besar area pada gambar ketiga disimulasikan dengan mengisi semua sel halftone.

![Digital Halftoning](https://user-images.githubusercontent.com/112601193/192878147-995d1e16-e433-4743-afcb-d13917a87a42.jpeg)
Gambar 1.1 Digital Halftoning 

Tiga metode umum untuk menghasilkan gambar halftoning digital adalah:
- Petterning
- Dithering
- Error Diffusion

Patterning
===============
Pola adalah yang paling sederhana dari tiga teknik untuk menghasilkan gambar halftoning digital. Ini menghasilkan gambar yang memiliki resolusi spasial lebih tinggi daripada gambar sumber. Jumlah sel halftone citra keluaran sama dengan jumlah piksel citra sumber. Namun, setiap sel halftone dibagi lagi menjadi kotak 4x4. Setiap nilai piksel input diwakili oleh jumlah kotak terisi yang berbeda dalam sel halftone. Karena kisi 4x4 hanya dapat mewakili 17 tingkat intensitas yang berbeda, gambar sumber harus dikuantisasi. Gambar 1.2 menunjukkan matriks pola rekursif Rylander, yang akan digunakan dalam daftar 1.1, dan contoh operasi pola.

![Rylander's recursive patterning matrices](https://user-images.githubusercontent.com/112601193/192879921-4767cfc8-27a5-4918-988f-7f516381b5b6.jpeg)
Gambar 1.2 Rylander's recursive patterning matrices 
![The Patterning operation](https://user-images.githubusercontent.com/112601193/192880659-28a63569-21a9-4079-aeaa-68e84f94cc63.jpeg)
Gambar 1.3 The Patterning operation

Dithering
===============
Teknik lain yang digunakan untuk menghasilkan gambar halftoning digital adalah dithering. Tidak seperti pola, dithering membuat gambar keluaran dengan jumlah titik yang sama dengan jumlah piksel pada gambar sumber. Dithering dapat dianggap sebagai thresholding gambar sumber dengan matriks gentar. Matriks diletakkan berulang kali di atas gambar sumber. Dimanapun nilai piksel gambar lebih besar dari nilai dalam matriks, titik pada gambar output diisi. Masalah dithering yang terkenal adalah menghasilkan artefak pola yang diperkenalkan oleh matriks ambang batas tetap. Gambar 1.4 menunjukkan contoh operasi dithering.

![The dithering operation](https://user-images.githubusercontent.com/112601193/192881300-e81abd99-47b9-45f5-838f-00b7e9e6b1cc.jpeg)
Gambar 1.4 The dithering operation
