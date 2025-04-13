# AI_Face_Swap_Roop

# 🤖 AI Face Swap with Roop

Bu proje, komut satırı üzerinden çalışan Roop tabanlı bir AI yüz değiştirme sistemidir. Görseller ve videolar üzerinde yüz değişimi yapar ve esnek parametre desteği ile özelleştirilebilir çıktılar sunar.

---

## 📦 Kurulum

### 1. Roop klasörüne girin:
```
cd roop
```
2. Gerekli bağımlılıkları yükleyin:
```
pip install -r requirements.txt
```
3. Model dosyasını indirin:
Aşağıdaki modeli indirip roop dizinine yerleştirin:

inswapper_128.onnx

⚠️ Bu model GitHub'da paylaşılamaz. Lütfen manuel olarak indirin.

🚀 Kullanım
🧪 Temel çalıştırma:

```
python run.py
```
İlk çalıştırmada bazı ek modeller indirilecektir. Bu işlem internet hızınıza bağlı olarak zaman alabilir.

🔍 Örnek Kullanım Senaryoları
🎯 1. Basit Görsel Üzerinde Yüz Değişimi:
bash
Kopyala
Düzenle
```
python run.py -s kaynak.jpg -t hedef.jpg -o cikti.jpg
```
--------------------------------------------------------
-s, --source: Yüz alınacak kaynak görsel
-------------------------------------
-t, --target: Yüzün yapıştırılacağı hedef görsel
------------------------------------
-o, --output: İşlem sonucunda oluşacak çıktı dosyası
------------------------------------

🖼️ 2. PNG Formatında Giriş/Çıkış:

```
python run.py -s kaynak.png -t hedef.png -o cikti.png --temp-frame-format png
```
Bu komut, giriş ve çıkış dosyalarının PNG formatında olmasını sağlar.

Eğer hem kaynak hem hedef PNG ise, çıktı da PNG olur.

🛠️ 3. Gelişmiş Ayarlarla Kullanım (Tavsiye Edilen):

```
python run.py -s kaynak.jpg -t hedef.jpg -o cikti.jpg \
--temp-frame-format jpg \
--temp-frame-quality 100 \
--many-faces \
--keep-frames \
--execution-provider cpu \
--execution-threads 4
```
Parametre Açıklamaları:
--temp-frame-format: Geçici karelerin formatı (jpg, png vs.)

--temp-frame-quality: Görüntü kalitesi (0–100)

--many-faces: Birden fazla yüz varsa hepsini işleme alır

--keep-frames: İşlem sırasında oluşturulan kareleri saklar

--execution-provider: cpu veya cuda (GPU)

--execution-threads: İşlem için kullanılacak CPU çekirdek sayısı

🛎️ Notlar
Program ilk çalıştırmada bazı modelleri otomatik indirir.

Hata alırsanız, terminaldeki mesajları dikkatlice inceleyin.

Daha fazla bilgi için orijinal Roop GitHub sayfasını ziyaret edebilirsiniz.
