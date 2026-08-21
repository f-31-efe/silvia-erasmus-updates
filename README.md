# Silvia Erasmus — Güncellemeler

Bu depo yalnızca **sürüm bilgisi ve kurulum dosyalarını** barındırır.
Kaynak kod özel depoda durur.

## Yeni sürüm nasıl yayınlanır

1. Uygulamada `Updater.gd` içindeki `VERSION_CODE` değerini bir artır
2. APK'ları dışa aktar
3. Yeni bir release oluştur ve APK'ları ekle:

```bash
gh release create v1.0.1 SilviaErasmus.apk SilviaErasmusYonetim.apk --title "v1.0.1" --notes "Değişiklikler"
```

4. `latest.json` içindeki `code`, `version`, `notes` ve `apk` alanlarını güncelle

Uygulamalar her açılışta `latest.json` dosyasını okur. `code` değeri
uygulamanınkinden büyükse kullanıcıya güncelleme penceresi gösterilir.

`mandatory: true` yaparsan güncelleme zorunlu olarak sunulur.
