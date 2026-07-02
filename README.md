 # trex_research

 ***
#### *Programlama ile ilgili kısa bi araştırma raporu*
***

 
## 1. Modern Yazılım Geliştirme Pratikleri

  <details>
  <summary>Git nedir? GitHub nedir</summary>
    
* Git, yazılım geliştirme sürecinde kullanılan bir versiyon kontrol sistemidir.

* Kod üzerinde yapılan tüm değişiklikleri kayıt altına alır.

* Birden fazla geliştiricinin aynı proje üzerinde çakışmadan çalışabilmesine olanak sağlar.

* Geriye dönük olarak yapılan değişiklikler incelenebilir.

* GitHub ise Git’in üzerine kurulmuş bulut tabanlı bir platformdur.

* Git reposunu internette saklamaya yarar.

* Açık kaynak projelerin paylaşımı için en çok kullanılan sistemdir.

*  Ekip çalışmasını kolaylaştırmak için issue tracking (sorun takibi), pull request (katkı önerisi), GitHub Actions (otomasyon) gibi ek özellikler sunar.
 
* GitHub ise Git’in üzerine kurulmuş bulut tabanlı bir platformdur.

* Git reposunu internette saklamaya yarar.

* Açık kaynak projelerin paylaşımı<in en çok kullanılan sistemdir.

* Ekip çalışmasını kolaylaştırmak için issue tracking (sorun takibi), pull request (katkı önerisi), GitHub Actions (otomasyon) gibi ek özellikler sunar.
  
</details>

  <details>
<summary>Temel Git komutları: init, clone, add, commit, push, pull, branch, merge</summary>

*  git init

 Yeni bir Git deposu oluşturmak için kullanılır. Bir proje klasöründe git init komutu çalıştırıldığında, o klasör artık Git tarafından izlenmeye başlar. Bu sayede proje içerisinde yapılan her değişiklik Git tarafından kayıt altına    alınabilir.

 Örnek kullanım:
 
 git init 


 Bu komut çalıştırıldığında klasörde .git isimli gizli bir dosya oluşur ve bu dosya projenin tüm sürüm kontrol bilgilerini içerir.

*  git clone

 Var olan bir uzak Git deposunu bilgisayara kopyalamak için kullanılır. Özellikle GitHub üzerindeki projelerin yerel ortama indirilmesinde tercih edilir.

 Örnek kullanım:

 git clone https://github.com/kullanici/proje.git


 Bu komut sayesinde uzak depodaki tüm geçmiş commitler, branchler ve dosyalar yerel bilgisayara aktarılır.

*  git add

 Dosyaları staging area (hazırlık alanı) denilen bölgeye ekler. Bu alan, commit işleminden önce değişikliklerin hazırlanmasını sağlar.

 Örnek kullanım:

 git add dosya.txt
 git add .


 İlk komut sadece belirli bir dosyayı, ikincisi ise proje içindeki tüm değişiklikleri staging alanına ekler.

*  git commit
  
 Staging alanındaki dosyaları kalıcı olarak kaydeder. Commit işlemi, yapılan değişikliklere bir “anlık görüntü” almak gibidir. Her commit, açıklayıcı bir mesajla etiketlenmelidir.

 Örnek kullanım:

 git commit -m "Login ekranı eklendi"


 Bu komut, yapılan değişikliklerin tarihçede anlamlı şekilde tutulmasına yardımcı olur.

*  git push

 Yerelde yapılan commit’lerin uzak depoya (örneğin GitHub’a) gönderilmesini sağlar. Böylece proje ekibinin diğer üyeleri de güncellenmiş koda erişebilir.

 Örnek kullanım:

 git push origin main


 Bu komut, değişiklikleri origin isimli uzak depodaki main branch’ine gönderir.

*  git pull

 Uzak depodaki en güncel değişiklikleri indirip mevcut branch ile birleştirmeye yarar. Bu komut, ekip çalışmasında başkalarının yaptığı güncellemeleri almak için sıkça kullanılır.

 Örnek kullanım:

 git pull origin main


 Böylece uzak depodaki main branch’indeki tüm yeni değişiklikler yerel bilgisayara aktarılır.

