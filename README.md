# AI_Face_Swap_Roop

## <img width="451" alt="Image" src="https://github.com/user-attachments/assets/1e086436-2d25-4b65-b1e7-8ab964c858e5" />

## with
 https://github.com/s0md3v/roop

-------------------------------------------------------------------------------------------------------------------------
# 🤖 AI Face Swap with Roop

Bu proje, komut satırı üzerinden çalışan Roop tabanlı bir AI yüz değiştirme sistemidir. Görseller ve videolar üzerinde yüz değişimi yapar ve esnek parametre desteği ile özelleştirilebilir çıktılar sunar.

---

## 📦 Kurulum

### 1. Bu projeyi bilgisayarınıza klonlayın:
```
git clone https://github.com/ahmettsimsek/AI_Face_Swap_Roop.git
```
```
cd AI_Face_Swap_Roop/roop
```

### 2. Roop klasörüne girin:
```
cd roop
```
3. Gerekli bağımlılıkları yükleyin:
```
pip install -r requirements.txt
```
4. Model dosyasını indirin:
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



![Image](https://github.com/user-attachments/assets/1acbe331-f05e-4598-8c9a-3cd4cabfc0b2)

![Image](https://github.com/user-attachments/assets/4b8407a6-df78-44fa-904c-1bf8c0378e19)

![Image](https://github.com/user-attachments/assets/46ab75d1-2849-4156-83d7-fc8c16e20461)


