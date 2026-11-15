# Puantix 1.1 — İlk yayın sürümü

Bu paket GitHub Pages üzerinde `https://po7uk.github.io/puantix/` adresine yayınlamak içindir.

## Bordro — doğrudan FM ödeme ayrıntısı

- **Doğrudan ödenen FM (toplam):** O bordro döneminde ücrete çevrilen, doğrudan ödenen FM toplamı.
- **Önceki dönemden devreden FM:** Önceki aylarda çalışılmış, kapanış tarihi nedeniyle bu aya ödeme olarak aktarılmış FM süresi ve tutarı.
- **Bu ayın doğrudan ödenen FM’si:** İçinde bulunulan ayda çalışılmış ve o ay bordrosuna dahil edilmiş FM süresi ve tutarı.
- İki alt satır toplamın **dökümüdür**, bordro toplamına ikinci kez eklenmez.
- **Süresi dolan FM izni ödemeleri** ayrı bir kalemdir.
- FM saatleri ham çalışma süresidir; ödenen TL tutarları ilgili günün 1,25/1,50/2,00 katsayısı ve o günün saatlik ücreti ile hesaplanır.

## Sürüm ve veri uyumluluğu

- Kullanıcıya gösterilen ürün sürümü **Puantix 1.1** olarak güncellendi.
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