*  git branch

 Proje üzerinde dallar (branch) oluşturmaya, görüntülemeye veya yönetmeye yarar. Branch’ler, geliştiricilerin aynı proje üzerinde farklı özellikler geliştirmesini sağlar.

 Örnek kullanım:

 git branch          # mevcut branch’leri listeler
 git branch yeni-ozellik   # yeni bir branch oluşturur
 git checkout yeni-ozellik # o branch’e geçiş yapar


 Branch kullanımı, aynı projede bağımsız geliştirmelerin çakışmadan yapılabilmesine imkân verir.

*  git merge

 İki farklı branch’i birleştirmek için kullanılır. Örneğin, yeni-ozellik branch’inde geliştirilen bir özellik tamamlandığında, bu branch main ile birleştirilir.

 Örnek kullanım:

 git checkout main
 git merge yeni-ozellik


 Bu komutlar sayesinde yeni-ozellik branch’indeki değişiklikler main branch’ine eklenmiş olur. Eğer aynı    çakışan değişiklikler varsa merge conflict oluşabilir ve manuel çözüm gerekir.

</details>

<details>

 <summary>Merge conflict nedir, nasıl çözülür?</summary>
  
Merge conflict Git’te iki dal aynı dosyanın aynı bölümünü farklı şekilde değiştirdiğinde Git’in hangisini seçeceğini bilememesiyle oluşan çakışmadır. Çözümü de basittir: Çakışmalı dosyayı açıp <<<<<<<, =======, >>>>>>> işaretleri arasındaki alternatiflerden mantıklı olan içeriği oluşturacak şekilde metni düzenlersin (gerekirse birleştirebilirsn) bu işaretleri temizlersin sonra değişikliği git add ile sahneleyip git commit ile birleştirmeyi tamamlarsın.
  
 </details>

<details> 
  
<summary>CI/CD nedir? Azure DevOps, GitHub Actions ile pipeline örnekleri </summary>


* CI/CD Nedir?

CI/CD, yazılım geliştirme süreçlerinde kaliteyi artıran ve teslimat hızını yükselten bir yöntemdir.

CI (Continuous Integration – Sürekli Entegrasyon): Geliştiricilerin kodlarını sık sık ana koda entegre etmesi, bu sırada otomatik testlerin ve derleme işlemlerinin çalışmasıdır. Amaç, hataların erkenden tespit edilmesi ve kodun sürekli olarak çalışır durumda kalmasıdır.

CD (Continuous Delivery/Deployment – Sürekli Teslimat / Dağıtım): CI sonrası başarılı olan kodun otomatik olarak test ortamına veya doğrudan canlı ortama aktarılmasıdır.

Continuous Delivery: Kod otomatik olarak test/stage ortamına alınır, canlıya geçiş manuel onayla yapılır.

Continuous Deployment: Kod tüm testlerden geçtikten sonra canlıya otomatik olarak alınır.

Bu yaklaşım sayesinde:

Daha hızlı geri bildirim alınır.

Ürün kalitesi artar.

Dağıtım süreçleri standartlaşır ve insan hatası azalır.

* Azure DevOps ile Pipeline Örneği

Azure DevOps Pipelines, YAML tabanlı veya görsel olarak oluşturulabilen güçlü bir CI/CD aracıdır. Microsoft’un bulut tabanlı çözümlerine doğrudan entegredir.

Basit Azure DevOps Pipeline (YAML)

Aşağıdaki örnek bir .NET uygulaması için CI pipeline’ıdır:

trigger:
- main   # main branch'e push geldiğinde pipeline çalışır

pool:
  vmImage: 'windows-latest'

steps:
- task: UseDotNet@2
  inputs:
    packageType: 'sdk'
    version: '7.0.x'

- script: dotnet restore
  displayName: 'Restore dependencies'

- script: dotnet build --configuration Release
  displayName: 'Build project'

- script: dotnet test --no-build --verbosity normal
  displayName: 'Run tests'


Bu pipeline şu işlemleri yapar:

Main branch’e kod push edildiğinde tetiklenir.

Gerekli .NET SDK kurulumu yapılır.

Paketler restore edilir.

Proje release modda derlenir.

Unit testler çalıştırılır.

Dağıtım (CD) için ek adımlar eklenebilir. Örneğin Azure Web App’e deploy etmek için AzureWebApp task’i kullanılabilir.

* GitHub Actions ile Pipeline Örneği

