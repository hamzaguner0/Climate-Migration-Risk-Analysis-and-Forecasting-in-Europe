# ERA5 Temperature Exploration · Europe

Copernicus Climate Data Store üzerinden ERA5 sıcaklık örneği indirme ve NetCDF verisini inceleme çalışması. Depo adındaki iklim göçü/öngörü hedefi araştırma niyetidir; mevcut dosyalarda eğitilmiş göç riski veya göç tahmin modeli bulunmaz.

## İçerik

`data_retrieval.ipynb` 2023 Ocak, Şubat ve Mart için seçili gün/saatlerde 2 m sıcaklık verisi ister. Bu sınırlı örnek, uzun dönem sıcaklık eğilimi veya göç nedenselliği analizi değildir. `temperature_europe_2023.nc` tarihsel örnek dosyadır; tam bir yıllık günlük seri olarak yorumlanmamalıdır. İstek alanı ve koordinatları notebook'ta ayrıca kontrol edilmelidir.

## Kurulum

```sh
git clone https://github.com/hamzaguner0/Climate-Migration-Risk-Analysis-and-Forecasting-in-Europe.git
cd Climate-Migration-Risk-Analysis-and-Forecasting-in-Europe
python -m pip install -r requirements.txt
jupyter notebook data_retrieval.ipynb
```

CDS hesabı ve veri lisansı kabulü gerekir. [Resmî CDS API kurulumu](https://cds.climate.copernicus.eu/how-to-api) doğrultusunda anahtarınızı kullanıcı hesabınızdaki `.cdsapirc` dosyasında tutun. Kod `cdsapi.Client()` kullanır; notebook veya Git dosyasına anahtar yazmayın. Yerel yapılandırma dosyası ve `.env` Git dışında tutulur. Bu depoda `main.py` bulunmaz.

## Veri kaynağı ve sınırlar

[ERA5 single levels](https://cds.climate.copernicus.eu/datasets/reanalysis-era5-single-levels?tab=overview), Copernicus Climate Change Service (C3S). Verinin kullanımı ve yeniden paylaşımı kaynak lisansına tabidir; bu depodaki kod veri üzerinde yeni hak sağlamaz. Tarihsel indirme notebook'u güncel API şeması değişikliklerinde yeniden kontrol edilmelidir; bu düzenlemede hesap erişimiyle yeni veri indirme denenmedi.

İleride uzun dönem ve bölgesel kapsamı doğrulanmış seriler, göç gözlemleri, karıştırıcı değişkenler ve bağımsız değerlendirme gerekir. Mevcut çalışmadan göç riski veya güvenilir gelecek tahmini sonucu çıkarılamaz.
