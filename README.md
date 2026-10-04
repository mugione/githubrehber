<div align="center">

# 🚀 GitHub’ı Keşfet

## İlk Commit’ten Profesyonel Profile, Açık Kaynaktan Otomasyona

**🎨 Profil · 📖 README · 🤝 Katkı · 💻 Git · ⚡ Actions · 🌐 Pages · 🛡️ Güvenlik**

*GitHub’ı öğrenmek, projelerini anlatmak ve birlikte üretmek isteyenler için 10 bölümlük uygulamalı rehber.*

**🇹🇷 Türkçe · 📅 Ekim 2026**

</div>

---

GitHub’da bir hesap açtınız, birkaç projeye yıldız verdiniz ve belki ilk dosyanızı yüklediniz. Peki bundan sonra ne yapabilirsiniz?

Profilinizi kişisel bir vitrine dönüştürebilir, başka projelere katkı sunabilir, testlerinizi otomatik çalıştırabilir ve kendi web sitenizi yayımlayabilirsiniz. Bu rehberde bu adımları tek bir yolculukta bir araya getiriyoruz.

Her şeyi aynı gün uygulamanız gerekmiyor. Küçük bir proje seçin; okuduğunuz bölümleri o proje üzerinde deneyin. Yazının sonuna geldiğinizde elinizde yalnızca yeni kavramlar değil, geliştirebileceğiniz somut bir çalışma olsun.

> [!NOTE]
> Örneklerdeki `KULLANICI`, `PROJE`, ad ve bağlantılar yer tutucudur; kendi bilgilerinizle değiştirin. Komutlar, Git’in kurulu olduğunu varsayar. GitHub’a gönderim için hesabınızda uygun kimlik doğrulamasını ve depo erişimini ayarlamış olmalısınız.

## 🧭 İçindekiler