GitHub Actions, GitHub üzerinde barındırılan projeler için CI/CD iş akışları kurmaya yarayan bir sistemdir. YAML dosyaları .github/workflows/ klasöründe bulunur.

Basit GitHub Actions Workflow

Aşağıdaki örnek yine bir .NET uygulaması için CI pipeline’dır:

name: .NET CI

on:
  push:
    branches: [ "main" ]
  pull_request:
    branches: [ "main" ]

jobs:
  build:
    runs-on: ubuntu-latest

    steps:
    - name: Checkout repository
      uses: actions/checkout@v3

    - name: Setup .NET
      uses: actions/setup-dotnet@v3
      with:
        dotnet-version: '7.0.x'

    - name: Restore dependencies
      run: dotnet restore

    - name: Build
      run: dotnet build --configuration Release --no-restore

    - name: Test
      run: dotnet test --no-build --verbosity normal


Bu workflow şunları yapar:

Main branch’e push veya pull request geldiğinde çalışır.

Ubuntu sanal makinesi üzerinde işlem yapılır.

Kod checkout edilir.

.NET SDK yüklenir.

Restore, build ve test adımları gerçekleştirilir.

</details>

 <details>     
 
 <summary>Ek Maddeler</summary>

SDLC Aşamaları (Yazılım Geliştirme Yaşam Döngüsü)

* Planlama 

* Analiz 

* Geliştirme 

* Test 

* Dağıtım 

* Bakım
  
Metodolojiler

Agile → Esnek, hızlı geri bildirim.

Scrum → Sprint (2-4 hafta), roller (PO, SM, Dev Team).

Kanban → İş akışı panosu (To Do → Doing → Done).


 </details>
 # software_research

***
#### *Programlama Temelleri ve Veri Yapıları Araştırma Raporu*
***

## 2. Programlama Temelleri

<details>
  <summary>Programlama, Derleyici ve Yorumlayıcı Nedir?</summary>
  
* **Programlama Nedir?:** Bilgisayara belirli bir görevi yerine getirmesi için mantıksal adımlar halinde komutlar verme sürecidir.

* **Derleyici (Compiler) nedir?:** Yazılan kaynak kodun tamamını tek bir seferde bilgisayarın anlayabileceği makine diline çeviren yazılımdır.

* **Yorumlayıcı (Interpreter) nedir?:** Kaynak kodu satır satır okuyarak aynı anda makine diline çeviren ve çalıştıran yazılımdır.

* **Program çalıştırma süreci nasıl işler?:** Kod önce derleyici veya yorumlayıcı tarafından makine diline dönüştürülür, ardından işlemci (CPU) bu komutları sırayla çalıştırır.

</details>

<details>
  <summary>Temel Programlama Kavramları</summary>
  
* **Değişkenler, veri tipleri ve operatörler:** Değişkenler verileri hafızada tutan konteynerler, veri tipleri bu verilerin türünü (sayı, metin vb.), operatörler ise verilerle yapılan işlemleri (toplama, karşılaştırma vb.) ifade eder.

* **Koşullar (if-else):** Belirli bir şartın doğru olup olmamasına göre programın farklı kod bloklarını çalıştırmasını sağlayan kontrol yapılarıdır.

* **Döngüler (for, while, foreach):** Belirli bir kod bloğunun, verilen bir şart sağlandığı sürece ardı ardına tekrar tekrar çalıştırılmasını sağlayan yapılardır.

* **Fonksiyonlar ve Metotlar:** Belirli bir görevi yerine getiren, tekrar kullanılabilir ve isimlendirilmiş kod bloklarıdır.

</details>

## 3. Veri Yapıları ve Algoritmalar

<details>
  <summary>Veri Yapıları ve Algoritmalar Nedir?</summary>
  
* **Veri Yapıları ve Algoritmalar:** Veri yapıları verilerin bilgisayarda nasıl organize edileceğini belirler; algoritmalar ise bu verileri kullanarak bir problemi çözmek için izlenen mantıksal adımlardır.

</details>

<details>
  <summary>Temel Veri Yapıları</summary>
  
* **Array (Dizi):** Aynı veri tipindeki elemanların hafızada ardışık olarak saklandığı, sabit boyutlu veri yapılarıdır.

* **List (Liste):** Eleman ekleme ve çıkarma işlemlerine izin veren, boyutu dinamik olarak değişebilen sıralı veri yapılarıdır.

