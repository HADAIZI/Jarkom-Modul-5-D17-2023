# Jarkom-Modul-5-D17-2023

**Praktikum Jaringan Komputer Modul 5 Tahun 2023**

# Author
| Nama | NRP |Github |
|---------------------------|------------|--------|
|Adam Haidar Azizi | 5025211114 | https://github.com/HADAIZI |
|Ahda Filza Ghaffaru | 5025211144 | https://github.com/Ahdaaa |


## **Soal Nomor 0**
Setelah pandai mengatur jalur-jalur khusus, kalian diminta untuk membantu North Area menjaga wilayah mereka dan kalian dengan senang hati membantunya karena ini merupakan tugas terakhir.

- Tugas pertama, buatlah peta wilayah sesuai berikut ini:
![Alt text](image-1.png)
- Untuk menghitung rute-rute yang diperlukan, gunakan perhitungan dengan metode VLSM. Buat juga pohonnya, dan lingkari subnet yang dilewati.

- Kemudian buatlah rute sesuai dengan pembagian IP yang kalian lakukan. 

- Tugas berikutnya adalah memberikan ip pada subnet SchwerMountain, LaubHills, TurkRegion, dan GrobeForest menggunakan bantuan DHCP.

## **Penyelesaian Soal Nomor 0**
Setelah topologi berhasil dibuat pada GNS3, langkah selanjutnya yang dilakukan adalah membuat rute dan melakukan _subnetting_. Berikut adalah hasil dari pembuatan rute serta _subnetting_ yang sudah dilakukan:

- **Tree**

![Alt text](<WhatsApp Image 2023-12-20 at 9.55.51 PM.jpeg>)

- **Rute**
![Alt text](image-2.png)

- **Kongfigurasi setiap _node_** <br>

Berikut adalah kongfigurasi untuk tiap node dalam topologi pada soal praktikum:

- Aura

```shell
auto eth0
iface eth0 inet dhcp

auto eth1
iface eth1 inet static
	address 10.30.14.145
        netmask 255.255.255.252

auto eth2
iface eth2 inet static
	address 10.30.14.149
	netmask 255.255.255.252

```

- **Revolte**
```bash

auto eth0
iface eth0 inet static
	address 10.30.14.134
	netmask 255.255.255.252
	gateway 10.30.14.133
```

- **Richter**
```bash

auto eth0
iface eth0 inet static
	address 10.30.14.130
	netmask 255.255.255.252
	gateway 10.30.14.129
```

- **Fern**
```bash
auto eth0
iface eth0 inet static
	address 10.30.14.3
	netmask 255.255.255.128
        gateway 10.30.14.1

auto eth1
iface eth1 inet static
	address 10.30.14.129
	netmask 255.255.255.252

auto eth2
iface eth2 inet static
	address 10.30.14.133
	netmask 255.255.255.252



```

- **SchwerMountain**
```bash
auto eth0
iface eth0 inet dhcp
hwaddress ether fe:91:9a:1f:1d:bc
```

- **Himmel**
```bash
auto eth0
iface eth0 inet static
	address 10.30.14.142
	netmask 255.255.255.252
	gateway 10.30.14.141

auto eth1
iface eth1 inet static
	address 10.30.12.1
	netmask 255.255.254.0

auto eth2
iface eth2 inet static
	address 10.30.14.1
	netmask 255.255.255.128

```

- **LaubHills**
```bash
auto eth0
iface eth0 inet dhcp
hwaddress ether ca:98:ba:05:41:a3

```

- **Frieren**
```bash
auto eth0
iface eth0 inet static
	address 10.30.14.150
	netmask 255.255.255.252
	gateway 10.30.14.149

auto eth1
iface eth1 inet static
	address 10.30.14.137
	netmask 255.255.255.252

auto eth2
iface eth2 inet static
	address 10.30.14.141
	netmask 255.255.255.252


```

- **Stark**
```bash
auto eth0
iface eth0 inet static
	address 10.30.14.138
	netmask 255.255.255.252
	gateway 10.30.14.137

```

- **Heiter**
```bash
auto eth0
iface eth0 inet static
	address 10.30.14.146
	netmask 255.255.255.252
	gateway 10.30.14.145

auto eth1
iface eth1 inet static
	address 10.30.0.1
	netmask 255.255.248.0

auto eth2
iface eth2 inet static
	address 10.30.8.1
	netmask 255.255.252.0
```

- **TurkRegion**
```bash
#A9
auto eth0
iface eth0 inet dhcp
hwaddress ether 52:22:61:b7:6c:e3

```

- **Sein**
```bash
auto eth0
iface eth0 inet static
	address 10.30.8.2
	netmask 255.255.252.0
	gateway 10.30.8.1

```

- **GrobeForest**
```bash
auto eth0
iface eth0 inet dhcp
hwaddress ether 7e:62:3d:83:91:4e
```

