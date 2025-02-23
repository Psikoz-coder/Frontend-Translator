
# 🌍 Frontend Translator

## 📌 Amaç

Frontend Translator, HTML sayfalarındaki metinleri dinamik olarak çevirmek için geliştirilmiş basit ve esnek bir çeviri sistemidir. Web projelerinde birden fazla dili desteklemek isteyenler için hızlı ve pratik bir çözüm sunar.

**Öne çıkan amaçlar:**
- Manuel çeviri ihtiyacını ortadan kaldırır.
- Sayfa yenilemeden dil değişimini sağlar.
- Kolayca yeni diller ekleyebilmenizi sağlar.
- JSON formatı ile esnek çeviri yönetimi sunar.

---

## 🔥 Özellikler

- **✅ JSON Tabanlı Çeviri:** Çeviri metinleri `translate.json` dosyasından çekilir.
- **✅ Dinamik Dil Değişimi:** Kullanıcı bir dile geçtiğinde anında çeviri yapılır.
- **✅ Birden Fazla Sayfa Desteği:** Farklı HTML sayfaları için çeviri tanımlayabilirsiniz.
- **✅ Kolay Entegrasyon:** `script.js` dosyanızı ekleyerek hızlıca kullanabilirsiniz.
- **✅ Yerel Depolama Desteği:** Kullanıcının seçtiği dil tarayıcıda saklanır, sayfa yenilendiğinde dil kaybolmaz.
- **✅ Esnek Kullanım:** `h1`, `h2`, `p`, `button`, `title` gibi tüm HTML etiketleriyle uyumludur.
- **✅ Hafif ve Performanslı:** Sadece JavaScript ve JSON kullanarak çalışır, ekstra kütüphane gerektirmez.

---

## 🌟 Neden Kullanmalısınız?

- **✔ Kod yazmadan çok dilli destek ekleyin.**
- **✔ Performanslı ve hafif yapı.**
- **✔ Kolayca yeni diller ekleyebilirsiniz.**
- **✔ Hızlı, pratik ve her projeye entegre edilebilir.**

---

## 🚀 Frontend Translator Kullanım Kılavuzu

### 1️⃣ `script.js` Dosyasını Projeye Dahil Edin

`script.js` dosyasını projenize dahil etmek için:

**Yöntem 1:** `script.js` dosyasını projenize kopyalayın.

**Yöntem 2:** Projeyi klonlayın:

```bash
git clone https://github.com/Psikoz-coder/Frontend-Translator.git
cd Frontend-Translator
```

HTML dosyanızın sonuna ekleyin:

```html
<script src="script.js"></script>
```

---

### 2️⃣ `translate.json` Dosyanızı Oluşturun

Ana dizinde `translate.json` dosyasını oluşturup aşağıdaki formatta düzenleyin:

```json
{
  "/index.html": {
    "tr": {
      "h1": "Ana Sayfaya Hoş Geldiniz!",
      "p1": "Bu bir test paragrafıdır."
    },
    "en": {
      "h1": "Welcome to the Homepage!",
      "p1": "This is a test paragraph."
    }
  }
}
```

**📌 Dikkat:** `"/index.html"` çevirilecek sayfanın yoludur. Farklı sayfalar ekleyebilirsiniz!

---

### 3️⃣ HTML Etiketlerine `data-key` Ekleyin

Çeviri yapılacak öğelere `class="translate"` ve `data-key` ekleyin:

```html
<h1 class="translate" data-key="h1">Ana Sayfaya Hoş Geldiniz!</h1>
<p class="translate" data-key="p1">Bu bir test paragrafıdır.</p>
```

**📌 `data-key` değerleri, `translate.json` içindeki anahtarlarla aynı olmalıdır!**

---

### 4️⃣ Dil Seçim Butonlarını Ekleyin

```html
<div id="translate-buttons">
    <button class="translate-btn" data-lang="tr">🇹🇷 Türkçe</button>
    <button class="translate-btn" data-lang="en">🇬🇧 English</button>
</div>
```

**📌 Butonlara tıkladığınızda sayfanın dili değişecektir.**

---

## 🎯 Ekstra Örnekler

- **✅ Özel bir `data-key` ile çalışır:**

```json
"tr": {
  "psikoz": "PsikOz-coder tarafından yapıldı"
},
"en": {
  "psikoz": "by PsikOz-coder"
}
```

```html
<span class="translate" data-key="psikoz">PsikOz-coder tarafından yapıldı</span>
```

- **✅ Sayfa başlığını bile çevirebilirsiniz!**

```json
"tr": { "title": "Ana Sayfa" },
"en": { "title": "Home Page" }
```

```html
<title class="translate" data-key="title">Ana Sayfa</title>
```

**🚀 Bu adımları tamamladıktan sonra çeviri sistemi çalışacaktır!**
