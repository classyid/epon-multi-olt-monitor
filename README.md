# 🌐 EPON Multi-OLT Monitor

<div align="center">

![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)
![License](https://img.shields.io/badge/License-MIT-green.svg)
![Status](https://img.shields.io/badge/Status-Production%20Ready-brightgreen.svg)
![Monitoring](https://img.shields.io/badge/Monitoring-Real--time-orange.svg)

**Sistem monitoring real-time untuk Multiple OLT EPON/GPON dengan notifikasi WhatsApp otomatis**

[Demo](#-demo) • [Instalasi](#-instalasi-cepat) • [Dokumentasi](#-dokumentasi) • [Kontribusi](#-kontribusi)

</div>

---

## 🎯 Tentang Project

**EPON Multi-OLT Monitor** adalah solusi monitoring jaringan fiber optik yang powerful dan user-friendly, dirancang khusus untuk Internet Service Provider (ISP) dan operator telekomunikasi di Indonesia. Sistem ini dapat memonitor multiple perangkat OLT secara bersamaan dan memberikan notifikasi real-time via WhatsApp ketika terjadi gangguan jaringan.

### 🌟 Mengapa Memilih Solusi Ini?

- **⚡ Real-time Monitoring** - Deteksi gangguan dalam hitungan detik
- **📱 WhatsApp Integration** - Notifikasi langsung ke HP Anda
- **🔄 Multi-OLT Support** - Monitor semua OLT dari satu dashboard
- **🛡️ Recovery Detection** - Otomatis detect ketika jaringan pulih
- **📊 Detailed Analytics** - Analisis mendalam setiap ONU
- **🚀 Easy Deployment** - Setup dalam 5 menit

---

## ✨ Fitur Utama

### 🔍 **Real-time Network Monitoring**
- Monitor status semua ONU (Online/Down/PwrDown) 
- Tracking perubahan status secara real-time
- Analisis signal strength (RX Power, Temperature)
- Distance calculation dan RTT monitoring

### 📱 **Smart WhatsApp Notifications**
- Instant alert untuk setiap gangguan
- Recovery notification dengan detail lengkap
- Hourly status report otomatis
- Customizable message format

### 🔧 **Multi-OLT Management**
- Support unlimited jumlah OLT
- Concurrent monitoring untuk performa optimal
- Centralized configuration management
- Individual OLT status tracking

### 📊 **Advanced Analytics**
- Historical data storage
- Trend analysis dan reporting
- Downtime calculation
- Performance metrics

---

## 🚀 Instalasi Cepat

### Persyaratan Sistem
```bash
- Python 3.8+
- RAM: 2GB minimum (4GB recommended)
- Storage: 10GB minimum
- Network: Akses ke OLT dan internet untuk WhatsApp API
```

### Step 1: Clone Repository
```bash
git clone https://github.com/classyid/epon-multi-olt-monitor.git
cd epon-multi-olt-monitor
```

### Step 2: Setup Environment
```bash
# Buat virtual environment
python3 -m venv venv
source venv/bin/activate  # Linux/Mac
# atau venv\Scripts\activate untuk Windows

# Install dependencies
pip install -r requirements.txt
```

### Step 3: Konfigurasi
```bash
# Copy contoh konfigurasi
cp config.example.py config.py

# Edit konfigurasi sesuai kebutuhan
nano config.py
```

### Step 4: Jalankan
```bash
# Test koneksi
python test_connection.py

# Mulai monitoring
python epon_monitor.py
```

🎉 **Selamat! Sistem monitoring Anda sudah berjalan!**

---

## ⚙️ Konfigurasi

### Konfigurasi OLT
```python
olt_configs = [
    {
        'id': 'OLT-JAKARTA-01',
        'name': 'OLT Jakarta Pusat', 
        'url': 'http://192.168.1.100:88',
        'username': 'admin',
        'password': 'password123'
    },
    {
        'id': 'OLT-BANDUNG-01',
        'name': 'OLT Bandung Timur',
        'url': 'http://192.168.1.101:88', 
        'username': 'admin',
        'password': 'password456'
    }
    # Tambahkan OLT lainnya...
]
```

### Konfigurasi WhatsApp
```python
whatsapp_config = {
    'api_url': "https://kirimwa.classy.id/send-message",
    'api_key': "YOUR_API_KEY_HERE",
    'sender': "6281234567890",      # Nomor pengirim
    'recipient': "6281234567891"    # Nomor penerima alert
}
```

### Pengaturan Monitoring
```python
MONITOR_INTERVAL = 10    # Check setiap 10 detik
HOURLY_REPORT = True     # Aktifkan laporan per jam
DEBUG_MODE = False       # Mode debug untuk troubleshooting
```

---

## 📱 Contoh Notifikasi WhatsApp

### 🚨 Alert Gangguan
```
🚨 EPON MULTI-OLT STATUS ALERT 🚨

⏰ Time: 2024-01-15 14:30:25
🌐 Total OLT Monitored: 3

🏢 OLT Jakarta Pusat (OLT-JAKARTA-01)
──────────────────────────────────────────────
📊 Status: 2 Total Problems
   🔴 DOWN: 1
   🔌 PWRDOWN: 1

🔴 NEW DOWN DETECTED:
🔴 CUSTOMER-OFFICE-PLAZA
   📍 PON: 1/1/1:15
   🔗 MAC: 70:A5:6A:12:34:56
   🚨 Status: Down (Timeout)
   ⚠️ Priority: HIGH
   📏 Jarak: 1250m
   📵 RX: -28.5 dBm
   ❌ Reason: TIMEOUT (Koneksi Terputus)
```

### ✅ Alert Recovery
```
✅ RECOVERY DETECTED:
🟢 CUSTOMER-WARNET-SENTRAL (DOWN → ONLINE)
   📍 PON: 1/1/2:8
   🔗 MAC: 70:A5:6A:78:90:12
   ⏰ Recovery Time: 2024-01-15 14:35:10
   📈 Previous Status: Down (Timeout)
   ⏱️ Was Offline: 5m 15s
   🎉 Network Restored Successfully!
```


## 🤝 Kontribusi

Kami sangat welcome kontribusi dari community! 

### Cara Berkontribusi:
1. **Fork** repository ini
2. **Create branch** untuk fitur baru (`git checkout -b feature/AmazingFeature`)
3. **Commit** perubahan (`git commit -m 'Add: Amazing Feature'`)
4. **Push** ke branch (`git push origin feature/AmazingFeature`)
5. **Open Pull Request**


## 📄 Lisensi

Project ini dilisensikan under **MIT License** - lihat file [LICENSE](LICENSE) untuk detail.

## 🙏 Acknowledgments

- Tim Developer Indonesia yang telah berkontribusi
- Community ISP Indonesia untuk feedback
- Open source libraries yang digunakan

---

## 📞 Support & Contact

### Professional Support
Butuh implementasi enterprise atau custom development?

📧 **Email**: kontak@classy.id  

---

<div align="center">

**⭐ Jangan lupa kasih star jika project ini berguna! ⭐**

Made with ❤️ by Indonesian Developers for Indonesian ISP Community

[⬆ Back to Top](#-epon-multi-olt-monitor)

</div>
