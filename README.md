# tabel-subnet-dan-subnetingIPv4classC
<b>IP Address</b> adalah serangkaian angka yang menjadi identitas perangkat yang terhubung ke internet atau infrastruktur jaringan lainnya. Fungsinya seperti nomor rumah pada alamat, yaitu untuk memastikan agar data dikirimkan ke perangkat yang tepat. Panjang rangkaian angkanya adalah dari 0.0.0.0 sampai 255.255.255.255.

sedangkan <b>Subnetting</b> adalah proses untuk memecahkan atau membagi sebuat network menjadi beberapa network yang lebih kecil, atau Subnetting merupakan sebuah teknik yang mengizinkan para administrator jaringan untuk memanfaatkan 32 bit IP address yang tersedia dengan lebih efisien.

# table subneting IPv4 Class C
| bits/prefix | hosts | usable hosts | netmask | 
|------|-------|--------------|---------|
| /23 | 512 | 510 | 255.255.254.0 |
| /24 | 256 | 254 | 255.255.255.0 |
| /25 | 128 | 126 | 255.255.255.128 |
| /26 | 64 | 62 | 255.255.255.192 |
| /27 | 32 | 30 | 255.255.255.224 |
| /28 | 16 | 14 | 255.255.255.240 |
| /29 | 8 | 6 | 255.255.255.248 |
| /30 | 4 | 2 | 255.255.255.252 |
| /31 | 1 | 1 | 255.255.255.255 |
| /32 | 1 | 1 | 255.255.255.255 |

# cara menghitung bits dan subnet mask
cara kita untuk menghitung jumlah host dengan prefix. kita hanya perlu tahu bahwa bits /30 mengandung 4 host. dimana bisa untuk kita jadian acuan.
/30 = 4 host
/29 = maka 4+4 = 8 host
/28 = maka 8+8 = 16 host
/27 = maka 16+16 = 32 host
/26 = maka 32+32 = 64 host
dst...

sedangkan untuk menghitung <b>subnet mask</b>, maka
256 dikurangi jumlah host. sebagai contoh.
/28 dengan jumlah host (16) maka, 256 - 16 = 240 (255.255.255.240)

# contoh soal
### 1. IP Pertama dan terakhir yang dapat kita gunakan pada 130.12.12.195/26 adalah
/26 = 64 (host per prefix)
```bash
-> perhitungan ip awal/network
195/64 = 3
3 * 64 = 192(ip pertama)
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
