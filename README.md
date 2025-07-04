
<!DOCTYPE html>
<html lang="tr">
<head>
  <meta charset="UTF-8">
  <title>Hobi Öneri Sistemi</title>
</head>
<body>
  <h1>Hobi Öneri Sistemine Hoş Geldiniz!</h1>
  <p>Yaşadığınız yer, gelir düzeyiniz ve günlük rutininize göre size en uygun hobileri öneriyoruz.</p>
</body>
</html>body {
  font-family: Arial, sans-serif;
  background: #f2f2f2;
  padding: 20px;
}

.container {
  background: white;
  padding: 30px;
  max-width: 600px;
  margin: auto;
  border-radius: 10px;
  box-shadow: 0 0 10px #ccc;
}

form label {
  display: block;
  margin-bottom: 15px;const hobiVerileri = {
  dusuk: {
    az: ["Kitap okuma", "Günlük tutma", "Küçük ev egzersizleri"],
    orta: ["Boyama", "Makrome yapımı", "Origami"],
    cok: ["Ahşap oymacılığı", "Ev yapımı takı", "Online kurslar"]
  },
  orta: {
    az: ["Blog yazmak", "Fotoğraf düzenleme"],
    orta: ["Yürüyüş", "Podcast üretmek"],
    cok: ["Bisiklete binmek", "Müzik aleti öğrenmek"]
  },
  yuksek: {
    az: ["Tavla oynamak", "Youtube'da bilgi videoları izlemek"],
    orta: ["Tenis", "Dijital sanat"],
    cok: ["Kampçılık", "Yelken sporu", "Yabancı dil öğrenmek"]
  }
};
}

input, select, button {
  width: 100%;
  padding: 8px;
  margin-top: 5px;
}

button {
  background-color: #0077cc;
  color: white;
  border: none;
  cursor: pointer;
  margin-top: 10px;
}

#oneriler {const hobiVerileri = {
  dusuk: {
    az: ["Kitap okuma", "Günlük tutma", "Küçük ev egzersizleri"],
    orta: ["Boyama", "Makrome yapımı", "Origami"],
    cok: ["Ahşap oymacılığı", "Ev yapımı takı", "Online kurslar"]
  },
  orta: {
    az: ["Blog yazmak", "Fotoğraf düzenleme"],
    orta: ["Yürüyüş", "Podcast üretmek"],
    cok: ["Bisiklete binmek", "Müzik aleti öğrenmek"]
  },
  yuksek: {
    az: ["Tavla oynamak", "Youtube'da bilgi videoları izlemek"],
    orta: ["Tenis", "Dijital sanat"],
    cok: ["Kampçılık", "Yelken sporu", "Yabancı dil öğrenmek"]
  }
};document.getElementById("hobiForm").addEventListener("submit", function(e) {
  e.preventDefault();
  const maas = e.target.maas.value;
  const zaman = e.target.zaman.value;

  const hobiler = hobiVerileri[maas][zaman];
  const sonucAlani = document.getElementById("oneriler");

  sonucAlani.innerHTML = "<h2>Önerilen Hobiler:</h2><ul>" + 
    hobiler.map(hobi => <li>${hobi}</li>).join("") +
    "</ul>";
});# 🎯 Hobi Öneri Sistemi

Bu proje, insanların yaşadığı şehir, meslek, maaş aralığı ve günlük rutinleri gibi bilgileri girerek *kişiselleştirilmiş hobi önerileri* alabilecekleri basit ama işlevsel bir web uygulamasıdır.

---

## 🔍 Nedir Bu Proje?

Herkesin farklı bir yaşam tarzı ve boş vakitleri var. Bu site, kullanıcının hayat şartlarına göre zaman geçirebileceği yeni hobiler önerir.

### 🔢 Kullanıcıdan Alınan Bilgiler:
- Yaşadığı şehir
- Mesleği
- Maaş aralığı
- Günlük boş zamanı
- Tercih edilen ortam (ev, doğa, sosyal, vs.)

### 🎁 Sonuç:
Bu bilgilere göre uygun hobiler listelenir. Örneğin:
- Düşük bütçe + ev ortamı → Origami, boyama
- Doğa + yüksek boş zaman → Doğa yürüyüşü, kampçılık

---

## 🧩 Kullanılan Teknolojiler

- HTML5
- CSS3
- JavaScript (Vanilla)
- GitHub (versiyon kontrolü ve barındırma)
- Netlify (canlıya alma)

---

## 📁 Proje Klasör Yapısı
  margin-top: 20px;
}
