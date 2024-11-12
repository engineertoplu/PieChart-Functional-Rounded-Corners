# PieChartFunctional

Piechart from highcharts library in html format.

TR
-Köşeleri yuvarlanmış pie chart için highcharts kütüphanesi kullanıldı.
-Datalar fonksiyonel olarak doldurulabilir ve seçilen alan seçildiği anda true değeri dönmesi sağlandı.
-Seçilen alan tekrar seçildiğinde durumu eski haline geldiği gibi false değerini alert eder.
-Başka bir alan seçildiğinde daha önce seçilmiş olan alan önceki duruma geçmesi ayarlandı.
-Bu kodlar html içinde kullanıldığı gibi webview olarak da mobilde kullanılabilir fakat kurumsal yerler için lisans isteyebilir.
-webview içinde onJsAlert ile yakalanabilir


EN
-Highcharts library was used for pie chart with rounded corners.
-Data can be filled functionally and the selected area is returned to true when selected.
-When the selected area is selected again, it alerts false as its status returns to its previous state.
-When another area is selected, the previously selected area is set to return to its previous state.
-These codes can be used in html as well as in webview on mobile, but may require a license for corporate locations.
-It can be caught with onJsAlert in webview



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
