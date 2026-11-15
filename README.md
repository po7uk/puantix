# Puantix 11.3 — Özet ekranında FM İzin Durumu

- Özet ekranında **Bu ay yapılan FM** kartından sonra yeni **FM İzin Durumu** kartı eklendi.
- Bu ay **izne çevrilen FM**: çalışma tarihinin ait olduğu ayda, 1,25 / 1,50 / 2,00 katsayıları uygulanarak hesaplanır.
- **Toplam kalan FM izni**: seçili ayın sonu itibarıyla kullanılabilir olan tek toplam bakiye. Daha sonraki aylarda yapılan kullanımlar geçmiş ay bakiyesini azaltmaz.
- Bu ay **kullanılan FM izni**: izin kullanım tarihine göre.
- Bu ay **süresi dolan FM izni**: hakkın son kullanım tarihine göre, ücret dönüşümü öncesinde kullanılmamış süre.
- Eski Pazar ve Pzt–Cmt hakları tek toplamda, son kullanım tarihi önceliği korunarak hesaplanır.
- Mevcut veriler ve diğer ekranlar korunmuştur. Veri saklama anahtarı: `mesaitakip-v2`.

## Güncelleme

Yayın deposu: https://github.com/po7uk/puantix (main / root). ZIP içindeki **dosyaları** repo ana dizinine yükleyin. GitHub Pages adresi: https://po7uk.github.io/puantix/ . Önce Ayarlar üzerinden JSON yedeğinizi alın. Safari site verilerini silmeyin.

---

# Puantix 11.2 — FM izin hakkı tarih gösterimi

Puantix 11.0 paketinde atlanan `fixedActive` ve `payrollMonth` fonksiyonları geri eklendi. Ana ekran ve Bordro tekrar açılır. FM Durumu raporları 11.0 ile aynen korunur. Uygulama önbelleği 11.1 olarak güncellendi.

Yayın deposu: `https://github.com/po7uk/puantix` (`main / root`). Yayın URL: `https://po7uk.github.io/puantix/`. ZIP içindeki dosyaları doğrudan deponun ana dizinine yükleyin. **Yerel Safari verilerini temizlemeyin.** `mesaitakip-v2` veri anahtarı korunmaktadır.

---

# Puantix 11.1 — iPhone PWA

## Güncelleme ve veri güvenliği

1. Puantix'te **Ayarlar → Veri ve yedekleme → JSON yedeği indir** ile önce yedek oluşturun.
2. Bu paketin `mesaitakip/` klasörünün **içindeki** dosyaları GitHub'daki `po7uk/puantix` deposunun `main` branch'inin köküne yükleyin. `mesaitakip` klasörünü depo içinde ayrıca oluşturmayın.
3. GitHub Pages yayınını `main / (root)` olarak bırakın. Yayın adresi: `https://po7uk.github.io/puantix/`.
4. iPhone'da uygulamayı tamamen kapatıp yeniden açın; gerekiyorsa Safari'de aynı adresi yenileyin.

Mevcut `localStorage` anahtarı **`mesaitakip-v2`** korunur. GitHub kodu herkese açıktır, fakat yerel çalışma/maaş/izin kayıtları GitHub'a yüklenmez. Safari site verilerini silmek veri kaybına yol açabilir; yedek dosyalarını güvenli tutun.

## 9.0 temeli ve 10.0 güncellemeleri

- Takvim günlük kayıtlarında her gün ayrı FM tutarı artık gösterilmez.
- Pazartesi–Cumartesi FM kararı ilgili haftanın **Cumartesi** günündeki özet kutuda verilir. Cumartesi fiilî çalışma yoksa değerlendirme **Cuma** gününde gösterilir.
- **Pazar FM** bağımsız değerlendirilir. Her grupta `Ücret` veya `İzin` seçilir. Değerlendirme hafta bittikten sonraki pazartesiden itibaren yapılabilir.
- İzne dönüşen süre: `1,25 × FM saatleri + 1,50 × FM saatleri + 2,00 × resmî tatil saatleri`. İzne çevrilen saatler aynı zamanda doğrudan FM ücreti olarak ödenmez.
- FM izin hakkı ilgili haftayı takip eden pazartesi başlar ve **altı takvim ayı** sonra sona erer. Pzt–Cmt ve Pazar hakları ayrı kazanılır ancak kullanılabilir izin bakiyesinde birleştirilir. Kullanımda önce daha erken sonlanacak haklardan düşülür.
- Süresi dolmuş kullanılmamış izinler, yalnızca **ilk hak/onay dönemindeki kayıtlı saatlik FM tabanı** ile ücrete dönüştürülür; katsayı ikinci kez uygulanmaz. Ocak/Temmuz zamları veya terfi bu eski saatlik tabanı değiştirmez.
- Dönüşüm ödemesi, altı aylık sonlanma tarihi ile aynı gün veya daha sonraki **ilk bordro kapanışını** esas alan aya eklenir. Örnek: Kasım kapanışı 22'si, dönüşüm 24'ü ise Aralık bordrosu.
- Bordro: doğrudan ödenen FM ve süresi dolmuş FM izni ödemeleri ayrı gelir satırlarıdır.
- Günlük veya haftalık Kayıt ekranındaki FM izni alanı kullanılabilir/kullanılacak/kalan bakiyeyi gösterir. Yetersiz FM izninde kırmızı uyarı ve kayıt engeli vardır.
- Yıllık izin bakiyesi eksi olabilir; yetersiz bakiye uyarısı verilir ama günlük kayıt engellenmez.
- Dar iPhone ekranlarında tarih ve saat kutuları ayrıca daraltılmıştır.

