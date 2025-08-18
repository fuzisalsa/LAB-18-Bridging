# LAB-18-Bridging
tanggal 16 Agustus 

# Bridging

![n](BRIGTP.PNG) 

beberapa interface (eth2, eth3, eth4, eth5) digabungkan dalam satu bridge 
agar semua perangkat berada pada satu network.


**Langkah Konfigurasi Bridging di Mikrotik:**

1. Masuk ke Winbox / Terminal Mikrotik
2. buat interface Bridge

    /interface bridge add name=bridge1

3. tambahkan Port ke Bridge
   
   /interface bridge port add bridge=bridge1 interface=eth2.   
   /interface bridge port add bridge=bridge1 interface=eth3.     
   /interface bridge port add bridge=bridge1 interface=eth4.     
   /interface bridge port add bridge=bridge1 interface=eth5.     
   
4. berikan IP Address pada Bridge

   /ip address add address=192.168.x.1/24 interface=bridge1

5. Cek Status

   /interface bridge print     
   /interface bridge port print
   

# Kesimpulan
Bridging di Mikrotik menghubungkan beberapa port fisik ke dalam satu segment 
jaringan sehingga perangkat yang terhubung dapat berkomunikasi,
yang dapat di hubungkan melalui switch.
