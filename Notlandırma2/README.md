# TDAS(Takipçi Davranışı ve Analiz Otomasyon Sistemi)

Bu proje, bir sosyal medya platformunun veritabanı tasarımını temsil eder. Aşağıda varlıklar ve ilişkilerin detaylı açıklamaları verilmiştir.

---

## 🗂️ Varlıklar ve İlişkiler

### 1. *Sosyal Medya ve Kullanıcı*
- *SosyalMedya*(Isim (PK), KullaniciAdi, Eposta, Sifre)

- *Kullanici*(KullaniciID (PK), KullaniciIsim)

- *Kullanir* (Kullanıcı ve Sosyal Medya İlişkisi)(KullaniciID (FK), SosyalMedyaIsim (FK), KatilimTarihi
  - *PRIMARY KEY*: (KullaniciID, SosyalMedyaIsim)

---

### 2. *Yayınlar ve Reklamlar*
- *Yayinlar*(YayinID (PK)(YayinTarihi,SosyalMedyaIsim (FK))

- *Reklam*(ReklamID (PK), Tur, ReklamKategori, TiklanmaSayisi, GosterimSayisi)

- *Gosterilme* (Reklam ve Yayınlar İlişkisi)(ReklamID (FK), YayinID (FK))
  - *PRIMARY KEY*: (ReklamID, YayinID)

---

### 3. *Gruplar ve Katılım*
- *Gruplar*(GrupID (PK)(UyeSayisi, Rol)

- *Katil* (Kullanıcı ve Gruplar İlişkisi)(KullaniciID (FK), GrupID (FK), KatilimTarihi)
  - *PRIMARY KEY*: (KullaniciID, GrupID)

---

### 4. *Gönderiler ve Etkileşimler*
- *Gonderi*( GonderiID (PK), GonderiMetni, Gorunurluk, GonderiTarihi, GonderiTur, YorumSayisi, BegeniSayisi)

- *Begeni* (Kullanıcı ve Gönderi İlişkisi)( KullaniciID (FK), GonderiID (FK))
  - *PRIMARY KEY*: (KullaniciID, GonderiID)

- *Yorum* (Kullanıcı ve Gönderi İlişkisi)( KullaniciID (FK), GonderiID (FK), YorumMetni)
  - *PRIMARY KEY*: (KullaniciID, GonderiID)

---

### 5. *Popüler İçerik*
- *PopulerIcerik*( IcerikID (PK), Tur, Goruntuluk)

- *Alma* (Popüler İçerik ve Gönderi İlişkisi)( IcerikID (FK), GonderiID (FK))
  - *PRIMARY KEY*: (IcerikID, GonderiID)

---

### 6. *Takipçi İlişkisi*
- *Takipci*( Username (PK), TakipEdilen, TakipTarihi)

---

## 📚 Kullanım

Bu veritabanı tasarımı, bir sosyal medya platformunda kullanıcılar, gruplar, gönderiler, reklamlar ve etkileşimler gibi temel unsurların yönetimini destekler. Her varlık ve ilişki, aşağıdaki SQL notasyonuna göre modellenmiştir.

- *Primary Key (PK)*: Tablodaki her kaydı benzersiz şekilde tanımlar.
- *Foreign Key (FK)*: Diğer tablolardaki kayıtlara referans verir.




## 📂 SQL Dosyası
Bu yapıyı oluşturan SQL dosyalarına erişmek için [proje repository'sine](#) göz atabilirsiniz.

---
