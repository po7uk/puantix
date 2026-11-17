# Puantix 1.4.1 — Haftalık toplu giriş kolaylıkları

Bu paket GitHub Pages üzerinde `https://po7uk.github.io/puantix/` adresine yayınlamak içindir.

## Bordro — doğrudan FM ödeme ayrıntısı

- **Doğrudan ödenen FM (toplam):** O bordro döneminde ücrete çevrilen, doğrudan ödenen FM toplamı.
- **Önceki dönemden devreden FM:** Önceki aylarda çalışılmış, kapanış tarihi nedeniyle bu aya ödeme olarak aktarılmış FM süresi ve tutarı.
- **Bu ayın doğrudan ödenen FM’si:** İçinde bulunulan ayda çalışılmış ve o ay bordrosuna dahil edilmiş FM süresi ve tutarı.
- İki alt satır toplamın **dökümüdür**, bordro toplamına ikinci kez eklenmez.
- **Süresi dolan FM izni ödemeleri** ayrı bir kalemdir.
- FM saatleri ham çalışma süresidir; ödenen TL tutarları ilgili günün 1,25/1,50/2,00 katsayısı ve o günün saatlik ücreti ile hesaplanır.

## Sürüm ve veri uyumluluğu

- Kullanıcıya gösterilen ürün sürümü **Puantix 1.4.1** olarak güncellendi.
- Yerel veri saklama anahtarı aynıdır: `mesaitakip-v2`. Uygulama sürümü 1.0, veri şeması sürümü 2 ile karıştırılmamalıdır.
- Saatlik izin hakkı Ayarlar altında her yıl için değiştirilebilir; Yardım / SSS ekranı vardır.
- iOS önbellek kontrolü için servis çalışanının önbellek adı ve `app.js` kaynak bağlantısı yenilendi.

## GitHub Pages yükleme

ZIP içindeki **9 dosyanın tamamını** `po7uk/puantix` deposunda `main` branch kök dizinine yükleyin. Alt klasör oluşturmayın. GitHub Pages ayarı `main / (root)` olmalıdır.

**Veri güvenliği:** Güncellemeden önce uygulamadan JSON yedeği alın. Safari site verilerini ya da eski ana ekran uygulamasını doğrulamadan silmeyin.

## Sürüm 1.1 — Veri sıfırlama ve yardım güncellemeleri

- Ayarlar → Veri ve yedekleme altına **Tüm verileri sil ve sıfırla** eklendi.
- Silmeden önce kullanıcıdan **SIFIRLA** kelimesi ve ardından ikinci onay istenir. Herhangi bir onay iptal edilirse veriler korunur.
- Yalnızca Puantix'in `mesaitakip-v2` ve eski göç kaynağı `mesaitakip-v1` depolama anahtarları temizlenir. Böylece eski verilerin tekrar göç etmesi önlenir.
- Sıfırlanan veriler geri alınamaz; önceden dışa aktarılmış JSON yedeğiyle geri yüklenebilir.
- Yardım/SSS: reset ve yedek, iOS güncelleme davranışı, Özet izin durumu, doğrudan FM'nin bu ay/devreden ayrımı ve süresi dolan FM izni bordrosu.
- Çalışma ve ödeme hesaplama kuralları değiştirilmemiştir.

## Sürüm 1.2 — Günlük net süre

- Günlük Kayıt ekranında yeni bir gün için net normal çalışma varsayılanı **8 saat 00 dakika** oldu.
- Kullanıcı saat ve dakika seçicisiyle varsayılanı değiştirebilir.
- Daha önce kayıt yapılmış günler açıldığında kaydedilmiş çalışma süresi korunur; 8 saate sıfırlanmaz.
- Giriş/çıkış saatlerinden hesaplama ve haftalık toplu giriş varsayılanları değiştirilmedi.
- Kullanıcı verileri ve yerel saklama anahtarı değiştirilmedi.

## Sürüm 1.3 — Süre seçimleri

- Saat ve dakika alanına dokunulduğunda açılan iki sütunlu dokunmatik çark, kaydırarak seçim yapmaya devam eder.
- Dakika çarkında **00’ın hemen önünde 59**, **59’un hemen sonrasında 00** bulunur. Saat çarkı 00–24 aralığında benzer döngü uygular.
- Saat ve dakika birbirinden bağımsızdır; **24 saat 00 dakika** üst sınırına uyulur.
- Başlangıç ve bitiş için tarayıcının yerel `time` kontrolü değiştirilmedi.
- Mevcut kayıtlar ve `mesaitakip-v2` yerel depolama anahtarı aynen korundu.

## Sürüm 1.4 — Haftalık toplu giriş
- Haftalık toplu giriş açılırken güncel haftanın pazartesi günü varsayılan seçilir. Önceki hafta seçimi otomatik taşınmaz.
- “Pzt–Cum boş günleri 8 saat doldur” ile kayıt olmayan beş iş günü için net çalışma süresi 08:00 yazılır. Önceden kayıtlı günler korunur. Bu işlem sadece formu doldurur; değişiklikler “Haftayı kaydet” ile kaydedilir.
- Yardım/SSS güncellendi.


## 1.4.1 — Açılış ve önbellek düzeltmesi

- HTML içindeki JS sürüm numarası 1.4.1 olarak güncellendi (1.4 paketinde yanlışlıkla 1.3 kalmıştı).
- Service Worker sürümü ve önbellek anahtarı yenilendi.
- Başlangıç hatalarında boş ekran yerine verileri korumayı hatırlatan uyarı gösterilir.
- Haftalık giriş, Pzt–Cum 8 saat doldurma ve diğer kayıtlar korunur.
