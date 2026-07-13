### 🌐 Language / Dil: &nbsp; 🇬🇧 [English](README.md) &nbsp; | &nbsp; 🇹🇷 [Turkish](README.tr.md)

---

# 🛠️ Digistump / ATtiny85 Kart Yöneticisi Yedeği (Backup)

Bu depo, ATtiny85 ve ilgili geliştirme kartları için Digistump Arduino Kart Yöneticisi (Board Manager) yapılandırmasının kalıcı, bağımsız bir kopyasını barındırır.

### ❓ Bu Depo Neden Var?
Orijinal Digistump altyapısı ve buna bağlı harici dosya sunucuları (örneğin `arduino.esp8266.com`), zamanla bağlantı çürümesine (**link rot**) uğramıştır. Derleyici araç zincirlerine (toolchains), cihaz ikili dosyalarına ve çekirdek tanımlarına işaret eden orijinal bağlantıların birçoğu artık `404 Not Found` hatası vermekte ve bu durum kartların Arduino IDE üzerinden kurulmasını engellemektedir.

Bu yedek deposu, gerekli olan **45 adet çekirdek arşiv dosyasının tamamını** doğrudan GitHub Release varlıkları (Assets) olarak yerel olarak barındırıp yamalanmış bir `package_digistump_index.json` dosyası sunarak sorunu tamamen çözer.

---

### 🚀 Nasıl Kullanılır?

#### 🔌 1. Sürücü Kurulumu (Yalnızca Windows)
Windows işletim sistemi kullanıyorsanız, derleme ve yükleme döngüleri sırasında işletim sisteminizin ATtiny85 micronucleus önyükleyicisi (bootloader) ile iletişim kurabilmesi için düşük seviyeli USB sürücülerine ihtiyacı vardır:

1. Bu deponun **Releases** (Yayınlar) sekmesine gidin.
2. [📦 Digistump.Drivers.zip](https://github.com/appdevmon/attiny85-board-backup/releases/download/v1.0/Digistump.Drivers.zip) arşiv dosyasını indirin.
3. ZIP dosyasının içeriğini bir klasöre çıkarın ve sürücüleri kaydetmek için `Install Drivers.exe` dosyasını çalıştırın.

#### ⚙️ 2. Arduino IDE Ortam Kurulumu
Arduino geliştirme ortamınızı doğrudan bu güvenilir yedek sunucuya yönlendirmek için:

1. **Arduino IDE** uygulamasını açın.
2. **Dosya** ➡️ **Tercihler** (Preferences) yolunu izleyin.
3. **Ek Kart Yöneticisi URL'leri** (Additional Boards Manager URLs) metin alanına aşağıdaki doğrudan bağlantıyı yapıştırın:
   ```text
   [https://raw.githubusercontent.com/appdevmon/attiny85-board-backup/main/package_digistump_index.json](https://raw.githubusercontent.com/appdevmon/attiny85-board-backup/main/package_digistump_index.json)
