# Puantix 9.0 — iPhone PWA

## Güncelleme ve veri güvenliği

1. Puantix'te **Ayarlar → Veri ve yedekleme → JSON yedeği indir** ile önce yedek oluşturun.
2. Bu paketin `mesaitakip/` klasörünün **içindeki** dosyaları GitHub'daki `po7uk/mesaitakip` deposunun `main` branch'inin köküne yükleyin. `mesaitakip` klasörünü depo içinde ayrıca oluşturmayın.
3. GitHub Pages yayınını `main / (root)` olarak bırakın. Yayın adresi: `https://po7uk.github.io/mesaitakip/`.
4. iPhone'da uygulamayı tamamen kapatıp yeniden açın; gerekiyorsa Safari'de aynı adresi yenileyin.

Mevcut `localStorage` anahtarı **`mesaitakip-v2`** korunur. GitHub kodu herkese açıktır, fakat yerel çalışma/maaş/izin kayıtları GitHub'a yüklenmez. Safari site verilerini silmek veri kaybına yol açabilir; yedek dosyalarını güvenli tutun.

## 9.0 yenilikleri

- Takvim günlük kayıtlarında her gün ayrı FM tutarı artık gösterilmez.
- Pazartesi–Cumartesi FM kararı ilgili haftanın **Cumartesi** günündeki özet kutuda verilir. Cumartesi fiilî çalışma yoksa değerlendirme **Cuma** gününde gösterilir.
- **Pazar FM** bağımsız değerlendirilir. Her grupta `Ücret` veya `İzin` seçilir. Değerlendirme hafta bittikten sonraki pazartesiden itibaren yapılabilir.
- İzne dönüşen süre: `1,25 × FM saatleri + 1,50 × FM saatleri + 2,00 × resmî tatil saatleri`. İzne çevrilen saatler aynı zamanda doğrudan FM ücreti olarak ödenmez.
- FM izin hakkı ilgili haftayı takip eden pazartesi başlar ve **altı takvim ayı** sonra sona erer. Pzt–Cmt ve Pazar izinleri ayrı havuzlardır. Kullanımda önce daha erken sonlanacak haklardan düşülür.
- Süresi dolmuş kullanılmamış izinler, yalnızca **ilk hak/onay dönemindeki kayıtlı saatlik FM tabanı** ile ücrete dönüştürülür; katsayı ikinci kez uygulanmaz. Ocak/Temmuz zamları veya terfi bu eski saatlik tabanı değiştirmez.
- Dönüşüm ödemesi, altı aylık sonlanma tarihi ile aynı gün veya daha sonraki **ilk bordro kapanışını** esas alan aya eklenir. Örnek: Kasım kapanışı 22'si, dönüşüm 24'ü ise Aralık bordrosu.
- Bordro: doğrudan ödenen FM ve süresi dolmuş FM izni ödemeleri ayrı gelir satırlarıdır.
- FM izin kullanımı ekranı, kullanılabilir/kullanılacak/kalan bakiyeyi gösterir. Yetersiz FM izninde kırmızı uyarı ve kayıt engeli vardır.
- Yıllık izin bakiyesi eksi olabilir; yetersiz bakiye uyarısı verilir ama günlük kayıt engellenmez.
- Dar iPhone ekranlarında tarih ve saat kutuları ayrıca daraltılmıştır.

## Önceki özellikler

Haftalık 40 saat esnek çalışma; 1,25 / 1,50 / 2,00 FM; saatlik net ücret `(net maaş + kıdem) / 225`; Pazar FM; günlük saat/dakika ve iOS saat seçici; yarım gün 12:30 resmî tatil ayrımı; dinlenme hesabı; yıllık/saatlik izin; çift maaş; Ocak/Temmuz zamları; terfiyle sıfırlanan kıdem; yıllık/aylık rapor; bordro; JSON/CSV yedekleme.

## Önemli notlar

- Haftalık FM karşılığı izinler, haftanın tamamına ilişkin kayıtlar sonradan değiştirilirse tekrar hesaplanabilir. Kullanılmış izinle çelişen bir çalışma düzeltmesi yapılırsa uyarıları kontrol edin.
- FM saatlik tabanı, ilgili grubun ilk seçiminde (Pzt–Cmt için cumartesi, Pazar için pazar referans günü) kaydedilir. Sonradan aynı hakka yapılacak zam kıyaslamalarında **bu sabitlenmiş taban** geçerlidir.
- Geçmiş bordroyu değiştirmeden önce gerçek ödemelerle karşılaştırın. Süresi dolmuş hakların ilk ödeme ayları kullanıcının tanımladığı kapanış günlerine bağlıdır.
- Mazeret izninin yıllık hakkı ve çalışma yükümlülüğüne etkisi henüz tanımlanmadığından, bu sürümde ayrı bir mazeret izni hesap modülü açılmadı.
