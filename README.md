## Welcome to DataSearch!
Bu program  spesifik bir görev için "prototip" tasarlanmıştır. Kanser türlerinde; **DNA metilasyon** verisi bulunan örneklerin, **mRNA zscores** verilerinden alınıp yeni bir data oluşturmayı amaçlamaktadır.
> Böylelikle metilasyon verisi ile mRNA düzeyleri arasında karşılaştırma yapmamıza olanak sağlar.

## Programı başlatmadan önce
Programı başlatmadan önce Excell'den veri işlememizi sağlayan **openpyxl** modülünü ve **load_workbook** fonksiyonunu içeriye aktarmamız gerekmektedir. Ayrıca metilasyon tablosu ve mRNA düzeyleri aynı excell dosyası içerisinde farklı sheetlerde bulunmalıdır.

## Program başladıktan sonra
Program çalıştırıldığı anda **kullanıcıdan birkaç bilgi istemektedir.** Bunlar; verilerin bulunduğu **excell dosyası(uzantısıyla beraber)**, **yeni oluşturulacak dosyanın adı(uzantısıyla beraber)**, **sheetlerin numaraları (sheetler 0'dan numaralandırılmaya başlanır).**
Bu işlemlerden sonra döngü çalışmaya başlar ve dosyanın büyüklüğüne göre çalışma süresi değişebilmektedir.
## Programın içeriği

Programda, iç içe 4 döngü bulunmaktadır. Genel mantık itibariyle öncelikle;

 - DNA metilasyon verilerinin bulunduğu tablodan kişilere ulaşmak için her **kolonu tarar.**
 - Ardından aynı **işlemi gen isimleri için yapar.**
 - Kişi isimleri ve gen isimleri tamamlandıktan sonra, verilerin
   alınacağı diğer sheet üzerinden **kolon taraması yaparak birbirine eşit olan kolon yani kişi değerlerini alır.**
 - Kişi değerleri eşleştiğinde **gen taraması yaparak eşleşme arar.**
 - Gen ve kişi eşleştiğinde ise **kesişim noktalarındaki değeri alarak** yeni oluşturduğu dosya içerisine yazmaya başlar.
 - Bu işlemi **döngü içerisinde** her kişi ve gen için uygular.

## Önemli
Programı denemek ve hızlı bir sonuç alması açısından örnek bir Excell dosyası kaydedilmiştir. 
Bu program henüz büyük veriler için test aşamasındadır.