* **Linked List (Bağlı Liste):** Her bir elemanın hem kendi verisini hem de bir sonraki elemanın adresini tuttuğu dinamik bir zincir yapısıdır.

* **Stack (Yığın):** Eleman işlemlerinin sadece en üstten yapıldığı, "Son Giren İlk Çıkar" (LIFO) prensibiyle çalışan yapıdır.

* **Queue (Kuyruk):** Elemanların arkadan eklenip önden çıkarıldığı, "İlk Giren İlk Çıkar" (FIFO) prensibiyle çalışan yapıdır.

* **Hash Table / Dictionary:** Verilere hızlı erişim sağlamak amacıyla benzersiz birer "anahtar-değer" (key-value) çifti olarak saklayan yapılardır.

* **Set (Küme):** İçerisinde aynı elemandan sadece bir tane barındıran, sırasız ve benzersiz verilerden oluşan topluluklardır.

* **Tree (Ağaç):** Verilerin bir kök düğüm etrafında hiyerarşik (ebeveyn-çocuk ilişkisiyle) olarak organize edildiği doğrusal olmayan yapılardır.

* **Graph (Graf):** Verilerin (düğümler) ve bu veriler arasındaki ilişkilerin (kenarlar) ağ benzeri bir yapıyla modellendiği veri yapılarıdır.

</details>

<details>
  <summary>Algoritmalar</summary>
  
* **Linear Search (Doğrusal Arama):** Aranan elemanı bulmak için dizideki tüm elemanları baştan sona sırayla kontrol eden en temel arama algoritmasıdır.

* **Binary Search (İkili Arama):** Sıralı bir dizide, her adımda arama aralığını yarıya indirerek hedef elemanı çok hızlı bulan algoritmadır.

* **Sorting Algoritmaları (Sıralama Algoritmaları):** Karışık haldeki verileri belirli bir kritere göre (küçükten büyüğe vb.) düzenli bir sıraya koyan algoritmalardır.

* **Bubble Sort (Baloncuk Sıralaması):** Yan yana olan elemanları sürekli karşılaştırıp gerekirse yer değiştirerek en büyük elemanları adım adım sona taşıyan basit sıralama algoritmasıdır.

* **Selection Sort (Seçmeli Sıralama):** Her adımda dizideki en küçük elemanı bularak onu doğru sıradaki yerine yerleştiren sıralama algoritmasıdır.

* **Merge Sort (Birleştirmeli Sıralama):** Diziyi sürekli ikiye bölüp en küçük parçaya ayırdıktan sonra, bu parçaları sıralı olarak birleştirerek sonuca ulaşan "böl ve yönet" algoritmasıdır.

* **Quick Sort (Hızlı Sıralama):** Rastgele bir eleman (pivot) seçip, diğer elemanları bu pivottan küçük ve büyük olarak ayırarak çalışan hızlı bir "böl ve yönet" algoritmasıdır.

* **Recursion (Özyineleme):** Bir fonksiyonun, bir problemi daha küçük alt problemlere bölerek kendi kendisini doğrudan veya dolaylı olarak çağırma tekniğidir.

</details>

<details>
  <summary>Performans ve Karmaşıklık (Complexity)</summary>
  
* **Big O Notation (Big O Gösterimi):** Bir algoritmanın girdi boyutu büyüdükçe performansının ve kaynak tüketiminin nasıl değiştiğini gösteren matematiksel ölçüdür.

* **Time Complexity (Zaman Karmaşıklığı):** Bir algoritmanın çalışması için gereken sürenin, girdi miktarına bağlı olarak nasıl arttığını ifade eden kavramdır.

* **Space Complexity (Alan Karmaşıklığı):** Bir algoritmanın çalışırken bilgisayar hafızasında (RAM) ne kadar ek yere ihtiyaç duyduğunu gösteren kavramdır.

</details>

## 4. Nesne Yönelimli Programlama (OOP)

<details>
  <summary>OOP Nedir?</summary>
  
* **OOP (Object-Oriented Programming):** Yazılımı, gerçek dünyadaki nesneleri modelleyerek tasarlamayı sağlayan, kodun tekrar kullanılabilirliğini ve yönetilebilirliğini artıran bir programlama yaklaşımıdır.

</details>

<details>
  <summary>Temel Kavramlar</summary>
  
