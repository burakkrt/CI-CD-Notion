# CI / CD

### **Continuous Integration** (**Sürekli Entegrasyon- CI)**

**Geliştirilen değişikliklerin projeye entegre edilirken uygulanan bir dizi yöntemlerdir.**

Bir projede birden fazla geliştiricinin yaptığı değişiklikler projeye entegre edilirken herhangi bir sorun teşkil etmemesi ve birbirlerinin etkilememesi çok önemlidir. Geliştirilen kodların projeye entegre olmadan önce bir kontrol mekanizmasına tabi olma sürecine CI diyebiliriz. Entegrasyon sürecinde hataların tespit edilip çözümlenmesi önemlidir. Bu sorunları çözmek için çeşitli test otomasyonları kullanılır. Örn. Github ‘da pull request veya Gitlab ‘da merge request işlemleri birleştirme işleminden önce çeşitli testler ile kontrol edilir ve olası hata durumunda birleştirme isteği askıya alınır ve hatanın giderilmesi beklenir.

<aside>
💡 ****Integration Hell (Entegrasyon Cehennemi) :**** Aynı alanda yapılan birden fazla değişikliğin entegrasyon sırasında hata oluşturması ve çakışmaların yaşanması.

</aside>

### Continous Delivery (Sürekli Teslimat  ve  Sürekli Dağıtım- CD)

**CI ‘ işlemlerinden sonra projenin dağıtıma hazır hale getirilip kullanıcıya sunulması işlemleridir.**

### Sürekli Teslimat

CI sürecinin başarılı bir şekilde tamamlanmasının ardından projenin dağıtılmaya hazır bir yapıya (derleme, paketleme vs.) çevrilmesidir.

### Sürekli Dağıtım

Test, derleme ve paketleme gibi işlemlerin arından yazılımın canlı ortama (sunucuya) otomatik dağıtılmasıdır.

### İyi bir CI & CD nasıl uygulanır ?

1. **Otomatik Tetikleme**
Yapılan değişikliklerin entegrasyon sırasında algılanması ve bir dizi testi çalıştıracak şekilde otomatik tetiklenmesi gerekir. Kodunuzun her değişiklikte test edileceğini bilmek geliştiriciye rahatlık sağlar ve işlemlerin unutulma ihtimalini ortadan kaldırır.
2. **Derleme**
Otomatik tetikleme aşamasından sonra tetiklenen CI araçları başarılı olması halinde projenin derlemesi adımına geçilir. Derleyici adı verilen bir özel yazılım tarafından okunur ve dil spesifikasyonlarına uygun olarak düşük seviyeli bir makine koduna çevrilir. Derleyici, kaynak kodu analiz eder, hata kontrolü yapar ve ardından makine kodunu üretir.
3. **Test & QA**
Testlerin yürütülebilmesi için CI / CD aracı doğru yapılandırılmadır ve proje geliştirilmeye devam ederken testlerinde aynı doğrultuda geliştirilmesi yani testlerin sürdürülebilir olması önemlidir.

*Testlerinizin büyük kısmı birim testleri olmalıdır. Birim testleri, paranızın karşılığını verir. Yazması kolay, çalıştırması ucuz ve bakımı en düşük maliyetlidir. - Martin Fowler*
4. **Paketleme**
Yazılımın kaynak kodlarını veya derlenmiş dosyalarını içeren bir paketin oluşturulmasını içerir. Bu paket, genellikle belirli bir sürüm numarasıyla etiketlenir ve kullanıcılara, diğer geliştiricilere veya müşterilere dağıtılmak üzere hazır hale getirilir.
5. **Kabul Testleri**
Yazılımınızın yapması gerekeni yaptığından ve orijinal gereksinimleri karşıladığından emin olmanın bir yoludur. Otomatik kabul testleri için web sitlerini açma ve bazı yerlere tıklama yapabilme gibi kullanıcı davranışlarını simüle edebilen Selenium aracını kullanabilirsiniz.
6. **Teslimat ve Dağıtım**
Tüm test, derleme, paketleme ve kabul testlerinin başarılı bir şekilde gerçekleşmesinin ardından CD sürçlerine geçilebilir ve proje sunulacak ortama aktarılıp kullanıcı ile buluşturulur.

Bundan sonra yazılımda yapacağınız her kod değişikliği tetikleme aşaması ile başlayıp gene aynı aşamalardan geçecektir. CI/CD Pipeline’nın başarılı olması için testlere, kullanım kolaylığına ve güvenliğe çok dikkat edilmelidir.

Böylece **deployment**, tüm proje bittikten sonra bir defa yapılan büyük korkutucu bir iş olmaktan çıkar ve düzenli yapılan kolay bir işlem halini alır.

### CD / CD yazılım sektörüne katkıları ;

- CI/CD, şirketlerin yazılımlarını daha hızlı güncellemelerini ve teslim etmelerini sağladı.
- Kontrollü remote çalışma olanağını mümkün kıldı.
- Sürekli uygulanan testler ile daha sağlam ilerlemeyi sağladı.
- Hataların anında geri bildirim ile developerlere iletilmesi ile hataların büyümeden çözülmesini sağladığı için zamandan tasarrufu sağladı.
- Teslimat adımının kolaylaşmasını sağladı.

Kaynak:  [Hamit SEYREK - Medium](https://medium.com/devopsturkiye/continuous-integration-ve-continuous-delivery-nedir-neden-kullanılmalı-9f5ce57f200e)
