# PieChartFunctional

Rounded corners Piechart from highcharts library in html format. Android, Ios, Web

TR
-Köşeleri yuvarlanmış pie chart için highcharts kütüphanesi kullanıldı.
-Datalar fonksiyonel olarak doldurulabilir ve seçilen alan seçildiği anda true değeri dönmesi sağlandı.
-Seçilen alan tekrar seçildiğinde durumu eski haline geldiği gibi false değerini alert eder.
-Başka bir alan seçildiğinde daha önce seçilmiş olan alan önceki duruma geçmesi ayarlandı.
-Bu kodlar html içinde kullanıldığı gibi webview olarak da mobilde kullanılabilir fakat kurumsal yerler için lisans isteyebilir.
-webview içinde onJsAlert ile yakalanabilir
-Chart js örneği de eklendi


EN
-Highcharts library was used for pie chart with rounded corners.
-Data can be filled functionally and the selected area is returned to true when selected.
-When the selected area is selected again, it alerts false as its status returns to its previous state.
-When another area is selected, the previously selected area is set to return to its previous state.
-These codes can be used in html as well as in webview on mobile, but may require a license for corporate locations.
-It can be caught with onJsAlert in webview
-chart js example also added



TR
this.sliced: tıklanan alanın durumunu true false döner
this.slice: seçilen alanı animasyonla dışarı doğru açar benzer kullanımı this.slice(true) veya this.slice(false). true ve false değeri kullanıcıya özel durumlarda seçim için ayarlanmış
this.series.data.forEach(point => {
                                    if (point !== this) {
                                        point.slice(false);
                                    }
                                });  // Bütün alanları seçilmemiş hale getirir
                                
this.update({
                borderColor: 'black',
                borderWidth: 2
            }); // Alana 2 birim büyüklüğünde siyah kenarlar ekler, seçim zamanı kullanışlı olabilir.

            
EN
this.sliced: returns the state of the clicked area as true or false
this.slice: animates the selected area outwards, similar usage is this.slice(true) or this.slice(false). True and false values ​​are set for user-specific selection cases
this.series.data.forEach(point => {
                                    if (point !== this) {
                                        point.slice(false);
                                    }
                                });  // Deselects all fields

this.update({
                borderColor: 'black',
                borderWidth: 2
            }); // Adds 2-unit black borders to the area, which can be useful at selection time.

<img width="270" alt="Screen Shot 2024-11-12 at 14 37 49" src="https://github.com/user-attachments/assets/cb967054-fd56-4837-be17-e3ed4a51299e">
<img width="241" alt="Screen Shot 2024-11-12 at 14 38 12" src="https://github.com/user-attachments/assets/8bcdca30-f85e-4faf-8bc2-5c9b9e7ffbb9">
<img width="244" alt="Screen Shot 2024-11-12 at 14 39 03" src="https://github.com/user-attachments/assets/bf0f3ebb-f816-4893-89d5-cc896f8d8438">

--------------------------------

chartpiefinalclean.html
TR
label ismine göre tıklanan alanlar ilkin tıklanıyorsa label ismi ve true değeri, büyüyen alan tekrar tıklanırsa label ismi ve false değeri döneri döner. Küçükken büyüyen alanlar her zaman label ismiyle true döner.
EN 
If the areas clicked according to the label name are clicked first, the label name and true value are returned, if the growing area is clicked again, the label name and false value are returned. The areas growing when small always return true with the label name.

![Screen_Recording_20241128_161728_Chrome-ezgif com-crop](https://github.com/user-attachments/assets/975c111f-68ea-4a95-a472-c0b6ee44a719)
