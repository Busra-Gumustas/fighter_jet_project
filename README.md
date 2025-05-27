# ✈️ Unity 3D Endless Runner Uçak Oyunu

Bu proje, Unity ile geliştirilen 3D bir **sonsuz koşu (endless runner)** tarzında savaş uçağı oyunudur.  
Oyuncu, uçağı sağa ve sola hareket ettirerek binalardan kaçınır. Uçak sabit kalırken zemin ve çevredeki binalar ileri doğru akar.  
Çarpışma durumunda oyun sona erer ve kullanıcıya tekrar başlatma veya ana menüye dönme seçeneği sunulur.

---

## 🎮 Oynanış Özeti

- **Giriş Paneli**: Başlat (*Start*) ve Çıkış (*Exit*) butonları içerir.

- **Oyun Sahnesi**:
  - Uçak sabit bir pozisyonda kalır.
  - Kamera, uçağı dinamik olarak takip eder.
  - Zemin (`road_controller.cs`) ileri doğru hareket eder ve belli bir mesafeye ulaştığında başa sarar.
  - Oyuncu, `A`/`D` veya yön tuşları ile uçağı sağ/sol şeritlere kaydırır.
  - Uçak manevra sırasında sağa veya sola eğilir (DOTween ile).
  - Çarpışma sonrası, `UiManager` üzerinden son panel açılır ve kullanıcıya *Restart* veya *Home* seçimi sunulur.

---

## 🧩 Kullanılan Scriptler

### `kontrol_karakter.cs`
- Uçağın sağ/sol şerit değiştirme ve eğim animasyonlarını yönetir.
- `DOTween` kütüphanesi kullanılarak geçişler yumuşatılır.

### `road_controller.cs`
- Zemin sürekli ileri hareket eder.
- Belirli bir mesafeye ulaşıldığında zemin konumu sıfırlanır, böylece sürekli akan bir yapı sağlanır.
- `EndRoad()` fonksiyonu oyun sonlandığında zemini durdurmak için kullanılır.

### `UiManager.cs`
- Başlangıç ve bitiş ekranlarındaki UI geçişlerini kontrol eder.
- `SceneManager` ile sahne geçişleri yapılır.
- `Application.Quit()` ile oyundan çıkılır.

---

## 🚀 Gereksinimler

- Unity 2021.3.x veya üzeri
- [DOTween](http://dotween.demigiant.com/) kütüphanesi (Animasyonlar için)

---

## 🖼️ Ekran Görüntüleri (İsteğe Bağlı)
> Projeye ait oyun içi ekran görüntüleri buraya eklenebilir.

---

## 📂 Projeyi Çalıştırmak İçin

```bash
git clone https://github.com/kullanici_adin/proje-adi.git
