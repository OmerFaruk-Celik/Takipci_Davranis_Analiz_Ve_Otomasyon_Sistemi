# Takipçi Analizi ve Otomasyon Sistemi

Bu proje, sosyal medya takipçilerini analiz eden ve onlara özel reklam içerikleri sunan bir otomasyon sistemidir. Takipçilerin beğenileri, yorumları ve katıldıkları gruplar gibi etkileşimlerinden yola çıkarak, kişiselleştirilmiş reklam gösterimlerini ve içerik önerilerini otomatik olarak sunmayı amaçlamaktadır.

## Proje İçeriği

Bu proje, kullanıcıların sosyal medya üzerindeki davranışlarını analiz ederek, kişisel ilgi alanlarına göre özel içerik ve reklam önerileri sunmayı hedefler. Kullanıcı ve takipçi ilişkileri, gönderiler, popüler içerikler, reklamlar gibi birçok varlık arasındaki ilişkiler analiz edilmiştir.

### Varlıklar ve Özellikleri

1. **Kullanıcı**
   - Kullanıcı ID
   - İsim

2. **Takipçi**
   - Kullanıcı Adı (Username)
   - Takip Edilen
   - Takip Tarihi

3. **Gönderi**
   - Gönderi ID
   - Gönderi Metni
   - Beğeni Sayısı
   - Yorum Sayısı
   - Görünürlük
   - Gönderi Tarihi
   - Tür

4. **Gruplar**
   - Grup ID
   - Üye Sayısı
   - Rol

5. **Popüler İçerikler**
   - İçerik ID
   - Tür
   - Görünürlük
   - Yayınlanma Tarihi

6. **Reklam**
   - Reklam ID
   - Tür
   - Reklam Kategorisi
   - Tıklanma Sayısı

### ER Diyagramı

Projedeki varlıklar arasındaki ilişkileri gösteren basit ER diyagramı aşağıda sunulmuştur.

![ER Diyagramı](path/to/your/ER-diagram.png)

> Not: Diyagramı yerel depoya kaydettikten sonra dosya yolunu `ER-diagram.png` olarak güncelleyiniz.

### İlişkiler ve Türleri

| İlişki           | Varlık 1       | Varlık 2             | İlişki Türü       |
|------------------|----------------|----------------------|-------------------|
| Sahiptir         | Kullanıcı      | Takipçi              | Birden Çoğa       |
| Beğeni           | Takipçi        | Gönderi              | Çoktan Çoğa       |
| Yorum            | Takipçi        | Gönderi              | Çoktan Çoğa       |
| Yayımlar         | Kullanıcı      | Gönderi              | Birden Çoğa       |
| Katılma          | Takipçi        | Gruplar              | Çoktan Çoğa       |
| Olma             | Gönderi        | Popüler İçerikler    | Birden Bire       |
| Görüntüleme      | Takipçi        | Popüler İçerikler    | Çoktan Çoğa       |
| Gösterilme       | Reklam         | Popüler İçerikler    | Çoktan Bire       |
| Etkileşim        | Reklam         | Gruplar              | Çoktan Çoğa       |
| Yayınlar         | Reklam         | Sosyal Medya         | Birden Çoğa       |
| Tıklanma         | Takipçi        | Reklam               | Çoktan Çoğa       |

### Proje Amacı

Bu proje, sosyal medya platformları üzerinde kullanıcıların etkileşimlerini analiz ederek, onlara özel içerik ve reklam önerileri sunmayı hedefler. Takipçi davranışlarını ve tercihlerini analiz eden bu otomasyon sistemi, kişiselleştirilmiş reklamların etkili bir şekilde gösterilmesine olanak tanır.

---

## Kurulum ve Kullanım

1. Projeyi klonlayın:
   ```bash
   git clone https://github.com/yourusername/follower-analysis-automation.git