| Bölüm | Konu | Kazanım |
| :---: | :--- | :--- |
| 01 | [🧩 GitHub sözlüğü](#bolum-01) | Temel kavramları ayırt et. |
| 02 | [🎨 Etkileyici profil README’si](#bolum-02) | Kendini ve çalışmalarını tanıt. |
| 03 | [📖 İyi bir proje README’si](#bolum-03) | Projeni anlaşılır ve kullanılabilir kıl. |
| 04 | [💻 Günlük işlerde 10 Git komutu](#bolum-04) | Değişikliklerini takip et. |
| 05 | [🚀 İlk pull request](#bolum-05) | Başka bir projeye katkı gönder. |
| 06 | [🤝 Kod yazmadan katkı](#bolum-06) | Bilginle ve gözlemlerinle destek ol. |
| 07 | [🗂️ Issues, Projects ve Releases](#bolum-07) | Fikirlerini planla, sürümünü paylaş. |
| 08 | [⚡ GitHub Actions](#bolum-08) | Tekrarlayan kontrolleri otomatikleştir. |
| 09 | [🌐 GitHub Pages](#bolum-09) | İlk web siteni yayımla. |
| 10 | [🛡️ Kaçınılması gereken 7 güvenlik hatası](#bolum-10) | Hesabını ve projeni koru. |

---

<a name="bolum-01"></a>

## 01 · 🧩 GitHub Sözlüğü: Fork, Star, Watch ve Clone Ne Demek?

Önce iki temel kavramı ayıralım: **Git**, dosya değişikliklerini takip etmek için kullanılan sürüm kontrol sistemidir. **GitHub** ise Git depolarını barındıran ve ortak çalışmayı destekleyen platformdur.

Günlük kullanımda karşınıza en sık şu terimler çıkar:

| Terim | Ne işe yarar? | Kısa örnek |
| :--- | :--- | :--- |
| 📦 **Repository / Repo** | Dosyaları ve değişiklik geçmişini barındıran depo. | Bir görev takip uygulamasının deposu. |
| 🌿 **Branch** | Çalışmayı ayrı bir geliştirme dalında sürdürür. | `feat/arama` dalında arama özelliği geliştirmek. |
| 📸 **Commit** | Seçilen değişiklikleri bir kayıt hâline getirir. | “Arama sonucuna boş durum mesajı ekle.” |
| 🍴 **Fork** | Bir depodan GitHub üzerinde ayrı bir depo oluşturur. | Başkasının projesine katkı hazırlamak. |
| 💻 **Clone** | Depoyu geçmişiyle birlikte bilgisayarınıza kopyalar. | Editörünüzde çalışmak için projeyi indirmek. |
| ⭐ **Star** | İlginizi çeken projeyi kaydetmenizi sağlar. | Daha sonra inceleyeceğiniz aracı işaretlemek. |
| 🔔 **Watch** | Seçtiğiniz etkinlikler için bildirimleri yönetir. | Bir projenin yeni sürümlerini takip etmek. |
| 🔀 **Pull Request / PR** | Değişikliklerin hedef dala alınmasını önerir. | Hata düzeltmesini proje sahibine sunmak. |
| 🧬 **Merge** | Değişiklikleri hedef dala birleştirir. | İncelenen PR’ı ana dala almak. |
| 🐛 **Issue** | Hata, fikir veya yapılacak işi kaydeder. | “Mobil görünümde menü açılmıyor.” |

**En sık karışan ayrım:** Fork, GitHub üzerindeki ayrı deponuzdur; clone, bilgisayarınızdaki yerel kopyadır. Bir projeyi fork edip ardından kendi fork’unuzu bilgisayarınıza clone edebilirsiniz.

📚 [GitHub sözlüğü](https://docs.github.com/en/get-started/learning-about-github/github-glossary)

<a name="bolum-02"></a>

## 02 · 🎨 GitHub Profilini Konuştur: Etkileyici Bir Profil README’si

Profilinize gelen biri birkaç saniye içinde üç şeyi anlayabilsin: **Neler geliştiriyorsunuz, hangi konularla ilgileniyorsunuz ve hangi projenize bakmalı?**

Profil README’sini etkinleştirmek için kullanıcı adınızla aynı adı taşıyan **public** bir depo oluşturun. Bu deponun kök dizinindeki `README.md` dosyası boş olmamalıdır. Örneğin kullanıcı adınız `ornekdev` ise depo `ornekdev/ornekdev` olur. Bu özellik managed user hesaplarında kullanılamaz.

### ✨ Kopyalanabilir başlangıç şablonu

```markdown
# Merhaba, ben ADIN 👋

Web araçları geliştiriyor, öğrendiklerimi küçük projelerle paylaşıyorum.

## 🔭 Şu sıralar
- Üzerinde çalıştığım: PROJE VE KISA AMACI
- Öğrendiğim: KONU
- Katkıya açık olduğum: ALAN

## 🧰 Kullandığım teknolojiler
JavaScript · Python · Git

## 🚀 Öne çıkan çalışmalarım
| Proje | Çözdüğü ihtiyaç |
| --- | --- |
| [Proje adı](https://github.com/KULLANICI/PROJE) | Bir cümlelik açıklama. |

## 📫 Bağlantılar
[Web sitem](https://example.com)
```

Şablondaki teknoloji ve ilgi alanlarını gerçek çalışmalarınızla değiştirin. Her aracı listelemek yerine projelerinizde kullandıklarınızı seçin. Proje açıklamasında “harika uygulama” demek yerine “günlük harcamaları kategorilere ayırır” gibi somut bir işlev anlatın.

🎯 **Tasarım fikri:** Bir ana başlık, kısa tanıtım, seçilmiş projeler ve tek bir iletişim alanıyla başlayın. Eklediğiniz her ikonun veya görselin okunabilirliğe katkısı olsun. Haricî servislerden gelen istatistik kartlarının zaman zaman yüklenmeyebileceğini hesaba katın.

📚 [Profil README’sini yönetme](https://docs.github.com/en/account-and-profile/how-tos/profile-customization/managing-your-profile-readme)

<a name="bolum-03"></a>

## 03 · 📖 Kodun Vitrini: İyi Bir README Nasıl Yazılır?

Profil README’si sizi tanıtır; **proje README’si ise kullanıcının projeyi anlamasını ve çalıştırmasını sağlar**. Depoya ilk kez gelen birinin zihnindeki sorularla başlayın: Bu ne yapıyor? Bana uygun mu? Nasıl denerim?

### 📝 Kopyalanabilir proje şablonu

````markdown
# 📝 Görev Defteri

Günlük görevleri tarayıcıda düzenlemek için küçük bir uygulama.

## 📸 Önizleme
![Uygulamanın görev listesi](docs/ekran-goruntusu.png)

## ✨ Özellikler
- Görev ekleme ve tamamlama
- Tamamlanan görevleri filtreleme

## ⚙️ Gereksinimler
Projeye uygun çalışma ortamını ve sürümünü buraya yazın.

## 🚀 Kurulum
```bash
git clone https://github.com/KULLANICI/PROJE.git
cd PROJE
```
Projeyi çalıştırmak için gereken sonraki komutları buraya ekleyin.

## 💡 Kullanım
İlk görevi nasıl oluşturacağınızı kısa bir örnekle anlatın.

## 🤝 Katkı
Katkıdan önce CONTRIBUTING.md dosyasını okuyun.

## 📄 Lisans
Seçtiğiniz lisansı ve LICENSE dosyasını belirtin.
````

Bu taslağı yayımlamadan önce örnek proje adını ve özellikleri değiştirin. Görseli belirtilen konuma ekleyin; henüz bulunmayan dosyalara yapılan yönlendirmeleri tamamlayın veya kaldırın.

**Küçük bir kalite kontrolü:** Projeyi ilk kez gören bir arkadaşınızdan yalnızca README’yi izleyerek çalıştırmasını isteyin. Size sormak zorunda kaldığı her adım, belgede açıklığa kavuşturulabilecek bir noktadır.

📚 [Depo README dosyaları](https://docs.github.com/en/repositories/managing-your-repositorys-settings-and-features/customizing-your-repository/about-readmes)

<a name="bolum-04"></a>

## 04 · 💻 Terminalden Korkma: Günlük İşini Görecek 10 Git Komutu

Komutları ezberlemek yerine hangi soruya cevap verdiklerini öğrenin. “Ne değişti?”, “Hangi daldayım?” ve “Neyi göndereceğim?” soruları iyi bir başlangıçtır.

| # | Komut | İşlevi |
| :---: | :--- | :--- |
| 1 | `git clone URL` | Var olan depoyu bilgisayarınıza kopyalar. |
| 2 | `git status` | Dalı ve dosyaların çalışma durumunu gösterir. |
| 3 | `git switch -c feat/arama` | Yeni dal oluşturur ve o dala geçer. |
| 4 | `git diff` | Henüz hazırlık alanına alınmamış değişiklikleri gösterir. |
| 5 | `git add README.md` | Dosyanın değişikliklerini commit için hazırlık alanına alır. |
| 6 | `git commit -m "Kurulum adımlarını açıkla"` | Hazırlık alanındaki değişiklikleri kaydeder. |
| 7 | `git log --oneline -5` | Son beş commit’i kısa biçimde listeler. |
| 8 | `git fetch origin` | Uzaktaki güncellemeleri getirir; çalışma dalınızla birleştirmez. |
| 9 | `git pull --ff-only` | İzlenen uzak dalı getirir; yalnızca fast-forward mümkünse mevcut dalı ilerletir. |
| 10 | `git push -u origin feat/arama` | Dalı uzak depoya gönderir ve takip ilişkisini ayarlar. |

💡 `git diff --staged`, commit’e girecek değişiklikleri görmenizi sağlar. `git status` yeni, takip edilmeyen dosyaları da gösterirken `git diff` bunların içeriğini otomatik göstermez.

`git pull --ff-only` ayrışmış geçmiş nedeniyle durursa hata mesajını inceleyin. Sorunu anlamadan zorla gönderim yapmak yerine projenin merge veya rebase yaklaşımını izleyin. Yeni dalınız henüz bir uzak dalı izlemiyorsa önce takip ilişkisini kurmanız gerekir.

📚 [Günlük Git komutları](https://git-scm.com/docs/giteveryday) · [Git pull](https://git-scm.com/docs/git-pull)

<a name="bolum-05"></a>

## 05 · 🚀 İlk Pull Request: Açık Kaynağa Katkının İlk Adımı

İlk katkınız için kapsamı küçük, sonucunu açıklayabildiğiniz bir iş seçin. Kullandığınız bir aracın eksik kurulum açıklamasını tamamlamak iyi bir örnek olabilir.

1. **Projeyi tanıyın.** README’yi ve varsa `CONTRIBUTING.md` dosyasını okuyun.
2. **Mevcut işleri inceleyin.** Aynı sorun için issue veya PR açılmış mı bakın. `good first issue` etiketi başlangıç için yardımcı olabilir.
3. **Yazma yetkiniz yoksa fork oluşturun.** GitHub’daki Fork düğmesini kullanın.
4. **Kendi fork’unuzu clone edin ve dal açın.**

```bash
git clone https://github.com/KULLANICI/PROJE.git
cd PROJE
git switch -c docs/kurulum-aciklamasi
```

5. **Dosyayı düzenleyin.** Açıklamanın doğruluğunu veya kod değişikliğinin davranışını kontrol edin.
6. **Değişikliği inceleyin, kaydedin ve gönderin.**

```bash
git diff
git add README.md
git diff --staged
git commit -m "docs: kurulum adımlarını netleştir"
git push -u origin docs/kurulum-aciklamasi
```

7. **GitHub’dan PR açın.** Hedef depoyu ve dalı doğrulayın; kaynak olarak fork’unuzdaki çalışma dalını seçin.

### ✍️ PR açıklaması için kısa taslak

```markdown
## Neden?
Kurulumda gerekli yapılandırma adımı açıklanmıyordu.

## Ne değişti?
Eksik adım ve örnek ayar dosyası açıklaması eklendi.

## Nasıl kontrol edildi?
Belgelenen adımlar temiz bir ortamda uygulandı.
```

Son bölüme yalnızca gerçekten yaptığınız kontrolü yazın. İnceleyen kişi değişiklik isterse aynı dala yeni commit gönderin; mevcut PR güncellenir. Her düzeltme için yeni PR açmanız gerekmez.

📚 [Bir projeye katkıda bulunma](https://docs.github.com/en/get-started/exploring-projects-on-github/contributing-to-a-project) · [Açık kaynak katkı süreci](https://docs.github.com/en/get-started/exploring-projects-on-github/contributing-to-open-source)

<a name="bolum-06"></a>

## 06 · 🤝 Kod Yazmadan Açık Kaynağa Nasıl Katkı Sağlanır?

Bir projenin işe yaraması, insanların onu anlayabilmesine de bağlıdır. Kurulumda takıldığınız yeri açıklamak veya belirsiz bir hata mesajını belgelemek başka bir kullanıcının saatlerini kurtarabilir.

| Katkı | Somut bir başlangıç |
| :--- | :--- |
| 📚 Dokümantasyon | Eksik kurulum adımını ekran görüntüsüyle açıklayın. |
| 🌍 Çeviri | Projenin çeviri sürecine uygun bir sayfayı Türkçeleştirin. |
| 🐛 Hata bildirimi | Sorunu yeniden üretmek için gereken adımları yazın. |
| 🧪 Kullanıcı testi | Yeni sürümü deneyip beklenen ve gerçekleşen davranışı karşılaştırın. |
| ♿ Erişilebilirlik | Klavyeyle kullanımda karşılaştığınız engeli bildirin. |
| 💬 Topluluk desteği | Daha önce çözdüğünüz bir soruyu kaynak göstererek yanıtlayın. |

### 🔎 Faydalı hata bildirimi örneği

```markdown
## Sorun
Boş görev adıyla kayıt oluşturulabiliyor.

## Tekrarlama adımları
1. Yeni görev ekranını aç.
2. Başlığı boş bırak.
3. Kaydet düğmesine bas.

## Beklenen
Başlığın zorunlu olduğunu belirten mesaj gösterilmesi.

## Gerçekleşen
Listede başlıksız bir görev oluşması.

## Ortam
Uygulama sürümü, işletim sistemi ve tarayıcı sürümü.
```

Örneği kendi gözleminize göre doldurun. Bir ekran görüntüsü veya kısa kayıt ekliyorsanız içindeki kişisel bilgileri temizleyin. Aynı sorunun zaten raporlanıp raporlanmadığını kontrol etmek de katkının bir parçasıdır.

📚 [GitHub’ın katkı rehberi](https://docs.github.com/en/get-started/exploring-projects-on-github/contributing-to-open-source)

<a name="bolum-07"></a>

## 07 · 🗂️ Fikirden Sürüme: Issues, Projects ve Releases

Proje büyüdükçe yapılacakları zihinde tutmak zorlaşır. Bir görevin ne olduğunu, hangi aşamada bulunduğunu ve hangi sürümde yayımlandığını ayrı ayrı takip edin.

| Araç | Cevapladığı soru | Örnek |
| :--- | :--- | :--- |
| 🐛 **Issues** | Ne yapılmalı, neden? | “Görev listesine arama ekle.” |
| 📊 **Projects** | İşler hangi aşamada? | Backlog → In progress → Done. |
| 📦 **Releases** | Hangi sürümde ne yayımlandı? | `v1.1.0`: arama ve filtreleme. |

**Issue**, işin açıklamasını, kabul koşullarını ve tartışmasını taşır. **Projects**, issue ve PR’ları tablo, pano veya yol haritası görünümünde takip etmenizi sağlar. **Release** ise bir Git etiketiyle ilişkili sürüm notlarını ve varsa indirilebilir dosyaları sunar.

### 🧪 Örnek: Görev Defteri’ne arama eklemek

Bir issue açıp “Kullanıcı başlığa göre arayabilmeli; arama temizlenince tüm görevler görünmeli” şeklinde kabul koşulları yazın. İşi panoya ekleyin. Geliştirme PR’ında ilgili issue’ya bağlantı verin. Tamamlandığında yeni sürüm notunda kullanıcı açısından değişen davranışı açıklayın.

```markdown
## v1.1.0

### ✨ Yeni
- Görev başlıklarında arama yapılabiliyor.

### 🐛 Düzeltildi
- Boş başlıkla görev oluşturulması engellendi.

### 📚 Belgeler
- İlk kullanım örnekleri eklendi.
```

Sürüm notunu commit mesajlarının kopyası gibi düşünmeyin. Kullanıcının “Güncellersem ne değişecek?” sorusuna cevap verin.

📚 [Issues](https://docs.github.com/en/issues/tracking-your-work-with-issues/learning-about-issues/about-issues) · [Projects](https://docs.github.com/en/issues/planning-and-tracking-with-projects/learning-about-projects/about-projects) · [Releases](https://docs.github.com/en/repositories/releasing-projects-on-github/about-releases)

<a name="bolum-08"></a>

## 08 · ⚡ GitHub Actions: Tekrarlayan İşleri Otomatiğe Bağla

Her değişiklikten sonra aynı testi elle çalıştırıyorsanız, bunu bir workflow ile otomatikleştirebilirsiniz. GitHub Actions iş akışları `.github/workflows/` dizinindeki YAML dosyalarında tanımlanır.

| Kavram | Anlamı |
| :--- | :--- |
| **Workflow** | Otomasyonun tamamı. |
| **Event** | Çalışmayı başlatan olay; örneğin push veya PR. |
| **Job** | Bir runner üzerinde yürütülen iş. |
| **Step** | İş içindeki komut veya hazır action adımı. |
| **Runner** | İşin çalıştığı ortam. |

### 🧪 Küçük, çalıştırılabilir bir örnek

Depoda `gorev.mjs` dosyası oluşturun:

```javascript
export function gecerliBaslik(baslik) {
  return typeof baslik === 'string' && baslik.trim().length > 0;
}
```

Yanına `gorev.test.mjs` ekleyin:

```javascript
import test from 'node:test';
import assert from 'node:assert/strict';
import { gecerliBaslik } from './gorev.mjs';

test('anlamlı bir görev başlığını kabul eder', () => {
  assert.equal(gecerliBaslik('Kitap oku'), true);
});

test('boş veya yalnızca boşluk içeren başlığı reddeder', () => {
  assert.equal(gecerliBaslik(''), false);
  assert.equal(gecerliBaslik('   '), false);
});
```

Node.js 24 kurulu bir ortamda `node --test` ile testleri çalıştırabilirsiniz. Bu örnek haricî npm paketi gerektirmez.

Şimdi `.github/workflows/test.yml` dosyasını ekleyin:

```yaml
name: Görev testleri

on:
  push:
    branches: [main]
  pull_request:
    branches: [main]

permissions:
  contents: read

jobs:
  test:
    runs-on: ubuntu-latest
    steps:
      - name: Depoyu al
        uses: actions/checkout@v6
        with:
          persist-credentials: false

      - name: Node.js hazırla
        uses: actions/setup-node@v7
        with:
          node-version: '24'

      - name: Testleri çalıştır
        run: node --test
```

Örnek, `main` dalına gönderimde ve `main` hedefli PR’larda çalışır. Ana dalınız farklıysa adını değiştirin. Sonuçları deponun **Actions** sekmesinden inceleyin; başarısız testte ilgili adımın çıktısını okuyun.

Bu akış yalnızca test yapar; otomatik dağıtım gerçekleştirmez. Yayınlama otomasyonu için ayrıca hedef ortam, kimlik doğrulama ve dağıtım adımları tanımlanır. Kalıcı projelerde action sürümlerini doğrulanmış tam commit SHA’sına sabitlemek ek güvence sağlar.

📚 [Actions başlangıcı](https://docs.github.com/en/actions/get-started/quickstart) · [Workflow sözdizimi](https://docs.github.com/en/actions/reference/workflows-and-actions/workflow-syntax) · [Node.js test çalıştırıcısı](https://nodejs.org/api/test.html) · [Güvenli kullanım](https://docs.github.com/en/actions/reference/security/secure-use)

<a name="bolum-09"></a>

## 09 · 🌐 Koddan Web Sitesine: GitHub Pages ile İlk Yayının

Portföyünüz, makaleleriniz veya projenizin tanıtımı için küçük bir site hazırlamak istiyorsanız GitHub Pages’i kullanabilirsiniz. Pages, statik site dosyalarını yayımlar; uygulamanızın sunucu tarafındaki kodunu çalıştıran genel amaçlı bir sunucu değildir.

### 🏗️ Kullanıcı sitesi oluşturma

1. `KULLANICI.github.io` adında **public** bir depo oluşturun.
2. Kök dizine aşağıdaki `index.html` dosyasını ekleyin.
3. **Settings → Pages → Build and deployment** alanına gidin.
4. Kaynak olarak **Deploy from a branch**, dal olarak dosyanızın bulunduğu `main`, klasör olarak **/(root)** seçip kaydedin.
5. Yayın tamamlanınca `https://KULLANICI.github.io` adresini açın. İlk yayının görünmesi biraz zaman alabilir.

```html
<!doctype html>
<html lang="tr">
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>Geliştirici Notlarım</title>
  <style>
    body {
      max-width: 720px;
      margin: 64px auto;
      padding: 0 24px;
      background: #0d1117;
      color: #e6edf3;
      font: 18px/1.7 system-ui, sans-serif;
    }
    a { color: #79c0ff; }
  </style>
</head>
<body>
  <main>
    <h1>🚀 Geliştirici Notlarım</h1>
    <p>Projelerimi, öğrendiklerimi ve rehberlerimi burada paylaşıyorum.</p>
    <a href="https://github.com/KULLANICI">GitHub profilimi ziyaret et</a>
  </main>
</body>
</html>
```

`index.html` dosyasındaki kullanıcı adını değiştirin. Kullanıcı sitesi deposuyla profil README deposu farklıdır: biri `KULLANICI.github.io`, diğeri `KULLANICI` adını taşır.

GitHub Free ile public depolarda Pages kullanılabilir. Bir veritabanı veya gizli API anahtarı gerektiren işleviniz varsa bunlar için ayrı bir sunucu hizmeti gerekir; tarayıcıya gönderilen koda sır koymayın.

📚 [Pages başlangıç rehberi](https://docs.github.com/en/pages/quickstart) · [Pages sitesi oluşturma](https://docs.github.com/en/pages/getting-started-with-github-pages/creating-a-github-pages-site)

<a name="bolum-10"></a>

## 10 · 🛡️ GitHub’da Yapılan 7 Güvenlik Hatası

Bir projeyi yayımlamadan önce birkaç temel alışkanlık edinmek, sonradan yapılacak zahmetli düzeltmeleri azaltır.

| # | Hata | Daha iyi uygulama |
| :---: | :--- | :--- |
| 1 | API anahtarını veya parolayı koda yazmak. | Sırları uygun secret yönetiminde saklayın; örnek dosyalarda yer tutucu kullanın. |
| 2 | Sızan anahtarı dosyadan silince sorunun çözüldüğünü sanmak. | Önce anahtarı iptal edin veya yenileyin; geçmiş ve kopyaları ayrıca değerlendirin. |
| 3 | Hesap kurtarma yöntemlerini hazırlamamak. | 2FA veya passkey yapılandırın; kurtarma kodlarını güvenli yerde saklayın. |
| 4 | `.gitignore` dosyasının geçmişi temizlediğini sanmak. | Takip edilen dosyaların ve eski commit’lerin ayrıca ele alınması gerektiğini bilin. |
| 5 | Token ve otomasyonlara gereğinden fazla yetki vermek. | Yalnızca gereken depo ve işlem izinlerini tanımlayın. |
| 6 | İncelemeden üçüncü taraf action kullanmak. | Kaynağı inceleyin; doğrulanmış tam commit SHA’sına sabitleyin. |
| 7 | Güvenilmeyen PR kodunu sırların erişilebilir olduğu işte çalıştırmak. | Özellikle `pull_request_target` gibi ayrıcalıklı tetikleyicilerde güven sınırlarını koruyun. |

### 🔒 Basit bir `.gitignore` başlangıcı

```gitignore
# Yerel gizli ayarlar
.env
.env.*
!.env.example

# Bağımlılıklar ve yerel çıktılar
node_modules/
coverage/
*.log
```

`.env.example` dosyasında yalnızca ayar adları ve sahte örnek değerler bulunsun. `.gitignore`, daha önce takip edilmeye başlanmış dosyayı kendiliğinden takipten çıkarmaz ve Git geçmişindeki sırları silmez.

> [!IMPORTANT]
> Gerçek bir anahtarı yanlışlıkla paylaştıysanız yeni commit ile üstünü örtmek yeterli değildir. Anahtarı ilgili sağlayıcıda iptal etmek veya değiştirmek ilk adımdır.

📚 [Sızan sırları giderme](https://docs.github.com/en/code-security/tutorials/remediate-leaked-secrets/remediating-a-leaked-secret) · [Hassas verileri kaldırma](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/removing-sensitive-data-from-a-repository) · [Gitignore](https://git-scm.com/docs/gitignore) · [2FA](https://docs.github.com/en/authentication/securing-your-account-with-two-factor-authentication-2fa/about-two-factor-authentication) · [Actions güvenliği](https://docs.github.com/en/actions/reference/security/secure-use)

---

## 🎯 Öğrendiklerini Bir Projede Birleştir

Bir **Görev Defteri**, **Kitap Listesi** veya **Kişisel Notlar** projesi seçin. Aşağıdaki listeyi kendi deponuza kopyalayıp tamamladıkça işaretleyin:

- [ ] Profilime kısa ve doğru bir tanıtım ekledim.
- [ ] Projemin amacını README’nin ilk paragrafında anlattım.
- [ ] Kurulum veya kullanım adımlarını denedim.
- [ ] İlk geliştirme işimi issue olarak kaydettim.
- [ ] Değişiklik için ayrı bir branch oluşturdum.
- [ ] PR açıklamasında nedenini ve yaptığım kontrolü yazdım.
- [ ] Bir kullanıcı testi veya dokümantasyon katkısı yaptım.
- [ ] İşlerimi bir Projects görünümünde takip ettim.
- [ ] Uygun bir kontrolü Actions ile otomatikleştirdim.
- [ ] Tanıtım sayfamı Pages ile yayımladım.
- [ ] Sürüm notlarını yazdım ve paylaşılacak dosyaları kontrol ettim.

İlk hedefiniz bütün özellikleri kullanmak olmak zorunda değil. Birinin açıp anlayabildiği, deneyebildiği ve geri bildirim bırakabildiği küçük bir proje iyi bir başlangıçtır.

<div align="center">

**💡 Bir fikir seç. Küçük bir değişiklik yap. Ne öğrendiğini paylaş.**

<sub>Bu bağımsız rehberdeki teknik bağlantılar GitHub, Git ve Node.js’in resmî belgelerine yönlendirir. Arayüz adları ve action sürümleri zamanla değişebilir.</sub>

</div>
