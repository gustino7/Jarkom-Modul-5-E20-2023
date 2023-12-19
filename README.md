# Jarkom-Modul-5-E20-2023
Nama Anggota :

1. Moch. Taslam Gustino P (5025211011)

# Lapres

## Topologi
![image](https://github.com/gustino7/Jarkom-Modul-5-E20-2023/assets/93267604/e8e76a91-660d-422e-af01-85b8012f39a1)

## Rute
![image](https://github.com/gustino7/Jarkom-Modul-5-E20-2023/assets/93267604/cb91efc2-12f9-4477-9934-65283701ecd0)

## Tree
![image](https://github.com/gustino7/Jarkom-Modul-5-E20-2023/assets/93267604/f6068c38-014d-43ec-8a20-6dce405de718)

## Pembagian IP VLSM
![image](https://github.com/gustino7/Jarkom-Modul-5-E20-2023/assets/93267604/9bb9ec96-d192-455e-ad02-03ff45f75c64)

## Subnetting

### Aura
```
auto eth0
iface eth0 inet dhcp

auto eth1
iface eth1 inet static
	address 192.216.0.21
	netmask 255.255.255.252

auto eth2
iface eth2 inet static
	address 192.216.0.1
	netmask 255.255.255.252
```

### Frieren
```
auto eth0
iface eth0 inet static
	address 192.216.0.2
	netmask 255.255.255.252

auto eth1
iface eth1 inet static
	address 192.216.0.9
	netmask 255.255.255.252

auto eth2
iface eth2 inet static
	address 192.216.0.5
	netmask 255.255.255.252
```

### Stark
```
auto eth0
iface eth0 inet static
	address 192.216.0.6
	netmask 255.255.255.252
	gateway 192.216.0.5
```

### Himmel
```
auto eth0
iface eth0 inet static
	address 192.216.0.10
	netmask 255.255.255.252

auto eth1
iface eth1 inet static
	address 192.216.0.129
	netmask 255.255.255.128

auto eth2
iface eth2 inet static
	address 192.216.2.1
	netmask 255.255.254.0
```

### LaubHills
```
auto eth0
iface eth0 inet dhcp
```

### SchwerMountain
```
auto eth0
iface eth0 inet dhcp
```

### Fern
```
auto eth0
iface eth0 inet static
	address 192.216.0.131
	netmask 255.255.255.128

auto eth1
iface eth1 inet static
	address 192.216.0.17
	netmask 255.255.255.252

auto eth2
iface eth2 inet static
	address 192.216.0.13
	netmask 255.255.255.252
```

### Richter
```
auto eth0
iface eth0 inet static
	address 192.216.0.14
	netmask 255.255.255.252
	gateway 192.216.0.13
```

### Revolte
```
auto eth0
iface eth0 inet static
	address 192.216.0.18
	netmask 255.255.255.252
	gateway 192.216.0.17
```

### Heiter
```
auto eth0
iface eth0 inet static
	address 192.216.0.22
	netmask 255.255.255.128

auto eth1
iface eth1 inet static
	address 192.216.8.1
	netmask 255.255.248.0

auto eth2
iface eth2 inet static
	address 192.216.4.1
	netmask 255.255.252.0
```

### TurkRegion
```
auto eth0
iface eth0 inet dhcp
```

### Sein
```
auto eth0
iface eth0 inet static
	address 192.216.4.2
	netmask 255.255.252.0
	gateway 192.216.4.1
```

### GrobeForest
```
auto eth0
iface eth0 inet dhcp
```

## Routing

### Aura
```
Network 192.216.0.4 Netmask 255.255.255.252 Next Hop 192.216.0.2
Network 192.216.0.8 Netmask 255.255.255.252 Next Hop 192.216.0.2
Network 192.216.2.0 Netmask 255.255.254.0 Next Hop 192.216.0.2
Network 192.216.0.128 Netmask 255.255.255.128 Next Hop 192.216.0.2
Network 192.216.0.12 Netmask 255.255.255.252 Next Hop 192.216.0.2
Network 192.216.0.16 Netmask 255.255.255.252 Next Hop 192.216.0.2
Network 192.216.8.0 Netmask 255.255.248.0 Next Hop 192.216.0.22
Network 192.216.4.0 Netmask 255.255.252.0 Next Hop 192.216.0.22

route add -net 192.216.0.4 netmask 255.255.255.252 gw 192.216.0.2
route add -net 192.216.0.8 netmask 255.255.255.252 gw 192.216.0.2
route add -net 192.216.2.0 netmask 255.255.254.0 gw 192.216.0.2
route add -net 192.216.0.128 netmask 255.255.255.128 gw 192.216.0.2
route add -net 192.216.0.12 netmask 255.255.255.252 gw 192.216.0.2
route add -net 192.216.0.16 netmask 255.255.255.252 gw 192.216.0.2
route add -net 192.216.8.0 netmask 255.255.248.0 gw 192.216.0.22
route add -net 192.216.4.0 netmask 255.255.252.0 gw 192.216.0.22
```

### Frieren
```
Network 0.0.0.0 Netmask 0.0.0.0 Next Hop 192.216.0.1
Network 192.216.2.0 Netmask 255.255.254.0 Next Hop 192.216.0.10
Network 192.216.0.128 Netmask 255.255.255.128 Next Hop 192.216.0.10
Network 192.216.0.12 Netmask 255.255.255.252 Next Hop 192.216.0.10
Network 192.216.0.16 Netmask 255.255.255.252 Next Hop 192.216.0.10

route add -net 0.0.0.0 netmask 0.0.0.0 gw 192.216.0.1
route add -net 192.216.2.0 netmask 255.255.254.0 gw 192.216.0.10
route add -net 192.216.0.128 netmask 255.255.255.128 gw 192.216.0.10
route add -net 192.216.0.12 netmask 255.255.255.252 gw 192.216.0.10
route add -net 192.216.0.16 netmask 255.255.255.252 gw 192.216.0.10
```

### Himmel
```
Network 0.0.0.0 Netmask 0.0.0.0 Next Hop 192.216.0.9
Network 192.216.0.12 Netmask 255.255.255.252 Next Hop 192.216.0.131
Network 192.216.0.16 Netmask 255.255.255.252 Next Hop 192.216.0.131

route add -net 0.0.0.0 netmask 0.0.0.0 gw 192.216.0.9
route add -net 192.216.0.12 netmask 255.255.255.252 gw 192.216.0.131
route add -net 192.216.0.16 netmask 255.255.255.252 gw 192.216.0.131
```

### Fern
```
Network 0.0.0.0 Netmask 0.0.0.0 Next Hop 192.216.0.129

route add -net 0.0.0.0 netmask 0.0.0.0 gw 192.216.0.129
```

### Heiter
```
Network 0.0.0.0 Netmask 0.0.0.0 Next Hop 192.216.0.21

route add -net 0.0.0.0 netmask 0.0.0.0 gw 192.216.0.21
```

## Konfigurasi

### Router Aura
```
IPETH0="$(ip -br a | grep eth0 | awk '{print $NF}' | cut -d'/' -f1)"
iptables -t nat -A POSTROUTING -o eth0 -j SNAT --to-source "$IPETH0" -s 192.216.0.0/20
```

### DHCP Server
```
apt-get update
apt-get install isc-dhcp-server

echo '
INTERFACESv4="eth0"
INTERFACESv6="eth0"
' > /etc/default/isc-dhcp-server

echo '
subnet 192.216.0.16 netmask 255.255.255.252 {
}

# Subnet A8 SchwerMountain
subnet 192.216.0.128 netmask 255.255.255.128 {
    range 192.216.0.132 192.216.0.195;
    option routers 192.216.0.131; #IP Fern yang mengarah ke A8
    option broadcast-address 192.216.0.255;
    option domain-name-servers 192.216.0.14;
}

# Subnet A7 LaubHills
subnet 192.216.2.0 netmask 255.255.254.0 {
    range 192.216.2.2 192.216.3.1;
    option routers 192.216.2.1; #IP Himmel yang mengarah ke A7
    option broadcast-address 192.216.3.255;
    option domain-name-servers 192.216.0.14;
}

# Subnet A3 TurkRegion
subnet 192.216.8.0 netmask 255.255.248.0 {
    range 192.216.8.2 192.216.12.1;
    option routers 192.216.8.1; #IP Heiter yang mengarah ke A3
    option broadcast-address 192.216.15.255;
    option domain-name-servers 192.216.0.14;
}

# Subnet A2 GrobeForest
subnet 192.216.4.0 netmask 255.255.252.0 {
    range 192.216.4.3 192.216.6.4;
    option routers 192.216.4.1; #IP Heiter yang mengarah ke A2
    option broadcast-address 192.216.7.255;
    option domain-name-servers 192.216.0.14;
} ' > /etc/dhcp/dhcpd.conf
```

### DHCP Relay
```
apt-get update
apt-get install isc-dhcp-relay -y
```

- FERN
``` 
echo '
SERVERS="192.216.0.18" # IP DHCP SERVER
INTERFACES="eth0 eth1"
OPTIONS=' > /etc/default/isc-dhcp-relay
echo '
net.ipv4.ip_forward=1 ' > /etc/sysctl.conf
service isc-dhcp-relay start
```

- HIMMEL
```
echo '
SERVERS="192.216.0.18" # IP DHCP SERVER
INTERFACES="eth0 eth1 eth2"
OPTIONS=' > /etc/default/isc-dhcp-relay
echo '
net.ipv4.ip_forward=1 ' > /etc/sysctl.conf
service isc-dhcp-relay start
```

- FRIEREN
```
echo '
SERVERS="192.216.0.18" # IP DHCP SERVER
INTERFACES="eth0 eth1"
OPTIONS=' > /etc/default/isc-dhcp-relay
echo '
net.ipv4.ip_forward=1 ' > /etc/sysctl.conf
service isc-dhcp-relay start
```

- AURA
```
echo '
SERVERS="192.216.0.18" # IP DHCP SERVER
INTERFACES="eth1 eth2"
OPTIONS=' > /etc/default/isc-dhcp-relay
echo '
net.ipv4.ip_forward=1 ' > /etc/sysctl.conf
service isc-dhcp-relay start
```

- HEITER
```
echo '
SERVERS="192.216.0.18" # IP DHCP SERVER
INTERFACES="eth0 eth1 eth2"
OPTIONS=' > /etc/default/isc-dhcp-relay
echo '
net.ipv4.ip_forward=1 ' > /etc/sysctl.conf
service isc-dhcp-relay restart
```

## Jawaban

### Soal 1
Aura
```
IPETH0="$(ip -br a | grep eth0 | awk '{print $NF}' | cut -d'/' -f1)"
iptables -t nat -A POSTROUTING -o eth0 -j SNAT --to-source "$IPETH0" -s 192.216.0.0/20
```
ip -br a: Menampilkan informasi antarmuka jaringan dalam format ringkas.
grep eth0: Mencari baris yang mengandung "eth0" dalam output.
awk '{print $NF}': Mengambil kolom terakhir dari baris tersebut (kolom dengan alamat IP).
cut -d'/' -f1: Memotong bagian dari alamat IP yang berisi subnet dan menyimpan hanya bagian alamat IP itu sendiri di variabel IPETH0.

Paket yang keluar melalui antarmuka eth0 dan berasal dari jaringan 192.216.0.0/20 akan mengalami SNAT (Source NAT), di mana alamat pengirimnya akan diubah menjadi alamat IP dari eth0 (seperti yang telah diambil pada langkah sebelumnya dan disimpan di variabel IPETH0).

#### Testing
![image](https://github.com/gustino7/Jarkom-Modul-5-E20-2023/assets/93267604/88495cc3-7472-480e-9983-8f508040598c)

### Soal 2
LAUBHILLS
```
iptables -F
iptables -P INPUT DROP
iptables -P OUTPUT DROP
iptables -P FORWARD DROP
iptables -A INPUT -p tcp --dport 8080 -j ACCEPT
iptables -A OUTPUT -p tcp --sport 8080 -j ACCEPT
```
iptables -F
Perintah ini menghapus semua aturan yang sudah ada dalam tabel filter, sehingga mengatur ulang aturan firewall.

iptables -P INPUT DROP
Perintah ini mengatur kebijakan default untuk lalu lintas masuk (rantai INPUT) menjadi DROP. Artinya, kecuali ada aturan khusus yang mengizinkan lalu lintas tertentu, semua lalu lintas masuk akan ditolak.

iptables -P OUTPUT DROP
Perintah ini mengatur kebijakan default untuk lalu lintas keluar (rantai OUTPUT) menjadi DROP. Sama seperti sebelumnya, artinya kecuali ada aturan khusus yang mengizinkan lalu lintas tertentu, semua lalu lintas keluar akan ditolak.

iptables -P FORWARD DROP
Perintah ini mengatur kebijakan default untuk lalu lintas yang di-forward (rantai FORWARD) menjadi DROP. Ini berlaku untuk paket-paket yang diarahkan melalui sistem, yang umumnya terjadi dalam konfigurasi jaringan dengan beberapa subnet.

iptables -A INPUT -p tcp --dport 8080 -j ACCEPT
Aturan ini mengizinkan lalu lintas TCP masuk pada port 8080. Perintahnya menambahkan (-A) aturan ke rantai INPUT, yang menyatakan bahwa lalu lintas TCP pada port 8080 akan diterima.

#### Testing
![image](https://github.com/gustino7/Jarkom-Modul-5-E20-2023/assets/93267604/a3f9c9ca-c6d0-4b28-8556-334a3b5c663f)
![image](https://github.com/gustino7/Jarkom-Modul-5-E20-2023/assets/93267604/c842cf26-9fd8-453e-9abc-574c689af4f2)
![image](https://github.com/gustino7/Jarkom-Modul-5-E20-2023/assets/93267604/b139b09a-2383-4157-84f4-dfb6e4ed67a6)
![image](https://github.com/gustino7/Jarkom-Modul-5-E20-2023/assets/93267604/758b5b5a-85c4-4dca-9d85-1c9755fce597)

### Soal 3
Richter & Revolte
```
iptables -A INPUT -p icmp -m connlimit --connlimit-above 3 --connlimit-mask 0 -j REJECT
iptables -I INPUT -m state --state ESTABLISHED,RELATED -j ACCEPT
```
iptables -A INPUT
Menambahkan aturan ke rantai INPUT, yang berarti aturan ini akan diterapkan pada lalu lintas yang masuk ke sistem.

-p icmp
Menentukan protokol yang diizinkan, dalam hal ini ICMP (Internet Control Message Protocol), yang sering digunakan untuk ping dan pesan kontrol jaringan.

--connlimit-above 3
Menentukan bahwa aturan ini akan diterapkan jika jumlah koneksi melebihi 3.

--connlimit-mask 0
Menetapkan bahwa pembatasan koneksi akan diterapkan pada seluruh alamat IP (tanpa menggunakan subnet mask).

-j REJECT
Menentukan tindakan yang akan diambil jika aturan terpenuhi. Dalam hal ini, jika jumlah koneksi ICMP melebihi batas yang ditentukan, lalu lintas akan ditolak

#### Testing
![image](https://github.com/gustino7/Jarkom-Modul-5-E20-2023/assets/93267604/460c6fce-3805-407c-8874-179ec07b77ca)
![image](https://github.com/gustino7/Jarkom-Modul-5-E20-2023/assets/93267604/b59fd5cd-c583-43a1-aaa3-36bd9bfe3ad1)
![image](https://github.com/gustino7/Jarkom-Modul-5-E20-2023/assets/93267604/bc7e3939-7706-447d-aee2-5a9910906f5f)
![image](https://github.com/gustino7/Jarkom-Modul-5-E20-2023/assets/93267604/559e68d0-be5c-4c58-a693-fc3b566d26f0)
![image](https://github.com/gustino7/Jarkom-Modul-5-E20-2023/assets/93267604/16b900fc-0178-491a-b60f-8a11537707fb)

### Soal 4
Sein & Stark
```
iptables -A INPUT -p tcp --dport 22 -s 192.216.4.0/22 -j ACCEPT
iptables -A INPUT -p tcp --dport 22 -j REJECT
iptables -A OUTPUT -p tcp --dport 22 -j REJECT
```
iptables -A INPUT -p tcp --dport 22 -s 192.216.4.0/22 -j ACCEPT
Menambahkan aturan ke rantai INPUT untuk menerima lalu lintas TCP pada port 22 (port default SSH).
Hanya lalu lintas yang berasal dari alamat IP dalam rentang 192.216.4.0 hingga 192.216.7.255 yang akan diizinkan (subnet mask /22).

iptables -A INPUT -p tcp --dport 22 -j REJECT
Menambahkan aturan kedua ke rantai INPUT untuk menolak lalu lintas TCP pada port 22.
Aturan ini akan diterapkan pada lalu lintas yang tidak sesuai dengan aturan pertama (yang diizinkan hanya dari subnet tertentu). Jadi, aturan ini menolak sisa lalu lintas SSH.

iptables -A OUTPUT -p tcp --dport 22 -j REJECT
Menambahkan aturan ke rantai OUTPUT untuk menolak lalu lintas keluar pada port 22.
Ini memastikan bahwa sistem tidak dapat menginisiasi koneksi keluar melalui port SSH.

#### Testing
![image](https://github.com/gustino7/Jarkom-Modul-5-E20-2023/assets/93267604/ab796256-063b-4cf1-a15c-b314878ff08f)
![image](https://github.com/gustino7/Jarkom-Modul-5-E20-2023/assets/93267604/a102d11a-32df-4efa-871d-bd0f187b3640)
![image](https://github.com/gustino7/Jarkom-Modul-5-E20-2023/assets/93267604/17966238-a056-4e7c-954e-ee4d77290397)
![image](https://github.com/gustino7/Jarkom-Modul-5-E20-2023/assets/93267604/3128c529-a41c-46dc-86d9-6f98536d0139)

### Soal 5
Sein & Stark
```
iptables -A INPUT -m time --weekdays Mon,Tue,Wed,Thu,Fri --timestart 08:00 --timestop 16:00 -j ACCEPT
iptables -A INPUT -j REJECT
```
--weekdays Mon,Tue,Wed,Thu,Fri: Aturan ini berlaku pada hari Senin hingga Jumat.
--timestart 08:00: Waktu mulai aturan, dalam contoh ini pukul 08:00.
--timestop 16:00: Waktu berakhir aturan, dalam contoh ini pukul 16:00.
Jika waktu saat ini berada dalam rentang waktu dan hari yang ditentukan, aturan ini akan menerima lalu lintas.

iptables -A INPUT -j REJECT
Menambahkan aturan kedua ke rantai INPUT untuk menolak semua lalu lintas yang tidak sesuai dengan aturan pertama.

#### Testing
![image](https://github.com/gustino7/Jarkom-Modul-5-E20-2023/assets/93267604/854b11ca-5fc8-4350-9995-3db8e0315633)
![image](https://github.com/gustino7/Jarkom-Modul-5-E20-2023/assets/93267604/983ea25b-9097-44aa-b39e-bf24343a4470)

### Soal 6
Sein & Stark
```
iptables -A INPUT -m time --weekdays Mon,Tue,Wed,Thu --timestart 12:00 --timestop 13:00 -j REJECT
iptables -A INPUT -m time --weekdays Fri --timestart 11:00 --timestop 13:00 -j REJECT
```
iptables -A INPUT -m time --weekdays Mon,Tue,Wed,Thu --timestart 12:00 --timestop 13:00 -j REJECT
Pengaturan waktu:
--weekdays Mon,Tue,Wed,Thu: Aturan ini berlaku pada hari Senin hingga Kamis.
--timestart 12:00: Waktu mulai aturan, dalam contoh ini pukul 12:00.
--timestop 13:00: Waktu berakhir aturan, dalam contoh ini pukul 13:00.
Aturan ini akan menolak lalu lintas selama rentang waktu tersebut pada hari Senin hingga Kamis.

iptables -A INPUT -m time --weekdays Fri --timestart 11:00 --timestop 13:00 -j REJECT
Pengaturan waktu:
--weekdays Fri: Aturan ini berlaku pada hari Jumat.
--timestart 11:00: Waktu mulai aturan, dalam contoh ini pukul 11:00.
--timestop 13:00: Waktu berakhir aturan, dalam contoh ini pukul 13:00.
Aturan ini akan menolak lalu lintas selama rentang waktu tersebut pada hari Jumat.

#### Testing
![image](https://github.com/gustino7/Jarkom-Modul-5-E20-2023/assets/93267604/14bb4e1b-3f51-4cb0-889a-edb41dd35d8a)
![image](https://github.com/gustino7/Jarkom-Modul-5-E20-2023/assets/93267604/7ae420c2-0636-41f4-8776-2fa9e5c0ed9b)
![image](https://github.com/gustino7/Jarkom-Modul-5-E20-2023/assets/93267604/c82b93d4-5252-47f5-a90c-d4c0f32e4c54)

### Soal 7
Heiter
```
iptables -A PREROUTING -t nat -p tcp --dport 80 -d 192.216.4.2 -m statistic --mode nth --every 2 --packet 0 -j DNAT --to-destination 192.216.4.2
iptables -A PREROUTING -t nat -p tcp --dport 80 -d 192.216.4.2 -j DNAT --to-destination 192.216.0.6
iptables -A PREROUTING -t nat -p tcp --dport 443 -d 192.216.0.6 -m statistic --mode nth --every 2 --packet 0 -j DNAT --to-destination 192.216.0.6
iptables -A PREROUTING -t nat -p tcp --dport 443 -d 192.216.0.6 -j DNAT --to-destination 192.216.4.2
```
Aturan-aturan ini digunakan untuk mengarahkan lalu lintas TCP pada port 80 dan 443 ke alamat IP tujuan yang berbeda, dengan mempertimbangkan pola khusus (setiap paket kedua).

#### Testing
testing di Sein & Stark:
1.
while true; do nc -l -p 80 -c 'echo "ini sein"'; done
while true; do nc -l -p 80 -c 'echo "ini stark"'; done
nc 192.216.4.2 80
![image](https://github.com/gustino7/Jarkom-Modul-5-E20-2023/assets/93267604/e000248e-1430-461f-8e89-91e6efff4f34)

2.
while true; do nc -l -p 443 -c 'echo "ini sein"'; done
while true; do nc -l -p 443 -c 'echo "ini stark"'; done
nc 192.216.0.6 443
![image](https://github.com/gustino7/Jarkom-Modul-5-E20-2023/assets/93267604/bcefe70d-e94d-42ae-9068-28022a25ac4c)

### Soal 8
Sein & Stark
```
iptables -A INPUT -p tcp --dport 80 -s 192.216.0.16/30 -m time --datestart 2023-12-10 --datestop 2024-02-15 -j REJECT
iptables -A INPUT -s 192.216.0.16/30 -m time --datestart 2023-12-10 --datestop 2024-02-15 -j REJECT
```
```iptables -A INPUT -p tcp --dport 80 -s 192.216.0.16/30 -m time --datestart 2023-12-10 --datestop 2024-02-15 -j REJECT ```
Mengatur aturan agar hanya berlaku pada rentang waktu mulai dari 10 Desember 2023 hingga 15 Februari 2024. Untuk menolak lalu lintas TCP pada port 80.

```iptables -A INPUT -s 192.216.0.16/30 -m time --datestart 2023-12-10 --datestop 2024-02-15 -j REJECT```
Aturan ini juga menambahkan aturan ke rantai INPUT untuk menolak lalu lintas dari alamat IP dalam subnet 192.216.0.16/30.
Pengaturan waktu yang sama diterapkan untuk membatasi aturan agar hanya berlaku pada rentang waktu tertentu, mulai dari 10 Desember 2023 hingga 15 Februari 2024.

#### Testing
![image](https://github.com/gustino7/Jarkom-Modul-5-E20-2023/assets/93267604/98f86031-3128-4e58-9e6b-3984bc793619)
![image](https://github.com/gustino7/Jarkom-Modul-5-E20-2023/assets/93267604/75ca9777-2253-4c2d-ae02-5068c5dfe00b)
![image](https://github.com/gustino7/Jarkom-Modul-5-E20-2023/assets/93267604/790b954d-d5b3-43ae-9dc2-59cb12781044)

### Soal 9
Sein & Stark
```
iptables -N scan_port

iptables -A INPUT -m recent --name scan_port --update --seconds 600 --hitcount 20 -j REJECT
iptables -A FORWARD -m recent --name scan_port --update --seconds 600 --hitcount 20 -j REJECT

iptables -A INPUT -m recent --name scan_port --set -j ACCEPT
iptables -A FORWARD -m recent --name scan_port --set -j ACCEPT
```
```iptables -N scan_port``` Ini membuat rantai khusus bernama portscan. Rantai ini nantinya dapat digunakan untuk mengelola aturan-aturan terkait dengan deteksi port scanning.
-m recent --name scan_port: Menggunakan modul recent untuk melacak koneksi atau paket.
--update: Mengupdate informasi tentang paket terkini.
--seconds 600: Menetapkan waktu dalam detik, dalam hal ini 600 detik (10 menit).
--hitcount 20: Menetapkan jumlah hit (pembaruan) yang diperlukan untuk memicu aksi selanjutnya.
-j DROP: Menentukan tindakan yang diambil jika kriteria aturan terpenuhi, dalam hal ini menolak (DROP) paket.

#### Testing
![image](https://github.com/gustino7/Jarkom-Modul-5-E20-2023/assets/93267604/0f926f55-635c-4ee6-b24f-47e85ab4690b)
![image](https://github.com/gustino7/Jarkom-Modul-5-E20-2023/assets/93267604/a63fd6ac-b694-428f-adb7-628705ffbe1a)

### Soal 10
```
iptables -I INPUT -m recent --name portscan --update --seconds 600 --hitcount 20 -j LOG --log-prefix "Portscan detected: " --log-level 4
iptables -I FORWARD -m recent --name portscan --update --seconds 600 --hitcount 20 -j LOG --log-prefix "Portscan detected: " --log-level 4
```

```LOG --log-prefix "Portscan detected: " --log-level 4``` bertujuan untuk mengarahkan paket yang memenuhi aturan untuk dilakukan logging.
```-j LOG```: digunakan untuk melakukan logging.
```--log-prefix "Portscan detected: "```: digunakan untuk menambahkan prefix kedalam log yaitu teks "Portscan detected: {isi log}".
```--log-level 4```: menentukan tingakatan atau level log pada syslog, dalam hal ini level 4 berarti 'Warning'.
Karena pada log sebelumnya kita menentukan level log 4 (warning), selanjutnya kita perlu melakukan konfigurasi pada etc/rsyslog.d/50-default.conf untuk menambahkan configurasi ```kernel.warning- /var/log/iptables.log``` sehingga seperti configurasi dibawah ini
```sh

#
# First some standard log files.  Log by facility.
#
auth,authpriv.*                 /var/log/auth.log
*.*;auth,authpriv.none          -/var/log/syslog
#cron.*                         /var/log/cron.log
#daemon.*                       -/var/log/daemon.log
kern.*                          -/var/log/kern.log
kernel.warning                  -/var/log/iptables.log
#lpr.*                          -/var/log/lpr.log
mail.*                          -/var/log/mail.log
#user.*                         -/var/log/user.log

#
# Logging for the mail system.  Split it up so that
# it is easy to write scripts to parse these files.
#
#mail.info                      -/var/log/mail.info
#mail.warn                      -/var/log/mail.warn
mail.err                        /var/log/mail.err
```
jika sudah kita perlu melakukan menjalankan command ```touch /var/log/iptables.log``` dan menjalankan ```/etc/init.d/rsyslog restart``` untuk melakukan restart syslog supaya konfigurasi baru dapat diterapkan kedalam syslog dan hasil log bisa masuk kedalam iptables.log
