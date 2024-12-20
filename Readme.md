Proje Özeti:

Bu projede, bir derin öğrenme modeli (CNN) kullanarak görsel sınıflandırma işlemi yapılmıştır. Aşağıda yapılan işlemler ve elde edilen sonuçlar özetlenmiştir:

	1.Veri Setinin Hazırlığı ve Model Eğitimi:
	    •	Eğitim verisi (4550 örnek) ve test verisi (1950 örnek) kullanılarak model eğitildi.
	    •	Model, 30 epoch boyunca eğitildi ve doğruluk değerleri zamanla iyileşmeye başladı. Ancak, doğruluk oldukça düşük seviyelerde kaldı.
	    Sonuçlar:
        •	Eğitim doğruluğu: %69.9
        •	Test doğruluğu: %54.72
        •	Test kaybı: 1.4550

	2.Veri Manipülasyonu (Veri Artırımı ve Değiştirme):
        •	Görseller üzerinde veri artırımı (parlaklık artırma ve azaltma) işlemi yapıldı.
        •	Manipüle edilmiş test seti oluşturuldu ve bu test setiyle model test edildi. Ancak modelin doğruluğu oldukça düşük seviyelere geriledi.
        Sonuçlar:
        •	Manipüle edilmiş test doğruluğu: %9.79
        •	Manipüle edilmiş test kaybı: 53.57

	3.Renk Sabitleme (Gray World):
        •	Görseller üzerinde renk dengeleme (Gray World) uygulandı.
        •	Renk sabitlemesi yapılmış manipüle edilmiş test seti ile model tekrar test edildi. Ancak bu işlem de modelin performansını artırmadı.
        Sonuçlar:
	    •	Renk sabitlemesi yapılmış manipüle edilmiş test doğruluğu: %9.79

Değerlendirme ve Olası Sebepler:

        Düşük Performans ve Manipülasyonların Olumsuz Etkisi:
        •	Eğitim seti üzerinde belirli bir doğruluk elde edilmesine rağmen, test verisi üzerinde modelin doğruluğu düşük kalmıştır. Bu, modelin overfitting yapmadığını fakat genelleme yeteneği konusunda zorluklar yaşadığını gösteriyor.
        •	Manipülasyonlar (parlaklık değişimi ve renk sabitlemesi) modelin doğru tahmin yapmasını zorlaştırmış olabilir. Bu tür görüntü manipülasyonları, modelin daha önce görmediği özellikler görmesine yol açabilir ve bu da doğruluğun düşmesine neden olabilir.

        Veri Artırımı ve Etkisi:
        •	Veri artırımı genellikle modelin genelleme yeteneğini artırır. Ancak bu proje için yapılan artırımların etkisi sınırlı olmuş gibi görünüyor. Bu durum, kullanılan veri setinin çeşitliliğinin veya modelin kapasitesinin yeterli olmamasından kaynaklanabilir.

        Renk Sabitleme Etkisi:
        •	Renk sabitlemesi genellikle görsel dengeleme sağlar, ancak bu yöntemin modelin doğruluğunu artırması beklenen bir etkisi olmadı. Bu durum, modelin çok fazla görsel değişimle başa çıkmada zorlanması ve renk sabitlemesinin çok fazla bilgi kaybına yol açması nedeniyle olabilir.

İyileştirme Önerileri:

	1.Modelin Kapasitesinin Arttırılması:
        •	Modelin daha derin katmanlara ve daha fazla parametreye sahip olması, performansı artırabilir.
        •	Diğer optimizasyon teknikleri (örneğin, learning rate scheduler veya farklı optimizer’lar) uygulanabilir.

	2.Veri Manipülasyonlarının İyileştirilmesi:
	    •	Yapılan manipülasyonlar modelin doğruluğunu düşürdüyse, veri artırma tekniklerinin daha dikkatli seçilmesi gerekebilir. Özellikle daha anlamlı manipülasyonlar (farklı dönüşümler veya gürültü ekleme) test edilebilir.

	3.Daha Gelişmiş Veri Seti ve Eğitim Süreci:
	    •	Eğitim veri setinin çeşitliliği artırılabilir. Örneğin, farklı görüntü sınıflarına daha fazla örnek eklemek, modelin genelleme yeteneğini artırabilir.

Sonuç olarak, modelin eğitimi ve manipülasyonlar belirli sonuçlar vermiştir, ancak genel doğruluk hala geliştirilebilir.


İlgili veri setine kaggle üzerinden ulaşabilirsiniz:
[Animals with Attributes 2](https://www.kaggle.com/datasets/rrebirrth/animals-with-attributes-2)

Proje arkadaşımın GitHub profili:
[Reyyan İlci](https://github.com/reyyolimo)

