# Puantix 11.4 — Düzenlenebilir Saatlik İzin ve Yardım / SSS

- **Ayarlar → İzin hakları:** Her takvim yılı için ayrı **Saatlik izin hakkı (saat / yıl)** değeri girilebilir. 27 saat yalnızca önceki sürüm kullanıcıları için başlangıç değeri olup sabit bir kural değildir. Mevcut kayıtlı haklar korunur.
- Saatlik izin yıl içinde 1 Ocak–31 Aralık arasında geçerlidir, devir yapılmaz. Bu yılın tanımlı hakkından o yıl kullanılan saatler düşülür.
- **Ayarlar** altında kapsamlı, aranabilir **Yardım ve Sık Sorulan Sorular** ekranı eklendi: başlangıç, FM hesaplama, FM izin kullanımı, yıllık ve saatlik izin, maaş/bordro, veri yedekleme.
- **Özet:** Yıllık ve Saatlik İzin Durumu: kalan yıllık izin, kalan saatlik izin, o ay kullanılan yıllık ve saatlik izin. Negatif bakiyeler kırmızı gösterilir.
- FM toplam bakiye kartındaki yanıltıcı **“ay sonu itibarıyla kullanılabilir”** alt yazısı kaldırıldı.
- Veri saklama anahtarı aynen `mesaitakip-v2`; eski kayıtlar ve yedekler ile uyumluluk korunur.

**Yükleme:** https://github.com/po7uk/puantix deposunda `main` branch kök dizinindeki dosyaları ZIP içindeki dosyalarla değiştirin (alt klasör oluşturmayın). Yayın adresi: https://po7uk.github.io/puantix/. Önce Ayarlar → Veri ve yedekleme bölümünden JSON yedeği alın; Safari site verilerini silmeyin.


## Puantix 11.5 — Ayarlar bölümünün açık kalması
- İzin hakları açıkken yıl ileri/geri değiştirildiğinde bölüm açık kalır.
- Zam oranları bölümü için de yıl gezinirken aynı davranış geçerlidir.
- Form alanları seçili yıla ait kayıtlı haklarla yenilenir; değişikliklerin kalıcı olması için **Kaydet** kullanılır.
- Yerel veri biçimi ve saklama anahtarı değiştirilmedi.
