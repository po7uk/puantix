# Puantix 7.0 — iPhone PWA

GitHub Pages kurulumu: ZIP içindeki `mesaitakip` klasörünün **içeriğini** mevcut `po7uk/mesaitakip` deposunun ana dizinine yükleyin. Repo adını değiştirmeyin.

## Önce yedek

Uygulamada Ayarlar → Veri ve yedekleme → JSON yedeği indir. Yeni sürümü yüklemeden önce yedeği Dosyalar uygulamasında saklayın.

## Değişiklikler
- Puantix marka ve iPhone simgesi
- iOS'ta başlangıç/bitiş saatleri için yerel saat seçici; net süreler ve saatlik izin için parmakla kaydırmalı saat/dakika çarkı
- Ocak zorunlu ve Temmuz isteğe bağlı zam (% iki ondalık); uygulanma yılına bağlı
- Çift maaş ayları (net + kıdem iki kat); sabit gelirde isteğe bağlı çift ödeme
- Kıdem tarihçesi veya işe başlangıç tarihi üzerinden tamamlanmış yıl hesabı; saatlik FM tabanı (net+kıdem)/225
- Bordro, özet ve yıllık raporda ilgili ayın hesapları
- Tarihli geçmiş maaşların korunması ve geçmiş bordrodaki gerçekleşen ödemelerin saklanması

## Veri güvenliği ve saklama

Mevcut `localStorage` anahtarı (`mesaitakip-v2`) korunmuştur. GitHub'a hiçbir kişisel çalışma kaydı gönderilmez. Safari verileri temizlenirse kayıtlar kaybolabilir.

## Önemli

Maaş zamlarında bir tarihten itibaren yeni net maaş tutarı girilirse o kayıt yeni baz olur; aynı günün zam yüzdesi ayrıca uygulanmaz. Ocak/Temmuz zamları baz kayıt tarihinden sonra uygulanır. Eğer kıdem başlangıç tarihi girilirse tamamlanmış yıllar bu tarihe göre otomatik hesaplanır; aksi halde tarihli kıdem yılı kayıtları esas alınır.

Çift maaş FM saatlik tabanını iki katına çıkarmaz. Bordro kayıtları mali/hukuki danışmanlık değildir; ilk sonuçları gerçek bordro ile karşılaştırın.