* **Class (Sınıf):** Nesnelerin özelliklerini (property) ve davranışlarını (method) tanımlayan, onlara şekil veren temel şablonlardır.

* **Object (Nesne):** Sınıfların (Class) bellekte oluşturulmuş ve kullanılmaya hazır somut örnekleridir.

* **Property (Özellik):** Bir nesnenin durumunu, verisini veya sahip olduğu özellikleri tutan değişkenlerdir.

* **Method (Metot):** Bir nesnenin yapabileceği işlemleri veya sergileyebileceği davranışları tanımlayan fonksiyonlardır.

* **Constructor (Yapıcı Metot):** Bir nesne bellekte ilk oluşturulduğunda otomatik olarak çalışan ve nesnenin ilk ayarlarını yapan özel bir metottur.

</details>

<details>
  <summary>OOP Prensipleri</summary>
  
* **Encapsulation (Kapsülleme):** Bir nesnenin iç işleyişini ve verilerini dış dünyadan gizleyerek, verilere sadece izin verilen yöntemlerle (get/set) güvenli erişim sağlama prensibidir.

* **Inheritance (Kalıtım/Miras):** Bir sınıfın, başka bir sınıfın özelliklerini ve metotlarını devralarak kod tekrarını önlemesi ve hiyerarşik bir yapı kurmasıdır.

* **Polymorphism (Çok Biçimlilik):** Farklı nesnelerin aynı metoda sahip olmalarına rağmen, bu metodu kendi içlerinde farklı şekillerde çalıştırabilme (uygulayabilme) yeteneğidir.

* **Abstraction (Soyutlama):** Karmaşık bir sistemin sadece gerekli olan temel özelliklerini dışa sunup, arka plandaki karmaşık detayları gizleme işlemidir.

</details>

<details>
  <summary>İleri Seviye OOP Kavramları</summary>
  
* **Interface (Arayüz):** Sınıfların hangi metotları içermesi gerektiğini belirten ancak bu metotların nasıl çalışacağına karışmayan bir sözleşme (şablon) yapısıdır.

* **Abstract Class (Soyut Sınıf):** Doğrudan nesnesi oluşturulamayan, sadece diğer sınıflara kalıtım vermek amacıyla ve ortak özellikleri tek bir yerde toplamak için kullanılan temel sınıflardır.

* **Virtual / Override (Sanal / Ezme):** Temel sınıftaki bir metodun `virtual` olarak işaretlenip, miras alan alt sınıflarda `override` edilerek (ezilerek) yeniden yazılabilmesine olanak tanıyan yapıdır.

* **Generic Types (Jenerik Tipler):** Kodun belirli bir veri tipine bağlı kalmadan, çalıştırılacağı zaman belirlenen her türlü veri tipiyle güvenli bir şekilde çalışabilmesini sağlayan yapıdır.

* **Extension Methods (Genişletme Metotları):** Mevcut bir sınıfın kaynak kodunu değiştirmeden veya o sınıftan miras almadan, o sınıfa dışarıdan sonradan yeni metotlar eklememizi sağlayan özelliktir.

</details>

## 5. Web Geliştirme Mimarisi: Frontend ve Backend

<details>
  <summary>Frontend ve Backend Farkları</summary>
  
* **Frontend (Ön Yüz):** Kullanıcının doğrudan gördüğü, tıkladığı ve etkileşime girdiği her şeydir. Örneğin Binance gibi bir platforma girdiğinde gördüğün o anlık fiyat grafikleri, yeşil kırmızı al-sat butonları veya arayüzün tasarımı tamamen Frontend'dir. Senin bilgisayarının veya telefonunun donanımı kullanılarak ekrana çizilir. Görsel olarak kusursuz olabilir ama arkadan veri gelmediği sürece tek başına hiçbir işlem yapamaz.Kullanıcının gördüğü ve tıkladığı yerdir. (Örn: Bir alışveriş sitesindeki ürün fotoğrafları, "Sepete Ekle" butonu).

* **Backend (Arka Yüz):** İşin asıl beyni ve çalışan motorudur. Sen "Al" butonuna bastığında o emrin sisteme iletilmesi, piyasadaki uygun bir "Sat" emriyle eşleştirilmesi ve cüzdanındaki bakiyenin güncellenmesi işlemlerinin yapıldığı yerdir. Senin cihazında değil, uzaktaki güçlü sunucularda çalışır. Kullanıcının göremediği, sistemin beyni ve veritabanı kısmıdır. (Örn: Ürünlerin stok bilgisi, kredi kartı güvenliği ve ödeme onayı).

