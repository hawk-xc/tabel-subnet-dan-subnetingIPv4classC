# tabel-subnet-dan-subnetingIPv4classC
<b>IP Address</b> adalah serangkaian angka yang menjadi identitas perangkat yang terhubung ke internet atau infrastruktur jaringan lainnya. Fungsinya seperti nomor rumah pada alamat, yaitu untuk memastikan agar data dikirimkan ke perangkat yang tepat. Panjang rangkaian angkanya adalah dari 0.0.0.0 sampai 255.255.255.255.
</br>
</br>
sedangkan <b>Subnetting</b> adalah proses untuk memecahkan atau membagi sebuat network menjadi beberapa network yang lebih kecil, atau Subnetting merupakan sebuah teknik yang mengizinkan para administrator jaringan untuk memanfaatkan 32 bit IP address yang tersedia dengan lebih efisien.
</br>
</br>
IPv4 merupakan alamat Internet Protocol versi 4, alamat IPv4 memiliki beberapa kelas, antara lain class A, B, C, D, dan experimental. pada pembahasan kali ini saya akan membahas subnet pada IPv4 class C. IPv4 class C terdiri dari 4 octet atau 4 block yang dipisahkan oleh titik, nah pada block/octet 1 - 3 merupakan octet network dan octect ke-4 merupakan octect host, setiap octect direpresentasikan dengan 8 bit-per-octect hingga keseluruhannya IPv4 class C memiliki 32 bit . IPv4 tediri dari 192 - 223 range address.
</br>
</br>
Subnet mask adalah istilah teknologi Informasi yang membedakan Network ID dan Host ID atau sebagai penentu porsi Network ID dan Host ID pada deretan kode biner. Fungsi dari subnet mask sendiri adalah untuk membedakan Network ID dengan Host ID dan menentukan alamat tujuan paket data apakah local atau remote.
</br>
</br>
Apa itu Network ID dan Host ID ? Network ID adalah bagian dari IP Address yg berfungsi untuk menunjukan di jaringan mana komputer atau device tersebut berada, sedangkan Host ID menunjukan server, router, workstation, dan host TCP/IP lainnya yang berada di dalam jaringan tersebut. Terdapat 2 cara untuk mempresentasikan Subnet mask yaitu dengan cara notasi desimal bertitik dan notasi panjang prefix.

# table subneting IPv4 Class C
| bits/prefix | hosts | usable hosts | netmask | binnary |
|------|-------|--------------|---------|----------------|
| /23 | 512 | 510 | 255.255.254.0 | 11111111.11111111.11111110.00000000 |
| /24 | 256 | 254 | 255.255.255.0 | 11111111.11111111.11111111.00000000 |
| /25 | 128 | 126 | 255.255.255.128 | 11111111.11111111.11111111.10000000 |
| /26 | 64 | 62 | 255.255.255.192 | 11111111.11111111.11111111.11000000 |
| /27 | 32 | 30 | 255.255.255.224 | 11111111.11111111.11111111.11100000 |
| /28 | 16 | 14 | 255.255.255.240 | 11111111.11111111.11111111.11110000 |
| /29 | 8 | 6 | 255.255.255.248 | 11111111.11111111.11111111.11111000 |
| /30 | 4 | 2 | 255.255.255.252 | 11111111.11111111.11111111.11111100 |
| /31 | 1 | 1 | 255.255.255.255 | 11111111.11111111.11111111.11111111 |
| /32 | 1 | 1 | 255.255.255.255 | 11111111.11111111.11111111.11111111 |

# cara menghitung bits dan subnet mask
cara kita untuk menghitung jumlah host dengan prefix. kita hanya perlu tahu bahwa bits /30 mengandung 4 host. dimana bisa untuk kita jadian acuan.
</br>/30 = 4 host
</br>/29 = maka 4+4 = 8 host
</br>/28 = maka 8+8 = 16 host
</br>/27 = maka 16+16 = 32 host
</br>/26 = maka 32+32 = 64 host
</br>dst...

sedangkan untuk menghitung <b>subnet mask</b>, maka
</br>256 dikurangi jumlah host. sebagai contoh. /28 dengan jumlah host (16) maka, 256 - 16 = 240 (255.255.255.240)

# contoh soal
### 1. IP Pertama dan terakhir yang dapat kita gunakan pada 130.12.12.195/26 adalah
/26 = 64 (host per prefix)
```bash
-> perhitungan ip awal/network
195/64 = 3
3 * 64 = 192 (ip pertama)
130.12.12.192

# Tip
jika hasil pembagian menghasilkan bilangan desimal, contoh (4.56) maka ambil bilangan depan (4) abaikan hasil sisanya.

-> perhitungan ip akhir/broadcast
192+64-1 = 255(ip akhir)
130.12.12.255

-> range host
range host merupakan bilangan yang berada ditengah-tengah ip awal dan ip akhir, bisa dikalkulasikan seperti berikut
130.12.12.193 - 130.12.12.254

-> Subnet mask
256-64 = 192
255.255.255.192
```

### 2. IP Gateway yang mungkin digunakan jika ip client adalah 192.168.20.254/30 adalah…
/30 = 4 (host per prefix)
```bash
-> perhitungan ip awal/network
254/4 = 63.5
63 * 4 = 252 (ip pertama)
192.168.20.252

-> perhitungan ip akhir/broadcast
252+4-1 = 255
192.168.20.255

-> range host
ip gateway bisa dikatakan ip host pertama, maka
ip gateway = 192.168.20.253
192.168.20.253 - 192.168.20.254

-> Subnet mask
256 - 2 = 252
255.255.255.252
```

### 3. IP Host yang valid pada 178.167.10.234/29 adalah…
/29 = 8
```bash
-> perhitungan ip awal/network
234/8 = 29.25
29 * 8 = 232
178.167.10.232

-> perhitungan ip akhir/broadcast
232+8-1 = 239
178.167.10.239

-> range host
178.167.10.233 - 178.167.10.238

-> Subnet mask
256-8 = 248
255.255.255.248
```
mudah bukan, cara diatas merupakan perhitungan cepat, praktis dan mudah untuk dipahami dan mungkin bisa saja terdapat kesalahan, silakan dipelajari...
