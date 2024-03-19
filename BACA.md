[![Open Source Love](https://badges.frapsoft.com/os/v1/open-source.svg?style=flat)](https://github.com/ellerbrock/open-source-badges/)
[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg?logo=github&color=%23F7DF1E)](https://opensource.org/licenses/MIT)
![GitHub last commit](https://img.shields.io/github/last-commit/devancakra/Whatsapp-Bot-based-Automatic-Fish-Monitoring-Feeding-System-using-I2C-communication-protocol)
![Project](https://img.shields.io/badge/Project-Internet%20of%20Things-light.svg?style=flat&logo=arduino&logoColor=white&color=%23F7DF1E)

# Whatsapp-Bot-based-Automatic-Fish-Monitoring-Feeding-System-using-I2C-communication-protocol
<strong>Proyek Tunggal: Sistem Pemberian Pakan Ikan Otomatis Berbasis Bot Whatsapp menggunakan protokol komunikasi I2C</strong><br><br>
Segera Hadir...

<br><br>

## Kebutuhan Proyek
| Bagian | Deskripsi |
| --- | --- |
| Papan Pengembangan | • Arduino Nano V3<br>• ESP-01 |
| Editor Kode | Visual Studio Code |
| Ekstensi | PlatformIO IDE |
| Alat Pemrogram | USB CH340-ESP01 |
| Driver | USB-Serial CH340 |
| Dukungan Aplikasi | Bot Whatsapp |
| Platform IoT | • Twilio<br>• ThingESP |
| Protokol Komunikasi | • Inter Integrated Circuit (I2C)<br>• Hypertext Transfer Protocol (HTTP) |
| Arsitektur IoT | 4 Lapisan |
| Bahasa Pemrograman | C/C++ |
| Pustaka Arduino | • Wire (default)<br>• ThingESP<br>• Servo<br>• RTClib |
| Aktuator | Servo Motor SG90 180° (x1) |
| Sensor | RTC (x1) |
| Komponen Lainnya | • Kabel USB Mini - USB tipe A (x1)<br>• Kabel jumper (1 set)<br>• Casing servo pakan ikan (x1)<br>• Botol pakan ikan (x1)<br>• Pakan ikan (1 set) |

<br><br>

## Unduh & Instal
1. Visual Studio Code

   <table><tr><td width="810">
         
   ```
   https://code.visualstudio.com/docs/?dv=win
   ```

   </td></tr></table><br>
   
2. USB-Serial CH340

   <table><tr><td width="810">
   
   ```
   https://bit.ly/CH340_Driver
   ```
   
   </td></tr></table>
   
<br><br>

## Rancangan Proyek
<table>
<tr>
<th width="420">Diagram Blok</th>
<th width="420">Infrastruktur</th>
</tr>
<tr>
<td><img src="https://github.com/devancakra/Whatsapp-Bot-based-Automatic-Fish-Monitoring-Feeding-System-using-I2C-communication-protocol/assets/54527592/d6884acf-15ce-4ef3-b1f2-4b064147806d" alt="Block-Diagram"></td>
<td><img src="https://github.com/devancakra/Whatsapp-Bot-based-Automatic-Fish-Monitoring-Feeding-System-using-I2C-communication-protocol/assets/54527592/3fae99c8-3bdc-48b9-8a3f-f3ce9aea424e" alt="Infrastructure"></td>
</tr>
</table>
<table>
<tr>
<th width="420">Diagram Ilustrasi</th>
<th width="420">Pengkabelan</th>
</tr>
<tr>
<td><img src="" alt="Pictorial-Diagram"></td>
<td><img src="" alt="Wiring"></td>
</tr>
</table>

<br><br>

## Pengetahuan Dasar
• <strong>Serial Komunikasi</strong>

Pada dasarnya, suatu perangkat itu dapat dikomunikasikan dengan perangkat lain baik secara nirkabel maupun dengan kabel. Komunikasi antar perangkat keras yang umum digunakan salah satunya adalah ``` Komunikasi Serial ```. Dapat diketahui bersama bahwa ``` Komunikasi Serial ``` ini ada tiga jenis, yaitu meliputi: ``` UART (Universal Asynchronous Receiver-Transmitter) ```, ``` SPI (Serial Peripheral Interface) ```, dan ``` I2C (Inter Integrated Circuit) ```. ``` I2C (Inter Integrated Circuit) ``` adalah standar komunikasi serial dua arah yang menggunakan dua saluran untuk mengirim data ``` (OUTPUT dari Master ke Slave) ``` dan menerima data ``` (INPUT dari Slave ke Master) ```. I2C menggunakan dua jalur dua arah: ``` Serial Data (SDA) ``` dan ``` Serial Clock (SCL) ``` untuk mentransfer data dan menyinkronkan komunikasi antar perangkat. Setiap perangkat yang terhubung ke ``` Bus I2C ``` memiliki alamat unik yang mengidentifikasinya selama komunikasi. ``` Protokol I2C ``` memungkinkan beberapa perangkat untuk berbagi bus yang sama, dan setiap perangkat dapat bertindak sebagai ``` master ``` atau ``` slave ```. ``` Master ``` adalah perangkat utama yang memiliki otoritas penuh atas kontrol Slave, sedangkan ``` Slave ``` adalah perangkat sekunder yang berada di bawah otoritas perangkat Master.<br><br>

• <strong>Internet of Things</strong>

``` Internet of Things (IoT) ``` adalah sebuah konsep dimana suatu hal yang terhubung ke jaringan dapat melakukan satu tindakan atau lebih dalam mencapai suatu tujuan. Tindakan ini diantaranya berupa pengumpulan data, pengiriman data, penerimaan data, atau pengolahan data. Setiap proyek IoT pasti membutuhkan perangkat yang dapat terhubung ke WiFi seperti ESP. ESP terdiri dari 2 jenis, yaitu ``` ESP8266 ``` dan ``` ESP32 ```. Hal ini di pasaran sangat beragam sekali modelnya, untuk itu perlu sekali anda menyesuaikan kembali dengan kebutuhan yang ada di proyek agar tidak menimbulkan kekecewaan.

<br><br>

## Kalibrasi Sensor RTC
Sensor RTC ini dapat di kalibrasi dengan menggunakan kode program berikut :

```ino
#include <RTClib.h> // Calling the RTC library
RTC_DS3231 rtc; // Constructor

void setup(){
   RTCinit(); // Calling the RTCinit method
}

void loop(){}

void RTCinit(){
   // Starting up the RTC
   rtc.begin();

   // DateTime Setting
   rtc.adjust(DateTime(F(__DATE__), F(__TIME__)));

   // Set Time Now
   rtc.adjust(DateTime(YYYY,MM,DD,HH,MM,SS)); // If you have calibrated please close with a comment
}
```

<br><br>

## Pengaturan Visual Studio Code
Coming Soon...

<br><br>

## Pengaturan USB CH340-ESP01
<img width="840" src="https://github.com/devancakra/Whatsapp-Bot-based-Automatic-Fish-Monitoring-Feeding-System-using-I2C-communication-protocol/assets/54527592/a09121f7-c560-417f-890f-b683f8cf9540" alt="pinout"><br><br><br>

1. ``` Mode Pemrograman ``` :

   • Pasang ``` ESP-01 ``` ke ``` USB CH340-ESP01 ```.
   
   • Tekan dan tahan tombol yang ada di ``` USB CH340-ESP01 ```, lalu tancapkan pada komputer/laptop.
   
   • Lepaskan tombol ketika perangkat sudah dikenali oleh komputer/laptop.
   
   • Silakan ``` unggah program ```.<br><br>
   
2. ``` Mode Pengoperasian ``` :
   
   • Lepaskan ``` USB CH340-ESP01 ``` dari komputer/laptop.
   
   • Kode program yang telah tertanam dalam ``` board ESP-01 ``` ini siap untuk dioperasikan (sudah tidak ada aktivitas pemrograman lagi).

   • Lepaskan ``` ESP01 ``` dari ``` USB CH340-ESP01 ```. Lakukan pemasangan kabel seperti yang ditunjukkan dalam diagram ilustrasi.<br><br><br>

<strong>Catatan :</strong>

<table><tr><td width="840">

   • Untuk mengunggah program, selain menggunakan ``` USB CH340-ESP01 ```, anda juga dapat menggunakan alat pemrogram lainnya seperti: ``` USB CP2102 ```, ``` USB CH340 ```, ``` USB FTDI ```, atau dengan ``` USB PL2303 ```.

   • Berdasarkan pengalaman, saya akui bahwa penggunaan ``` USB CH340-ESP01 ``` ini jauh lebih baik daripada alat pemrogram lainnya karena tidak membutuhkan kabel untuk dapat terhubung ke komputer/laptop.

</td></tr></table><br><br>

## Pengaturan Twilio
1. Memulai Twilio :
   
   <table><tr><td width="810">
      
   • Buka url berikut ini: <a href="https://www.twilio.com/">Klik Disini</a>.

   • Klik ``` Log in ``` untuk mengakses layanan.

   • Jika anda belum memiliki akun, klik ``` Sign up ```.

   </td></tr></table><br>

2. Isi semua kolom yang diperlukan.<br><br>

3. Verifikasi ``` nomor telepon ``` dan ``` email ``` anda.<br><br>

4. Akses ``` WhatsApp sandbox ``` di menu ``` Settings ``` dan ``` kirimkan kode ``` ke ``` nomor WhatsApp yang disediakan ```.
   
<br><br>

## Pengaturan ThingESP
1. Memulai ThingESP :
   
   <table><tr><td width="810">

   • Buka url berikut ini: <a href="https://thingesp.siddhesh.me/#/">Klik Disini</a>.

   • Klik ``` Login ``` untuk mengakses layanan.

   • Jika anda belum memiliki akun, klik ``` Create Account ```.

   </td></tr></table><br>

2. Isi semua kolom yang diperlukan.<br><br>

3. Klik ``` Project ``` di bagian sidebar -> lalu pilih ``` Add New Project ```.<br><br>

4. Setelah proyek dibuat, masukkan ``` URL Twilio WhatsApp Endpoint ``` ke dalam ``` ThingESP ``` agar dapat terhubung.
   
<br><br>

## Memulai
1. Unduh dan ekstrak repositori ini.<br><br>

2. Pastikan anda memiliki komponen elektronik yang diperlukan.<br><br>
   
3. Pastikan komponen anda telah dirancang sesuai dengan diagram.<br><br>
   
4. Konfigurasikan perangkat anda menurut pengaturan di atas.<br><br>
    
5. Selamat menikmati [Selesai].

<br><br>

## Demonstrasi Aplikasi
Via Whatsapp: <a href="https://github.com/devancakra/Whatsapp-Bot-based-Automatic-Fish-Monitoring-Feeding-System-using-I2C-communication-protocol/">AutoFish Bot</a>

<br><br>

## Sorotan
<table>
<tr>
<th width="840">Perangkat Keras</th>
</tr>
<tr>
<td><img src="" alt="hardware"></td>
</tr>
</table>
<table>
<tr>
<th width="840" colspan="2">Bot Whatsapp</th>
</tr>
<tr>
<td width="420"><img src="" alt="wa_bot1"></td>
<td width="420"><img src="" alt="wa_bot2"></td>
</tr>
</table>

<br><br>

## Pengujian Komponen
Anda dapat mengunduh berkas uji komponen melalui tautan berikut: <a href="https://github.com/devancakra/Whatsapp-Bot-based-Automatic-Fish-Monitoring-Feeding-System-using-I2C-communication-protocol/">Klik Disini</a>

<br><br>

## Apresiasi
Jika karya ini bermanfaat bagi anda, maka dukunglah karya ini sebagai bentuk apresiasi kepada penulis dengan mengklik tombol ``` ⭐Bintang ``` di bagian atas repositori.

<br><br>

## Penafian
Aplikasi ini dibuat dengan menyertakan sumber-sumber dari pihak ketiga. Pihak ketiga di sini adalah penyedia layanan, yang layanannya berupa pustaka, kerangka kerja, dan lain-lain. Saya ucapkan terima kasih banyak atas layanannya. Telah terbukti sangat membantu dan dapat diimplementasikan.

<br><br>

## LISENSI
LISENSI MIT - Hak Cipta © 2024 - Devan C. M. Wijaya, S.Kom

Dengan ini diberikan izin tanpa biaya kepada siapa pun yang mendapatkan salinan perangkat lunak ini dan file dokumentasi terkait perangkat lunak untuk menggunakannya tanpa batasan, termasuk namun tidak terbatas pada hak untuk menggunakan, menyalin, memodifikasi, menggabungkan, mempublikasikan, mendistribusikan, mensublisensikan, dan/atau menjual salinan Perangkat Lunak ini, dan mengizinkan orang yang menerima Perangkat Lunak ini untuk dilengkapi dengan persyaratan berikut:

Pemberitahuan hak cipta di atas dan pemberitahuan izin ini harus menyertai semua salinan atau bagian penting dari Perangkat Lunak.

DALAM HAL APAPUN, PENULIS ATAU PEMEGANG HAK CIPTA DI SINI TETAP MEMILIKI HAK KEPEMILIKAN PENUH. PERANGKAT LUNAK INI DISEDIAKAN SEBAGAIMANA ADANYA, TANPA JAMINAN APAPUN, BAIK TERSURAT MAUPUN TERSIRAT, OLEH KARENA ITU JIKA TERJADI KERUSAKAN, KEHILANGAN, ATAU LAINNYA YANG TIMBUL DARI PENGGUNAAN ATAU URUSAN LAIN DALAM PERANGKAT LUNAK INI, PENULIS ATAU PEMEGANG HAK CIPTA TIDAK BERTANGGUNG JAWAB, KARENA PENGGUNAAN PERANGKAT LUNAK INI TIDAK DIPAKSAKAN SAMA SEKALI, SEHINGGA RISIKO ADALAH MILIK ANDA SENDIRI.