</details>

<details>
  <summary>Backend'in Temel Bileşenleri ve Çalışma Mantığı</summary>

**1. İş Kuralları (Business Logic)**
* Uygulamanın "zekasını" barındıran algoritmalar ve kod bloklarıdır. Sistemdeki her hareketin mantıksal kontrolü burada yapılır.
* Örneğin 10x kaldıraçlı bir işlem (Long/Short) açmak istediğinde arka planda çalışan Java veya farklı bir dildeki sınıflar (class'lar) ve metotlar devreye girer.
* Backend anında şu hesaplamaları yapar: "Kullanıcının cüzdanında yeterli marjin var mı? Bu işlem için likidasyon seviyesi hangi fiyata denk gelmeli? Piyasada bu emri karşılayacak hacim var mı?" Şartlar sağlanmıyorsa Frontend'e "Yetersiz bakiye" hatasını fırlatan yer burasıdır.

**2. Veritabanı İşlemleri**
* Verilerin geçici bellekte değil, kalıcı olarak saklandığı ve yönetildiği yerdir.
* Telefonunu kapatıp açtığında veya oyundan çıkıp tekrar girdiğinde (örneğin rekabetçi bir oyundaki MMR sıralamanın) kaybolmamasının tek sebebi, bu bilgilerin Backend'e bağlı devasa veritabanlarına yazılmış olmasıdır.
* Backend, senin bir eylemin sonucunda veritabanına bağlanır ve verileri günceller. Veritabanındaki "Linked List" veya ağaç (Tree) yapıları sayesinde milyonlarca veri arasından senin hesabını saniyeden kısa sürede bulup getirir.

**3. Güvenlik**
* Sistemin ve kullanıcı verilerinin kötü niyetli hareketlerden korunmasını sağlayan kalkandır.
* Giriş şifren veritabanında asla düz metin olarak saklanmaz; Backend bu şifreyi geri döndürülemez matematiksel algoritmalara sokarak (hashleyerek) kaydeder.
* Ayrıca yetki kontrolü yapar. Hesaptan bir çıkış veya transfer isteği geldiğinde Backend, "Bu istek gerçekten o kişinin cihazından mı geliyor? Gerekli iki aşamalı doğrulama kodları girilmiş mi?" gibi kontrolleri yaparak sistemi güvende tutar.


**4. API Servisleri**
* Frontend ile Backend'in aynı dili konuşmasını ve veri alışverişi yapmasını sağlayan köprüdür. 
* Sen uygulamayı açtığında, Frontend ekrandaki verileri doldurmak için API üzerinden Backend'e bir istek (Request) atar.
* Backend veritabanından gerekli bilgileri alır, gereksiz detayları kırpar ve anlaşılır, saf bir veri formatında (genellikle JSON formatında, örneğin `{"bakiye": 500, "coin": "SOLANA"}` şeklinde) API aracılığıyla geri gönderir. Frontend de bu saf veriyi alıp arayüzdeki o süslü kutucukların içine yerleştirir.

</details>

## 6. İstemci-Sunucu (Client-Server) Mimarisi

<details>
  <summary>Client-Server Mimarisi Nedir?</summary>
  
* **Client-Server Mimarisi:** İnternet üzerindeki uygulamaların ve cihazların birbirleriyle nasıl iletişim kurduğunu tanımlayan temel ağ modelidir. Temel mantığı, iş yükünün "hizmeti talep eden" (İstemci) ile "hizmeti sağlayan" (Sunucu) arasında paylaştırılmasına dayanır.

</details>

<details>
  <summary>Client (İstemci) ve Server (Sunucu)</summary>
  
* **Client (İstemci):** Son kullanıcının doğrudan etkileşime girdiği cihaz veya yazılımdır. Girdiğiniz web tarayıcısı (Chrome, Safari), telefonunuzdaki bir mobil uygulama veya bilgisayarınızdaki bir oyun istemcisi olabilir. Kendi başına yeterli veriye sahip olmadığı için, ihtiyaç duyduğu bilgileri sunucudan talep eder.

* **Server (Sunucu):** İstemcilerden gelen talepleri 7/24 dinleyen, bu talepleri işleyen, verileri güvenli bir şekilde barındıran güçlü bilgisayarlar veya sistemlerdir. İstemci "bana şu bilgiyi ver" dediğinde veritabanına bağlanıp o bilgiyi bulmak ve geri göndermek sunucunun görevidir.

</details>

<details>
  <summary>İletişim Döngüsü: Request ve Response</summary>
  
* **Request (İstek):** Client tarafından Server'a gönderilen "işlem talebi" mesajıdır. Örneğin; bir e-ticaret sitesinde arama çubuğuna bir ürün yazıp "Ara" butonuna bastığınızda, Client arka planda Server'a "Bana bu isme sahip ürünleri getir" diyen bir Request gönderir.

* **Response (Yanıt):** Server'ın gelen Request'i (isteği) işledikten sonra Client'a geri gönderdiği sonuç paketidir. Bu yanıt, talep edilen ürünlerin listesi (genellikle JSON formatında) olabileceği gibi, eğer ürün bulunamadıysa veya sistemde bir hata varsa bir hata mesajı (örneğin; 404 Not Found) da olabilir. Client bu Response'u alır ve kullanıcının ekranında görselleştirir.

</details>

## 7. HTTP Protokolü ve İletişim Standartları

<details>
  <summary>HTTP Protokolü Nedir?</summary>
  
* **HTTP Protokolü:** İstemci (Client) ve Sunucu (Server) arasında veri alışverişinin nasıl yapılacağını belirleyen, internetin temel iletişim standartları ve kuralları bütünüdür.

</details>

<details>
  <summary>HTTP Metotları</summary>
  
* **GET:** Sunucudan sadece veri okumak veya bilgi getirmek için kullanılır.
* **POST:** Sunucuya yeni bir veri göndermek ve veritabanında yeni bir kayıt oluşturmak için kullanılır.
* **PUT:** Sunucudaki mevcut bir kaydı *tamamen* değiştirmek (üzerine yazmak) için kullanılır.
* **PATCH:** Sunucudaki mevcut bir kaydın sadece *belirli bir parçasını* (örn: sadece şifreyi) güncellemek için kullanılır.
* **DELETE:** Sunucudaki belirli bir veriyi silmek için kullanılır.

</details>

<details>
  <summary>HTTP Status (Durum) Kodları</summary>
  
**2xx - Başarı Durumları**
* **200 OK:** İstek kusursuz bir şekilde işlendi ve beklenen yanıt geri döndürüldü.
* **201 Created:** İstek başarıyla işlendi ve bunun sonucunda sunucuda yeni bir kaynak (kayıt) başarıyla oluşturuldu.

**4xx - İstemci (Client) Hataları**
* **400 Bad Request:** İstek hatalı, eksik veya sunucunun anlayamayacağı bir formatta gönderildi.
* **401 Unauthorized:** Bu işlemi yapabilmek için sisteme giriş yapmış olman (kimliğini doğrulaman) gerekiyor.
* **403 Forbidden:** Sisteme giriş yapmış olabilirsin ancak bu işlemi yapmaya yetkin (iznin) yok.
* **404 Not Found:** İstediğin sayfa, dosya veya veri sunucuda bulunamadı.

**5xx - Sunucu (Server) Hataları**
* **500 Internal Server Error:** İstemcinin isteği doğru olsa da sunucu tarafında (Backend) beklenmeyen bir çökme veya kod hatası meydana geldi.

</details>

## 8. JSON (JavaScript Object Notation)

<details>
  <summary>JSON Nedir?</summary>
  
* **JSON:** Verileri depolamak ve farklı sistemler (örneğin Frontend ve Backend) arasında taşımak için kullanılan, metin tabanlı evrensel bir veri formatıdır. Temel mantığı tamamen "Anahtar-Değer" (Key-Value) ilişkisine dayanır.Kısaca anlatmak gerekirse API iki dağ arasında köprü JSON ise arabalar halinde geçen bilgiler.Burdaki dağlar iki farklı sisteme , arabalar da verilere benzetilmiştir.

</details>

<details>
  <summary>Neden Kullanılır?</summary>
  
* **Hafif (Lightweight):** XML gibi gereksiz açılış-kapanış etiketleri kullanmaz. Veriyi minimum karakterle ifade ettiği için dosya boyutu küçüktür, bu da ağ üzerindeki veri transferini inanılmaz derecede hızlandırır.
* **İnsan Tarafından Okunabilir (Human-readable):** Karmaşık makine kodları içermez. Sadece süslü `{}` ve köşeli `[]` parantezler kullanarak hiyerarşik bir yapı kurar, böylece bir geliştirici veriyi baktığı anda kolayca okuyup anlayabilir.
* **Platform Bağımsız (Platform Independent):** Temelde sadece düz bir "metin" (text) dosyasıdır. Java, C#, JavaScript, Swift gibi birbirinden tamamen farklı dillerin hepsi JSON formatını tanır ve kendi içindeki nesnelere sorunsuz bir şekilde çevirebilir. Sistemler arası evrensel bir dildir.

</details>

<details>
  <summary>Örnek JSON Yapısı (Objeleştirme)</summary>
  
Aşağıda bir "Kullanıcı" nesnesinin JSON formatında nasıl modellendiğini görebilirsiniz:

```json
{
  "isim": "Ahmet",
  "yas": 24,
  "aktif_mi": true,
  "yetenekler": ["Java", "Git", "SQL"],
  "iletisim": {
    "email": "ahmet@ornek.com",
    "sehir": "İstanbul"
  }
}
```
</details>

## 9. XML (eXtensible Markup Language)

<details>
  <summary>XML Nedir?</summary>
  
* **Tanım:** Verileri depolamak ve farklı sistemler arasında taşımak için kullanılan, etiket (tag) tabanlı bir işaretleme dilidir. 
* **Mantığı:** HTML'e çok benzer ancak temel bir farkı vardır: HTML veriyi tarayıcıda görsel olarak sergilemek için tasarlanmıştır, XML ise sadece veriyi taşımak ve ne olduğunu tanımlamak için vardır.
* **Esneklik:** "Genişletilebilir" (eXtensible) olmasının sebebi, HTML'deki gibi sabit etiketler yerine kendi etiketlerini (Örn: `<kullanici>`, `<isim>`) özgürce yaratabilmendir.

**Örnek bir XML Yapısı:**
```xml
<kullanici>
    <isim>Ahmet</isim>
    <yas>24</yas>
    <yetenekler>
        <yetenek>Java</yetenek>
        <yetenek>Git</yetenek>
    </yetenekler>
</kullanici>
 ```


<details>
<details>

## 10. Protocol Buffers (Protobuf) ve gRPC

  <summary>Protocol Buffers (Protobuf) Nedir?</summary>
  
* **Tanım:** Google tarafından geliştirilen, verileri JSON veya XML gibi metin (text) formatında değil, **ikili kod (binary)** formatında serileştiren (paketleyen) bir yapıdır.
* **Avantajı:** İnsanlar tarafından doğrudan okunamaz ancak JSON'a göre çok daha küçük boyutludur. Bu sayede veriler ağ üzerinde çok daha az bant genişliği tüketir ve makineler tarafından inanılmaz hızlı işlenir.
* **Yapısı:** Verinin şablonu bir `.proto` dosyasında tanımlanır ve sistem bu şablonu kullanarak veriyi sıkıştırıp karşı tarafa iletir.

</details>

<details>
  <summary>gRPC ve Mikro Servis İletişimi</summary>

* **Mikro Servis (Microservices) İletişimi:** Modern devasa uygulamalar tek bir bütün yerine, küçük ve bağımsız çalışan servislerden (Örn: Ödeme servisi, Kullanıcı servisi) oluşur. Bu servislerin kendi aralarında saniyede binlerce kez haberleşmesi gerekir. JSON bu yoğun trafik için bazen yavaş kalabilir.
* **gRPC Nedir?:** Google tarafından geliştirilen yüksek performanslı bir iletişim sistemidir. API'lerin JSON ve REST kullandığı yerde, gRPC veri formatı olarak **Protobuf** kullanır.
* **Nasıl Çalışır?:** Bir mikro servis, başka bir sunucudaki mikro servisin içindeki bir metodu (fonksiyonu) sanki kendi bilgisayarındaymış gibi doğrudan çağırabilir (Remote Procedure Call). Yüksek hızlı ve düşük gecikmeli backend-to-backend (sunucudan sunucuya) iletişimde sektör standardıdır.

</details>
