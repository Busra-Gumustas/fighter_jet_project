✈️ Unity 3D Endless Runner Uçak Oyunu
Bu proje, Unity ile geliştirilen 3D bir sonsuz koşu (endless runner) tarzında savaş uçağı oyunudur. Oyuncu, uçağı sağa ve sola hareket ettirerek binalardan kaçınır. Uçak sabit kalırken zemin ve çevredeki binalar ileri doğru akar. Çarpışma durumunda oyun sona erer ve kullanıcıya tekrar başlatma veya ana menüye dönme seçeneği sunulur.

🎮 Oynanış Özeti
Giriş paneli: Başlat (Start) ve Çıkış (Exit) butonları içerir.

Oyun sahnesi:

Uçak sabit bir pozisyonda kalır.

Kamera uçağı dinamik olarak takip eder.

Zemin (road_controller.cs) ileri doğru hareket eder ve belli bir mesafeye ulaştığında başa sarar.

Oyuncu, A/D veya yön tuşlarıyla uçağı sağ/sol şeritlere kaydırır.

Uçak manevra sırasında sağa veya sola eğilir (DOTween ile).

Çarpışma sonrası: UiManager üzerinden son panel açılır ve kullanıcı Restart veya Home seçimi yapabilir.

🧩 Kullanılan Scriptler
kontrol_karakter.cs
Uçağın sağ/sol şerit değiştirme ve eğim animasyonlarını yönetir.

DOTween kütüphanesi kullanılarak geçişler yumuşatılır.

road_controller.cs
Zemin sürekli ileri hareket eder.

Belirli bir mesafeye ulaşıldığında zemin konumu sıfırlanır ve sürekli akan bir yapı sağlanır.

EndRoad() fonksiyonu oyun sonlandığında zemini durdurmak için kullanılır.

UiManager.cs
Başlangıç ve bitiş ekranlarındaki UI geçişlerini kontrol eder.

SceneManager ile sahne geçişleri yapılır.

Application.Quit() ile oyundan çıkılır.
