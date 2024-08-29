# BAB I - PENDAHULUAN

## 1.1. Tujuan Praktikum
- Mengetahui prosedur instalasi pada sistem operasi Linux.
- Mampu menjalankan instalasi melalui Graphic User Interface (GUI) maupun Command Line Linux.
- Mampu menganalisis proses instalasi.

## 1.2. Alat yang Digunakan
1. Laptop
2. Sistem Operasi Linux/Ubuntu
3. Virtual Machine

# BAB II - PEMBAHASAN

## 2.1 Proses Instalasi
Saya hanya memasukkan bukti telah menginstall VMware dan Linux/Ubuntu, dan saya juga telah mengikuti prosedur instalasi yang terdapat pada modul.

## 2.2 Analisis / pada opsi mount point
Pada sistem operasi Linux, direktori root (`/`) adalah direktori tertinggi dalam hierarki sistem. Jika kita tidak memilih root sebagai mount point, maka sistem operasi tidak tahu akan memulai dari mana hierarki file sistemnya.

## 2.3 Penjelasan tentang ext4, ext3, swap, ntfs, fat32, btrfs

### 1. ext4 (Fourth Extended Filesystem)
- **Jenis:** Sistem berkas (Filesystem)
- **Platform:** Linux
- **Keterangan:**
  - ext4 adalah penerus dari ext3 dan menawarkan perbaikan kinerja, pengurangan fragmentasi, dan dukungan untuk volume dan file yang lebih besar.
  - Ini mendukung file hingga 16 TB dan partisi hingga 1 EB (exabyte).
  - ext4 juga memiliki fitur journaling yang membantu mengurangi risiko kerusakan data selama pemadaman listrik atau crash sistem.

### 2. ext3 (Third Extended Filesystem)
- **Jenis:** Sistem berkas (Filesystem)
- **Platform:** Linux
- **Keterangan:**
  - ext3 adalah pendahulu dari ext4 dan juga mendukung fitur journaling.
  - Ini memastikan integritas data dengan mencatat perubahan sebelum diterapkan.
  - Namun, ext3 memiliki keterbatasan pada ukuran file (hingga 2 TB) dan kinerja yang lebih rendah dibandingkan ext4.

### 3. Swap
- **Jenis:** Partisi khusus (Partition)
- **Platform:** Linux, Unix
- **Keterangan:**
  - Swap bukan sistem berkas tetapi partisi khusus yang digunakan oleh Linux untuk menambah memori fisik (RAM) dengan menyediakan ruang pada disk sebagai memori virtual.
  - Ketika RAM hampir habis, sistem akan menggunakan swap space ini untuk memindahkan data dari RAM ke disk sementara, yang memungkinkan operasi terus berjalan meskipun dengan kinerja yang lebih lambat.

### 4. NTFS (New Technology File System)
- **Jenis:** Sistem berkas (Filesystem)
- **Platform:** Windows
- **Keterangan:**
  - NTFS adalah sistem berkas standar untuk sistem operasi Windows modern.
  - Ini mendukung fitur-fitur seperti enkripsi, kompresi file, kontrol akses, dan pemulihan kesalahan.
  - NTFS dirancang untuk mendukung file dan partisi yang sangat besar serta memiliki fitur journaling untuk menjaga integritas data.

### 5. FAT32 (File Allocation Table 32)
- **Jenis:** Sistem berkas (Filesystem)
- **Platform:** Windows, Linux, macOS
- **Keterangan:**
  - FAT32 adalah sistem berkas yang lebih tua dan sangat kompatibel dengan hampir semua sistem operasi.
  - Ini sering digunakan pada perangkat penyimpanan portabel seperti USB drive dan kartu SD.
  - Keterbatasannya termasuk ukuran file maksimum 4 GB dan ukuran partisi maksimum 2 TB.

### 6. Btrfs (B-tree File System)
- **Jenis:** Sistem berkas (Filesystem)
- **Platform:** Linux
- **Keterangan:**
  - Btrfs adalah sistem berkas Linux yang dikembangkan untuk menyediakan fitur-fitur canggih seperti snapshotting, subvolume, checksumming data dan metadata, serta manajemen penyimpanan yang lebih fleksibel.
  - Btrfs dirancang untuk menjadi alternatif yang lebih modern dan fleksibel dibandingkan ext4, meskipun ext4 masih lebih banyak digunakan dalam lingkungan produksi.
