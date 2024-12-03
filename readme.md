# Exercise 4: Understanding Task Behavior with Priority Preemptive Scheduling

Latihan ini dirancang untuk menunjukkan bagaimana penjadwalan preemptive berdasarkan prioritas mempengaruhi perilaku tugas (task) dalam sistem multitasking. Melalui simulasi ini, kita dapat melihat efek dari preemption atau penghentian sementara yang terjadi ketika tugas dengan prioritas lebih tinggi menginterupsi tugas dengan prioritas lebih rendah.

## Tujuan
- Memahami dampak dari penjadwalan preemptive terhadap runtime tugas.
- Melihat bagaimana tugas prioritas tinggi dapat mengganggu tugas prioritas rendah, serta dampak visualnya melalui pola nyala LED.
- Memahami pentingnya manajemen waktu dan prioritas dalam sistem multitasking real-time.

## Deskripsi Proyek

Pada latihan ini, kita memiliki dua tugas:
1. **FlashGreenLedTask** - Mengontrol LED Hijau dan Biru.
2. **FlashRedLedTask** - Mengontrol LED Merah dan Oranye.

### Rincian Tugas
- **FlashGreenLedTask**
  - **Periode**: 10 detik.
  - **Waktu Eksekusi**: 4 detik.
  - **Indikator LED**: LED Hijau berkedip selama tugas aktif, LED Biru menyala saat tugas dalam status "siap" atau "aktif".

- **FlashRedLedTask**
  - **Periode**: 2 detik.
  - **Waktu Eksekusi**: 0,5 detik.
  - **Indikator LED**: LED Merah berkedip selama tugas aktif, LED Oranye menyala saat tugas dalam status "siap" atau "aktif".

### Perilaku Preemptive
Ketika kedua tugas berjalan bersamaan:
- `FlashRedLedTask` memiliki prioritas lebih tinggi daripada `FlashGreenLedTask`.
- Setiap kali `FlashRedLedTask` aktif, ia akan **menginterupsi** `FlashGreenLedTask`, menyebabkan LED Hijau berhenti berkedip dan berada dalam status "steady" (tetap menyala atau mati).
- Pola ini menunjukkan **preemption**, di mana tugas dengan prioritas lebih tinggi mengambil alih CPU, sehingga tugas prioritas rendah ditunda hingga tugas prioritas tinggi selesai.

### Instalasi

1. **Clone repositori ini**:
   ```bash
   git clone https://github.com/username/repository.git
2. Buka Proyek di IDE: Pastikan proyek ini dibuka pada IDE yang mendukung pemrograman mikroprosesor dan RTOS, seperti STM32CubeIDE atau Keil uVision.

3. Konfigurasi dan Atur Prioritas Tugas:
   Konfigurasikan FlashRedLedTask dengan prioritas lebih tinggi dari FlashGreenLedTask.
4. Kompilasi dan Unduh ke Sistem Target:
   Pastikan tugas dijalankan sesuai dengan konfigurasi di atas, dengan prioritas FlashRedLedTask lebih tinggi.

### Demo



https://github.com/user-attachments/assets/ccd7f922-e0e1-4c19-a518-aed9eaa8727f