## Önceki özellikler

Haftalık 40 saat esnek çalışma; 1,25 / 1,50 / 2,00 FM; saatlik net ücret `(net maaş + kıdem) / 225`; Pazar FM; günlük saat/dakika ve iOS saat seçici; yarım gün 12:30 resmî tatil ayrımı; dinlenme hesabı; yıllık/saatlik izin; çift maaş; Ocak/Temmuz zamları; terfiyle sıfırlanan kıdem; yıllık/aylık rapor; bordro; JSON/CSV yedekleme.

## Önemli notlar

- Haftalık FM karşılığı izinler, haftanın tamamına ilişkin kayıtlar sonradan değiştirilirse tekrar hesaplanabilir. Kullanılmış izinle çelişen bir çalışma düzeltmesi yapılırsa uyarıları kontrol edin.
- FM saatlik tabanı, ilgili grubun ilk seçiminde (Pzt–Cmt için cumartesi, Pazar için pazar referans günü) kaydedilir. Sonradan aynı hakka yapılacak zam kıyaslamalarında **bu sabitlenmiş taban** geçerlidir.
- Geçmiş bordroyu değiştirmeden önce gerçek ödemelerle karşılaştırın. Süresi dolmuş hakların ilk ödeme ayları kullanıcının tanımladığı kapanış günlerine bağlıdır.
- Mazeret izninin yıllık hakkı ve çalışma yükümlülüğüne etkisi henüz tanımlanmadığından, bu sürümde ayrı bir mazeret izni hesap modülü açılmadı.


## Puantix 10.0 değişiklikleri
- FM izin bakiyesi tek toplam tutar olarak gösterilir; Pzt–Cmt / Pazar havuz seçimi kaldırılmıştır.
- FM izni kullanımı Takvim ekranından kaldırılıp Günlük Kayıt ekranına (ve haftalık toplu girişe) taşındı.
- FM izni kullanımları altı ay geçerli haklardan son kullanım tarihi önce gelenden düşülür. Eski havuz etiketli kayıtlar tek bakiyeye dahil olur.
- Yetersiz bakiyede kayıt engellenir. Ayrıntılı haklar, ilk saatlik ücret, hak bitişi ve ücret dönüşümü Takvim ekranından görülebilir.
- Yerel veri anahtarı `mesaitakip-v2` korunur; önce JSON yedeği alın.
- **Not:** FM izin kullanımının haftalık yükümlülüğe etkisi ayrıca netleştirilmediği için bu sürümde FM izin saatleri yeni FM üretmez ve çalışma süresine eklenmez.


## Puantix 11.0 — Raporlar: FM Durumu
Yıllık raporda kazanılan FM (ham saat), ücret seçilen FM, katsayılı izin olarak kazanılan FM, yıl içinde kullanılan FM izni, yıl sonu/bugün kalan toplam FM izni ve ilgili yıl bordrolarına aktarılan süresi dolmuş izin ödemeleri ayrı gösterilir. Ay açılımında haftalık Pzt–Cmt ve Pazar ücret/izin seçimleri görünür. Ücret karşılıkları için hak kazanılan dönemin baz saatlik ücreti korunur.


## Puantix 11.2

Takvim > FM izin haklarım > Haklar bölümünde fazla mesai haftasının başlangıcı yerine, hakkın kullanılmaya başlandığı sonraki pazartesi gösterilir. Hesaplama ve kayıt formatı değişmemiştir.
