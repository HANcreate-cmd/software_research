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
</details>

## 10. Protocol Buffers (Protobuf) ve gRPC


<details>

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

## 11. Veritabanı Temelleri

<details>
  <summary>Relational Databases (İlişkisel Veritabanları / SQL)</summary>
  
* **Mantığı:** Verileri kusursuz bir düzen içinde, tıpkı Excel tabloları gibi **satırlar (row)** ve **sütunlar (column)** halinde tutar. En büyük özelliği, tabloların birbirine sıkı kurallarla (Örn: ID numaraları üzerinden) bağlı (ilişkili) olmasıdır. Finans, bankacılık ve e-ticaret gibi verinin hata kaldırmadığı sistemlerde kullanılır.

**Popüler SQL Veritabanları:**
* **SQL Server (MSSQL):** Microsoft tarafından geliştirilmiş, çok güçlü, güvenli ancak lisans maliyetleri yüksek kurumsal bir veritabanıdır. (Örn: Otomobil dünyasındaki Mercedes gibidir; mühendisliği harikadır ama bakımı pahalıdır.)
* **PostgreSQL:** Dünyanın en gelişmiş açık kaynaklı (ücretsiz) ilişkisel veritabanıdır. Karmaşık veri tipleriyle başa çıkma konusunda rakipsizdir. (Örn: Sanayideki elinden her iş gelen, doğru ayarlandığında paralı rakiplerini bile geçen o efsanevi ustadır.)
* **MySQL:** Web dünyasının en eski ve yaygın kullanılan açık kaynaklı veritabanıdır. (Örn: Toyota Corolla gibidir; piyasada çok fazladır, parçası ve çözümü her yerde bulunur, asla yolda bırakmaz.)

</details>

<details>
  <summary>NoSQL Databases (İlişkisel Olmayan Veritabanları)</summary>

* **Mantığı:** Verileri katı tablolara ve sütunlara sıkıştırmak yerine, özgür ve esnek formatlarda (genellikle JSON yapısına benzer şekilde) tutan sistemlerdir. Sistemdeki bir verinin 5, diğerinin 50 özelliği olabilir; kurallar katı değildir.

**Popüler NoSQL Veritabanları:**
* **MongoDB:** Dünyanın en popüler NoSQL veritabanıdır. Verileri "Dokümanlar" (Document) halinde saklar. Şema (Schema) zorunluluğu yoktur, proje değiştikçe yeni veri tiplerini anında kabul eder. (Örn: İçine ne atarsan alan, sınırları olmayan devasa bir klasör gibidir; her müşterinin dosyası farklı boyutta olsa da veriyi anında bulur.)
* **Redis:** Verileri yavaş olan Harddisk'e değil, doğrudan bilgisayarın uçuş hızındaki **RAM belleğine** yazan bir "Key-Value" (Anahtar-Değer) veritabanıdır. İnanılmaz hızlıdır ancak RAM geçici olduğu için ana veritabanı yerine genellikle "Cache" (Önbellek) olarak kullanılır. (Örn: Rekabetçi oyunlardaki anlık maç skoru veya saniyelik top pozisyonu gibi şimşek hızında okunması gereken geçici verilerin tutulduğu yerdir.)

</details>

<details>
  <summary>Temel SQL Sorguları (CRUD İşlemleri)</summary>
  
Veritabanında yapılabilecek en temel 4 işleme **CRUD** (Create, Read, Update, Delete) denir. SQL dillerinde bunların karşılığı şöyledir:

* **SELECT (Okuma):** Veritabanından veri çekmek (okumak) için kullanılır. Sistemi değiştirmez, sadece listeler. (Örn: Sadece kırmızı renkli BMW'leri listele).
* **INSERT (Ekleme):** Tabloya yepyeni bir kayıt (satır) ekler. (Örn: Sisteme yeni bir kullanıcı kaydetmek).
* **UPDATE (Güncelleme):** Var olan bir kaydın içindeki bilgileri değiştirir. (Örn: Aracın yakıt türünü Benzin'den LPG'ye çevirmek. Hangi aracı değiştireceğini filtrelemezsen tüm arabaları güncellersin!).
* **DELETE (Silme):** Var olan bir kaydı tablodan tamamen siler.
</details>

<details>
  <summary>İleri Seviye SQL Kavramları (Bölüm 1)</summary>
  
* **JOIN (Birleştirme):** İlişkisel veritabanlarının (SQL) kalbidir. Parçalanmış farklı tabloları ortak bir ID (kimlik) üzerinden birleştirip anlamlı bir bütün oluşturur. (Örn: Sadece isimlerin olduğu 'Kullanıcılar' tablosu ile sadece ürünlerin olduğu 'Siparişler' tablosunu birleştirip faturayı oluşturmak).
* **GROUP BY (Gruplama):** Verileri belirli bir özelliğine göre kategorilere ayırıp özet (sayı, toplam vb.) çıkarmaktır. (Örn: Sistemdeki oyuncuları ülkelerine göre gruplayıp hangi ülkeden kaç kişi olduğunu saymak).
* **HAVING (Grup Filtreleme):** Standart `WHERE` komutu satırları filtrelerken, `HAVING` komutu `GROUP BY` ile oluşturulmuş **grupları** filtreler. (Örn: Oyuncuları grupladıktan sonra sadece "1000'den fazla oyuncusu olan ülkeleri" listele demek).
</details>

<details>
  <summary>İleri Seviye SQL Kavramları (Bölüm 2: Performans ve Güvenlik)</summary>
  
* **Index (İndeksleme):** Veritabanında arama işlemlerini inanılmaz derecede hızlandıran arka plan fihristidir. 1000 sayfalık kitapta bir kelimeyi sayfa sayfa aramak yerine kitabın arkasındaki "İçindekiler" bölümüne bakmak gibidir. Okuma hızını uçurur ancak yeni veri eklendiğinde fihristin de güncellenmesi gerektiğinden yazma işlemlerini ufak oranda yavaşlatır.
* **View (Sanal Tablo / Görünüm):** Karmaşık sorguları kaydedip, sanki gerçek bir tabloymuş gibi kullanılmasını sağlayan pencerelerdir. (Örn: Güvenlik amacıyla bir çalışana tüm veritabanını vermek yerine, sadece "Maaşlar" sütununun gizlendiği bir "View" penceresi gösterilir).
* **Stored Procedure (Saklı Yordam):** Veritabanı sunucusunun içine doğrudan kaydedilmiş kod bloklarıdır. "Sepeti onayla, stoktan düş, faturayı kes" gibi zincirleme işlemleri tek bir paket (makro) haline getirir. Uygulama sadece bu paketin adını çağırır, işlemler veritabanı içinde çok yüksek hızda ve güvenli bir şekilde peş peşe gerçekleşir.
</details>

<details>
  <summary>ACID Prensipleri (Veritabanı Güvenilirlik Kuralları)</summary>
  
İlişkisel (SQL) veritabanlarında yapılan işlemlerin (transaction) güvenli ve hatasız bir şekilde tamamlanacağını garanti eden 4 temel kuraldır. Bankacılık ve borsa gibi sistemlerin hatasız çalışmasını sağlar.

* **A - Atomicity (Bölünemezlik):** "Ya hep ya hiç" kuralıdır. Bir işlem birden fazla adımdan oluşuyorsa, ya tüm adımlar kusursuzca tamamlanır ya da işlem hata verirse sistem tamamen eski haline döner (Rollback). (Örn: Para transferinde para sizden çıkıp karşıya ulaşmazsa, sistem parayı size geri iade eder; işlem yarıda bırakılmaz).
* **C - Consistency (Tutarlılık):** Yapılan her işlemin, veritabanındaki mevcut kurallara ve kısıtlamalara (constraints) uyması zorunluluğudur. (Örn: "Bakiye eksiye düşemez" kuralı varsa, sistem yetersiz bakiye ile işlem yapılmasına asla izin vermez).
* **I - Isolation (İzolasyon):** Aynı saniyede gerçekleşen binlerce işlemin, birbirlerini etkilemeden sanki sıraya dizilmiş gibi tek tek yapılmasıdır. İşlemler birbirinin verisine müdahale edemez.
* **D - Durability (Kalıcılık):** Başarıyla tamamlandığı (Commit) onaylanan bir verinin, anında elektrik kesilse veya sunucu çökse bile asla kaybolmaması, diske kalıcı olarak yazılmasıdır.
</details>
<details>
  <summary>ORM (Object-Relational Mapping) Nedir?</summary>
  
* **Tanım:** Backend tarafında kullanılan Nesne Yönelimli Programlama (OOP) dillerindeki "Nesneler" ile İlişkisel Veritabanlarındaki (SQL) "Tablolar" arasında köprü kuran otomatik bir çevirmen sistemidir.
* **Mantığı:** Yazılımcı kod tarafında bir `Kullanici` sınıfı (Class) oluşturduğunda, ORM bu sınıfı veritabanında bir "Kullanıcılar" tablosuna; sınıfın içindeki her bir özelliği (isim, yaş vb.) ise tablonun sütunlarına otomatik olarak haritalar (eşler).

</details>

<details>
  <summary>ORM Kullanmanın Avantajları</summary>
  
* **Daha Az SQL (Less SQL):** Veritabanına kayıt eklemek, silmek veya okumak için uzun ve karmaşık SQL sorguları yazmak (Örn: `INSERT INTO...`) gerekmez. Geliştirici sadece kendi programlama dilindeki hazır metotları kullanır (Örn: `repository.save(kullanici)`). ORM bu komutu arka planda otomatik olarak kusursuz bir SQL sorgusuna çevirir.
* **Hızlı Geliştirme (Fast Development):** Geliştirici SQL sözdizimi hatalarıyla veya veritabanı yapılandırmasıyla vakit kaybetmez. Sadece uygulamanın iş mantığına (business logic) odaklandığı için projeler çok daha hızlı geliştirilir.
* **Veritabanı Bağımsızlığı:** Yazılan kod veritabanından bağımsızdır. Proje MySQL'den PostgreSQL'e taşınmak istendiğinde, yazılım kodlarında tek bir satır SQL sorgusu değiştirmeye gerek kalmaz; ORM yeni veritabanının diline anında adapte olur.

</details>

<details>
  <summary>EF Core Nedir?</summary>
  
* **Tanım:** Microsoft tarafından .NET ekosistemi için geliştirilmiş, dünyanın en popüler ve yetenekli ORM (Object-Relational Mapping) aracıdır. C# kodları ile SQL veritabanı arasındaki iletişimi nesne yönelimli (OOP) bir yaklaşımla çözer.

</details>

<details>
  <summary>DbContext ve DbSet Kavramları</summary>
  
* **DbContext (Veritabanı Bağlamı):** Uygulama ile veritabanı arasındaki ana köprü ve oturum yöneticisidir. Veritabanına bağlanma, değişiklikleri takip etme ve verileri kaydetme işlemlerinden sorumludur. (Örn: Bir garajın baş makinisti gibidir; garajla ilgili tüm iletişim ve işlemler onun üzerinden yürütülür).
* **DbSet (Tablo Temsilcisi):** `DbContext` içinde yer alan ve veritabanındaki spesifik bir tabloyu (Örn: Kullanıcılar tablosu) temsil eden koleksiyonlardır. (Örn: Garajın içindeki belirli araçlara ayrılmış özel park alanlarıdır). Okuma, ekleme veya silme işlemleri ilgili `DbSet` üzerinden yapılır.

</details>

<details>
  <summary>Migration (Veritabanı Güncellemesi)</summary>
  
* **Mantığı:** Geliştirme sürecinde yazılım kodları (Modeller/Sınıflar) sürekli değişir. Sınıfa yeni bir özellik eklendiğinde (Örn: Kullanıcıya 'Profil Fotoğrafı' eklemek), veritabanında bu özelliğin karşılığı olan bir sütun yoktur.
* **Ne İşe Yarar?:** Migration, C# kodunda yapılan bu değişiklikleri algılayıp, veritabanındaki tabloları bu yeni duruma uygun hale getirmek için gereken SQL komutlarını otomatik olarak oluşturan "versiyonlama ve güncelleme" aracıdır.
* **Özetle:** Kod ile veritabanı arasındaki yapıyı her zaman senkronize (uyumlu) tutmayı sağlayan mimari plan güncellemeleridir.

</details>

<details>
  <summary>LINQ (Language Integrated Query) Nedir?</summary>
  
* **Tanım:** C# dilinin içine entegre edilmiş, koleksiyonlar (diziler, listeler) veya veritabanı tabloları (DbSet) üzerinde SQL benzeri sorgular yapmamızı sağlayan yapıdır.
* **Mantığı:** Geliştiricinin karmaşık SQL metinleri yazmasına gerek kalmaz. Doğrudan C# nesneleri (OOP) kullanılarak yazılan LINQ komutları (Örn: `arabalar.Where(a => a.Marka == "BMW")`), EF Core tarafından arka planda otomatik olarak SQL sorgusuna dönüştürülüp veritabanına iletilir.
</details>

<details>
  <summary>Temel LINQ Operasyonları</summary>
  
* **Where (Filtreleme):** Listedeki elemanlar arasından sadece verilen koşulu sağlayanları (Örn: Kilometresi 100 binden küçük olan araçları) süzüp getiren filtreleme metodudur.
* **Select (Seçme / Dönüştürme):** Bir nesnenin tamamını değil, sadece istenilen belirli özelliklerini (Örn: Arabaların sadece plakalarını) çekmek veya veriyi farklı bir formata dönüştürmek için kullanılır. (Projeksiyon işlemi).
* **OrderBy / OrderByDescending (Sıralama):** Listeyi belirtilen bir özelliğe göre küçükten büyüğe (veya tam tersi) sıralar. (Örn: Araçları üretim yılına göre eskiden yeniye dizmek).
* **GroupBy (Gruplama):** Verileri ortak bir özelliğine göre alt kümelere ayırır. (Örn: Tüm araçları markalarına göre paketler halinde gruplandırmak).
* **Join (Birleştirme):** Ortak bir değere (Örn: Müşteri ID) sahip iki farklı listeyi eşleştirip, iki tarafın verilerini içeren tek bir birleşik sonuç (Örn: Araçlar ve Sahipleri tablosu) üretir.
</details>
<details>
  <summary>EF Core Yaklaşımları: Code First vs Database First</summary>

Projelerde veritabanı ile yazılım kodu arasındaki köprüyü inşa etmeye hangi taraftan başlanacağını belirleyen iki temel felsefe vardır:

* **Code First (Koddan Veritabanı Üretme):** Modern ve en yaygın yaklaşımdır. Ortada veritabanı yoktur. Geliştirici önce OOP mantığıyla C# sınıflarını (modellerini) yazar. Ardından EF Core (Migration aracıyla) bu kodlara bakar ve uygun SQL veritabanını sıfırdan inşa eder. *(Örn: Önce mimari planı kağıda çizip, sonra o plana göre gerçek binayı inşa etmektir. Kontrol kodlardadır.)*
* **Database First (Veritabanından Model Üretme):** Genellikle halihazırda var olan eski/büyük projelere dahil olunduğunda kullanılır. Veritabanı zaten mevcuttur. EF Core (Scaffolding yöntemiyle) mevcut veritabanına bağlanır, tabloları inceler ve geliştiricinin kullanması için gerekli C# sınıflarını otomatik olarak üretir. *(Örn: Halihazırda var olan eski bir binanın içine girip, ölçümler yaparak o fiziksel binanın mimari krokisini kağıda dökmektir. Kontrol veritabanındadır.)*

</details>

## 12. Docker ve Containerization

<details>
  <summary>Docker Nedir?</summary>
  
* **Tanım:** Uygulamaları ve onların çalışması için gereken tüm bağımlılıkları (kütüphaneler, ortam değişkenleri) tek bir standart paket olan **"Konteyner" (Container)** içine hapseden platformdur.
* **Çözdüğü Sorun:** Geliştiricilerin korkulu rüyası olan "Benim bilgisayarımda çalışıyordu, sunucuda neden hata veriyor?" sorununu çözer. Docker konteyneri içine hapsedilen bir uygulama, Linux, Windows veya Bulut ortamı fark etmeksizin her yerde kusursuz ve aynı şekilde çalışır. (Tıpkı içindeki yük ne olursa olsun dünyadaki her gemiye, tıra ve vince tam uyum sağlayan standart çelik nakliye konteynerleri gibi).

</details>

<details>
  <summary>Kubernetes (K8s) Nedir?</summary>

* **Tanım:** Google tarafından geliştirilen, binlerce Docker konteynerinin otomatik olarak dağıtılmasını, ölçeklendirilmesini ve yönetilmesini sağlayan **"Konteyner Orkestrasyon"** aracıdır.
* **Ne İşe Yarar?:** Tek bir konteyneri elde yönetmek kolaydır ancak devasa bir sistemde binlerce konteyneri yönetmek imkansızdır. Kubernetes, bu sistemin "Vinç Operatörü"dür. Bir konteyner çöktüğünde anında yerine yenisini açar (Self-healing), trafiğin arttığı kampanya günlerinde kopyalar oluşturarak sistemi büyütür (Auto-scaling) ve trafik düştüğünde sistemi küçülterek maliyetleri düşürür.

</details>

<details>
  <summary>Docker vs Kubernetes Farkı</summary>

* Sanılanın aksine bu iki teknoloji birbirine **rakip değildir**, birbirini tamamlayan teknolojilerdir.
* **Docker**, uygulamayı çalıştırılabilir, izole bir kutuya (konteynere) koyma işlemidir.
* **Kubernetes** ise o kutulardan binlercesini aynı anda yöneten, organize eden ve trafik akışını sağlayan liman yönetim sistemidir.
* Küçük projelerde Kubernetes olmadan sadece Docker kullanılabilir, ancak devasa mikro servis projelerinde Docker konteynerlerini yönetmek için Kubernetes şarttır.

</details>
<details>
  <summary>Docker Bileşenleri: Dockerfile, Image ve Container</summary>
  
Docker ekosisteminde bir uygulamanın ayağa kalkma sürecini oluşturan 3 temel yapı taşı vardır:

* **Dockerfile (Montaj Kılavuzu):** Uygulamanın nasıl paketleneceğini, içine hangi kütüphanelerin (Örn: Java 17, Ubuntu) kurulacağını adım adım belirten düz bir metin dosyasıdır.
* **Docker Image (Dondurulmuş Kalıp / Kurulum Dosyası):** Dockerfile talimatları doğrultusunda derlenen, uygulamanın çalışmaya hazır ancak kendi başına değiştirilemez (read-only) olan paketlenmiş halidir. Bir oyunun internetten indirilen setup (ISO) dosyası gibidir.
* **Docker Container (Canlı Çalışan Örnek):** İmaj kalıbının sunucuda veya bilgisayarda canlandırılmış, aktif olarak RAM üzerinde **çalışan halidir**. Tek bir imaj kalıbından (Setup dosyasından) yan yana binlerce bağımsız çalışan container (canlı uygulama) üretilebilir.

</details>

<details>
  <summary>Docker Compose Nedir?</summary>

* **Tanım:** Birden fazla Docker konteynerine sahip karmaşık uygulamaları (Örn: Aynı anda çalışması gereken bir Backend, bir Frontend ve bir SQL Veritabanı) tek bir merkezden tanımlayıp yönetmeyi sağlayan araçtır.
* **Mantığı:** Tüm bu servislerin ayarları ve birbirleriyle nasıl konuşacakları `docker-compose.yml` adlı tek bir dosyada yazılır. Geliştirici her konteyneri tek tek elle başlatmak yerine `docker-compose up` komutunu yazarak tüm sistemi tek bir hamlede kusursuz bir uyumla ayağa kaldırır.

</details>

<details>
  <summary>Docker'ın Sağladığı Temel Avantajlar</summary>

* **Ortam Bağımsızlığı (Environment Independence):** Uygulamanın çalışacağı işletim sistemi, sürüm farklılıkları veya bağımlılık sorunları tamamen tarih olur. Uygulama geliştiricinin yerel bilgisayarında nasıl çalışıyorsa; test ortamında veya canlı sunucuda (production) da birebir aynı kararlılıkla çalışır.
* **Kolay Deployment (Hızlı Canlıya Alma):** Sunucu üzerinde dakikalarca veya saatlerce süren altyapı kurulumu (Java versiyonu eşleme, veritabanı indirme, port yönlendirme) ihtiyacını ortadan kaldırır. Hazırlanan Docker imajı sunucuya tek bir komutla çekilir ve saniyeler içinde uygulama yayına (canlıya) alınır.

</details>

## 13. API Teknolojileri

<details>
  <summary>REST API Prensipleri</summary>
  
REST, farklı sistemlerin (Frontend, Backend, Mobil) internet üzerinden birbiriyle konuşurken uyması gereken evrensel mimari kurallardır.

* **Stateless (Durumsuzluk):** Sunucu, gelen isteklerin geçmişini aklında tutmaz (balık hafızalıdır). Bu nedenle her bir istek (request), sunucunun o işlemi gerçekleştirebilmesi için ihtiyaç duyduğu **tüm bilgileri** (kimlik doğrulama token'ı, parametreler vb.) kendi içinde barındırmak zorundadır.
* **Resource Based (Kaynak Odaklılık):** API tasarlanırken eylemlere (fiillere) değil, verilere (isimlere) odaklanılır. Adresler `.../kullanici-getir` veya `.../araba-sil` şeklinde fiillerden oluşamaz. Bunun yerine odak noktamız olan kaynak (isim) çoğul olarak yazılır: `.../users` veya `.../cars`. İşlemin ne olacağını adres değil, HTTP metotları (GET, POST vb.) belirler.

</details>

<details>
  <summary>HTTP Methods ve Endpoint Tasarımı Örnekleri</summary>

RESTful mimaride Endpoint (URL Adresi) sabit kalır, o adrese atılan isteğin "Türü" (HTTP Metodu) yapılarak işlemi değiştirir:

* **`GET /api/users`**
  * **İşlevi:** Sistemdeki tüm kullanıcıların listesini getirir. Veritabanında sadece okuma işlemi yapar.
* **`POST /api/users`**
  * **İşlevi:** Sisteme yepyeni bir kullanıcı ekler. İsteğin gövdesinde (Body) yeni kullanıcının JSON formatındaki bilgileri yer alır.
* **`GET /api/users/1`**
  * **İşlevi:** URL'nin sonuna eklenen parametre sayesinde sadece ID numarası "1" olan o spesifik kullanıcının detaylarını getirir.
* **`PUT /api/users/1`**
  * **İşlevi:** ID numarası 1 olan kullanıcının bilgilerini (Örn: Adresini veya şifresini) tamamen günceller.
* **`DELETE /api/users/1`**
  * **İşlevi:** ID numarası 1 olan kullanıcıyı sistemden siler.

</details>

<details>
  <summary>GraphQL Nedir?</summary>
  
* **Tanım:** Facebook tarafından geliştirilen, REST API'ye güçlü bir alternatif olan veri sorgulama dilidir. 
* **Temel Farkı:** REST mimarisinde sunucunun belirlediği standart paketler (veriler) istemciye gönderilirken; GraphQL'de **kontrol istemcidedir (Frontend)**. İstemci, sunucuya bir "istek listesi" gönderir ve sunucu sadece bu listedeki alanları döndürür.

</details>

<details>
  <summary>GraphQL'in Avantajları</summary>
  
* **İhtiyaç Kadar Veri Çekebilme (No Overfetching / Underfetching):** REST API'de sadece bir kullanıcının ismine ihtiyacınız olsa bile `/users/1` isteği size o kullanıcının tüm şifre, adres ve geçmiş bilgilerini gereksiz yere indirebilir (Overfetching). GraphQL'de ise sadece `"isim"` alanını istersiniz ve sadece o alan gelir. İnternet bant genişliğinden inanılmaz tasarruf sağlar.
* **Tek Endpoint (Single Endpoint):** REST API'de her kaynak için ayrı bir URL adresi (`/users`, `/orders`, `/products`) bulunurken, GraphQL'de sistem ne kadar büyük olursa olsun dışarıya açılan sadece **tek bir kapı** (`/graphql`) vardır. Frontend geliştiricisi elindeki listeyi bu kapıya verir, sistem arka planda gerekli veritabanlarından bilgileri toplayıp tek seferde geri döndürür.

</details>

<details>
  <summary>GraphQL'in Dezavantajları</summary>
  
* **Cache (Önbellekleme) Yönetiminin Karmaşıklığı:** REST mimarisinde HTTP önbellekleme sistemleri URL tabanlı çalışır (Örn: `/users/1` adresi her zaman aynı veriyi döndürdüğü için kolayca hafızaya alınır). Ancak GraphQL'de tüm istekler aynı adrese (`/graphql`) yapıldığı ve her isteğin içeriği (istenen veri kombinasyonu) farklı olduğu için, sonuçları hafızada tutmak (caching) ve yönetmek çok daha zor ve karmaşık bir mühendislik gerektirir.

</details>


<details>
  <summary>SOAP Nedir ve Mantığı Nasıldır?</summary>
  
* **Tanım:** İnternet üzerindeki uygulamaların birbiriyle iletişim kurmasını sağlayan, kuralları son derece katı, yüksek güvenlikli ve eski ama çok sağlam bir protokoldür.
* **Mantığı:** REST mimarisinin esnekliğinin tam zıttıdır. REST günlük hayattaki rahat bir sohbet ise, SOAP resmi bir devlet dairesine verilen ıslak imzalı bir dilekçe gibidir. Her şeyin kuralı, formatı ve güvenlik duvarları önceden kesin bir şekilde belirlenmiştir. Esnekliğe yer yoktur.

</details>

<details>
  <summary>Temel Özellikleri ve Kavramlar</summary>
  
* **XML Tabanlı (Sıkı Format):** REST genellikle hafif olan JSON'u tercih ederken, SOAP sadece XML kullanır. Veriler; Envelope (Zarf), Header (Başlık) ve Body (Gövde) adı verilen standart etiketlerin içine hapsedilerek gönderilir. En ufak bir format hatasında (eksik etiket vb.) işlem tamamen reddedilir.
* **WSDL (Web Services Description Language):** SOAP servisinin dış dünyaya sunduğu, makine tarafından okunabilen "Kullanım Kılavuzu" veya "Sözleşmesi"dir. Servisin hangi işlemleri yapabildiği, parametrelerin veri tipleri (Örn: yaş bilgisinin sadece rakam olabileceği) bu belgede kesin olarak yazar. İstemci (Client) bu WSDL dosyasını okumadan sisteme istek atamaz.

</details>

<details>
  <summary>Neden Kurumsal Sistemlerde Kullanılır?</summary>
  
* **Kullanım Alanları:** Bankacılık sistemleri, E-Devlet uygulamaları, telekomünikasyon ve büyük finansal entegrasyonlar.
* **Neden REST Değil de SOAP?:** SOAP, veri transferinde ekstra karakterler (XML) kullandığı için REST'e göre hantal ve yavaştır. Ancak WS-Security gibi gömülü güvenlik standartlarına ve işlemlerin yarıda kalmasını önleyen çok katı ACID uyumluluğuna sahiptir. Milyon dolarlık EFT işlemlerinde veya resmi devlet evraklarında "hız veya esneklik" değil; "kusursuz güvenlik ve değişmez kurallar" istendiği için devasa kurumların vazgeçilmezidir.

</details>

<details>
  <summary>Büyüklük Karşılaştırma: REST vs GraphQL vs SOAP</summary>

API mimarisi seçerken projenin ihtiyaçlarına göre bu üç teknolojiden biri tercih edilir. Aralarındaki temel farklar şu şekildedir:

| Özellik | REST API | GraphQL | SOAP |
| :--- | :--- | :--- | :--- |
| **Yapı Türü** | Mimari Tarz (Esnek) | Sorgu Dili / Spesifikasyon | Katı Protokol (Standartlar) |
| **Veri Formatı** | JSON, XML, HTML, Metin | Sadece JSON | Sadece XML |
| **Endpoint (Adres)** | Çoklu (Örn: `/users`, `/cars`) | Tek bir kapı (Örn: `/graphql`) | Tek bir kapı (WSDL odaklı) |
| **Veri Kontrolü** | Sunucu belirler (Backend) | İstemci belirler (Frontend) | Sunucu belirler (Katı kurallar) |
| **Hız / Boyut** | Orta (Gereksiz veri gelebilir) | Çok Hızlı (Sadece istenen veri) | Yavaş ve Hantal (Ağır XML yükü) |
| **Güvenlik** | SSL/TLS, Token tabanlı | SSL/TLS, Esnek güvenlik | WS-Security (En yüksek/katı) |

### Özet Analojilerle Farklar:

* **REST:** Bir restoranda standart menü sipariş etmek gibidir. 3 numaralı menüyü istersiniz; içindeki kolayı sevmeseniz bile o kola masanıza mecbur gelir (Overfetching).
* **GraphQL:** Garsona özel sipariş vermektir. *"Bana sadece burgerin köftesini ve marulunu getir, patates ve içecek istemiyorum"* dersiniz. Tam ihtiyacınız olan bayt kadar veri gelir, internet kotasını yormaz.
* **SOAP:** Bankalar arası para taşıyan zırhlı nakliye aracı gibidir. Çok hantaldır, yavaş ilerler, şifreli kilitleri ve katı prosedürleri vardır; ancak içindeki değerli varlığı (veriyi) %100 güvenlik ve sıfır hata payı ile taşır.

### Hangisini Ne Zaman Seçmeli?
1.  **REST:** Standart web projeleri, mobil uygulamalar, herkesin hızlıca entegre olabileceği genel (public) API'ler geliştirilirken sektör standardıdır.
2.  **GraphQL:** Frontend tarafının çok karmaşık olduğu, ekranın farklı yerlerinde sürekli farklı veri kombinasyonlarına ihtiyaç duyulduğu (Örn: Kripto borsası arayüzleri veya sosyal medya akışları) ve bant genişliğinin kritik olduğu durumlaboratuvar ortamlarında tercih edilir.
3.  **SOAP:** Bankacılık sistemleri, e-devlet entegrasyonları ve iki büyük kurumun birbiriyle hatasız, resmi sözleşmelere (WSDL) bağlı olarak veri transferi yapması gereken durumlarda zorunluluktur.

</details>
<details>
  <summary>WebSocket Nedir ve Mantığı Nasıldır?</summary>
  
* **Tanım:** İstemci (Client) ve Sunucu (Server) arasında, tek bir bağlantı üzerinden **çift yönlü (bidirectional)** ve **kesintisiz/eşzamanlı (real-time)** veri aktarımı sağlayan iletişim protokolüdür.
* **REST'ten Farkı:** REST API'de iletişim "Soru-Cevap" şeklindedir. İstemci istek atar, sunucu cevap verir ve kapıyı kapatır. Sunucu durup dururken istemciye veri yollayamaz. WebSocket'te ise iletişim bir "Telefon Görüşmesi" gibidir. Hat bir kez açılır ve bağlantı koparılana kadar açık kalır. İki taraf da birbirine sormadan, istediği an veri gönderebilir.
</details>

<details>
  <summary>WebSocket Kullanım Alanları (Gerçek Hayat Örnekleri)</summary>
  
REST mimarisinin yetersiz kaldığı, saniyelik güncellemelerin hayati olduğu sistemlerde kullanılır:

* **Canlı Borsa ve Kripto Grafikleri:** Binance gibi platformlarda AVAX veya BTC fiyatlarını izlerken sayfayı yenilemenize gerek kalmaz. Fiyatta bir oynama olduğu an sunucu, WebSocket tüneli üzerinden bu veriyi doğrudan ekranınıza iter (push) ve grafikler anında güncellenir.
* **Rekabetçi Çok Oyunculu Oyunlar (Multiplayer):** Rocket League gibi hızın kritik olduğu oyunlarda, topun ve rakip araçların milisaniyelik koordinat değişiklikleri, açık soket bağlantıları üzerinden kesintisiz bir veri akışıyla oyuncuya iletilir. Gecikmesiz (lag-free) oyun deneyiminin temelidir.
* **Canlı Sohbet Uygulamaları:** WhatsApp Web veya Twitch Chat gibi platformlarda, siz bir yere tıklamadan karşıdan gelen mesajın anında ekranınıza düşmesini sağlayan teknoloji yine WebSocket'tir.
</details>

<details>
  <summary>OpenAPI ve Swagger Nedir?</summary>
  
* **OpenAPI:** REST API'lerin hangi endpoint'lere (adreslere) sahip olduğunu, hangi verileri (JSON) kabul edip ne döndüreceğini tanımlayan evrensel bir spesifikasyon (standartlar bütünü) dilidir.
* **Swagger (Swagger UI):** OpenAPI standartlarıyla yazılmış API dokümanlarını alıp, tarayıcı üzerinde çalışan, görsel, renkli ve interaktif bir web sayfasına çeviren araçtır.
* **Mantığı:** WSDL'in modern, okunabilir ve test edilebilir versiyonudur. Geliştiriciler kodlarına ekledikleri ufak notasyonlar sayesinde, API'lerinin "Canlı Kullanım Kılavuzunu" otomatik olarak oluştururlar. Swagger arayüzü üzerinden "Execute" butonuna basılarak harici bir araca (Örn: Postman) ihtiyaç duymadan API doğrudan tarayıcı üzerinden test edilebilir.

</details>

<details>
  <summary>Client Generation (Otomatik Kod Üretimi) Nedir?</summary>
  
* **Tanım:** OpenAPI/Swagger dosyasındaki standart API haritasını kullanarak, Frontend (İstemci) tarafında backend ile iletişim kuracak kodların makine tarafından otomatik olarak yazılması işlemidir.
* **Ne İşe Yarar (Avantajları):** Büyük bir platformun (Örn: Binance) API'sine bağlanmak için HTTP istekleri, Header ayarları ve JSON ayrıştırma (parsing) kodlarını elde yazmak haftalar sürebilir ve hataya açıktır. Client Generation araçları, API şemasını okur ve saniyeler içinde projenize özel hazır metotlar (Örn: `apiClient.getUsers()`) üretir.
* **Özetle:** Backend ile Frontend arasındaki iletişimi sağlayan "Kabloyu ve Adaptörü" geliştiricinin yerine otomatik olarak üreten fabrika gibidir. Büyük bir zaman ve iş gücü tasarrufu sağlar.

</details>

## 14. .NET Ekosistemi

<details>
  <summary>.NET Nedir ve Tarihsel Gelişimi</summary>
  
* **.NET (Genel Tanım):** Microsoft'un geliştirdiği; masaüstü, web, bulut, mobil ve yapay zeka gibi A'dan Z'ye her türlü uygulamanın geliştirilebildiği devasa bir yazılım ekosistemidir.
* **.NET Framework (Klasik Dönem):** Sistemlerin atasıdır (2002-2014). Çok güçlü ve stabil bir altyapısı vardır ancak **sadece Windows** işletim sistemlerinde çalışır. Günümüz modern sunucu mimarilerinde (Linux vb.) hantal kaldığı için artık yeni projelerde tercih edilmemektedir.
* **.NET Core (Evrensel ve Modüler Dönem):** Microsoft'un eski sistemi bırakıp sıfırdan yazdığı; hafif, hızlı ve modüler olan yeni nesil altyapısıdır. En büyük devrimi **Cross-Platform (Çapraz Platform)** olmasıdır; yani Windows, Linux veya macOS fark etmeksizin her yerde kusursuz çalışır.
* **Modern .NET (.NET 5 ve Sonrası):** Sektördeki isim karmaşasını bitirmek için "Framework" ve "Core" isimlerinin atılıp sistemlerin tek bir çatı altında birleştirilmiş halidir. Eski sistemin gücüyle yeni sistemin evrenselliğini (platform bağımsızlığını) tek bir motorda buluşturur.

</details>

<details>
  <summary>Sürüm Stratejisi (LTS vs STS)</summary>

Microsoft'un sürümleri yönetirken kullandığı "Tek - Çift Yıl" kuralıdır:

* **LTS (Long Term Support - Çift Numaralar):** Uzun süreli destek versiyonlarıdır (.NET 6, 8, 10). 3 yıl boyunca yama ve güvenlik garantisi sunar. Kurumsal firmalar, bankalar ve büyük projeler sistemlerini riske atmamak için daima LTS sürümlerini kullanır. (Kur-unut mantığı).
* **STS (Standard Term Support - Tek Numaralar):** Standart süreli destek versiyonlarıdır (.NET 7, 9). Sadece 18 ay desteklenir. Yeni teknolojilerin, performans iyileştirmelerinin ve yapay zeka entegrasyonlarının agresif şekilde test edildiği "geçiş/inovasyon" sürümleridir.

</details>

<details>
  <summary>Güncel .NET Sürümleri (8, 9 ve 10)</summary>
  
* **.NET 8 (LTS):** 2023 sonunda çıkan, bulut (cloud-native) mimarileri ve hız konusunda ciddi temellerin atıldığı, son derece stabil çalışan uzun süreli ana sürümdür.
* **.NET 9 (STS):** 2024 sonunda çıkan geçiş sürümüdür. .NET 8'in üzerine özellikle Yapay Zeka (AI) entegrasyonlarını kolaylaştıran, bulut sistemlerinde daha az bellek (RAM) tüketen, performans odaklı kısa ömürlü bir versiyondur.
* **.NET 10 (LTS):** 2025 sonunda yayınlanan, en güncel zirve noktasıdır. .NET 9'daki tüm agresif yapay zeka ve performans iyileştirmelerini bünyesine alıp, 3 yıllık uzun süreli güvenlik garantisiyle paketleyen; kurumsal şirketlerin aktif olarak geçiş yaptığı tam donanımlı ana sürümdür.

</details>

<details>
  <summary>Eski .NET (Framework) ile Yeni .NET (Core/Modern) Arasındaki Temel Farklar</summary>
  
* **Windows Bağımlılığı ve Platform Desteği:** * Eski sistem (.NET Framework) doğrudan Windows işletim sisteminin çekirdeğine bağımlıydı. Bir Linux veya macOS sunucusunda çalıştırılamazdı. 
  * Yeni nesil .NET ise **Cross-Platform (Çapraz Platform)** mimarisine sahiptir. Aynı kod hiçbir değişikliğe uğramadan Windows, Linux ve macOS üzerinde kusursuz bir şekilde çalışır. Bu özellik, şirketleri pahalı Windows lisanslarından kurtarmıştır.
* **Açık Kaynak (Open Source) Yaklaşımı:** * Eski sistem tamamen kapalı kapılar ardında (Closed Source) Microsoft tarafından geliştirilirdi. 
  * Yeni sistem %100 açık kaynaklıdır (GitHub üzerinde). Dünyanın dört bir yanındaki bağımsız geliştiriciler ve rakip teknoloji devleri (Google, AWS vb.) bile .NET'in kodlarına katkıda bulunabilir, hataları anında çözebilir. Bu, sistemin gelişim hızını muazzam artırmıştır.
* **Performans ve Modülerlik:** * Eski sistem (Monolitik) hantaldı; küçük bir proje yapsanız bile tüm devasa kütüphaneleri sisteme dahil ederdi, çok RAM tüketirdi. 
  * Yeni sistem (Modüler) ise bir "Lego" gibidir. Çekirdek çok küçüktür ve geliştirici sadece projesinde kullanacağı özellikleri sisteme dahil eder (Örn: Sadece veritabanı kütüphanesini ekler). Bu hafiflik sayesinde inanılmaz hızlıdır, saniyeler içinde başlar ve bulut (cloud) sistemlerinde minimum maliyet/kaynak tüketimi sağlar.

</details>

<details>
  <summary>.NET'in Mimari Bileşenleri: CLR ve Runtime</summary>
  
* **Runtime (Çalışma Zamanı):** Yazılan kodun bilgisayar üzerinde canlı olarak çalıştırılması, belleğin (RAM) yönetilmesi ve hataların denetlenmesi işlemlerini üstlenen çalışma ortamıdır.
* **CLR (Common Language Runtime):** .NET platformunun kalbidir (Motor beyni/Tercümanı). C# gibi dillerde yazılan insan okumasına yakın kodları, program çalıştığı anda (Just-In-Time) o an üzerinde bulunduğu işletim sisteminin anlayacağı makine koduna (0 ve 1'lere) çeviren çekirdek yapıdır.

</details>

<details>
  <summary>Kestrel Web Sunucusu Nedir?</summary>
  
* **Tanım:** Modern .NET (ASP.NET Core) projelerinin içinde varsayılan olarak gelen, açık kaynaklı, Cross-Platform (her işletim sisteminde çalışan) web sunucusudur.
* **Ne İşe Yarar?:** Uygulamaya dış dünyadan gelen web isteklerini (HTTP Requests) kapıda karşılayan ve yanıtları (Responses) geri gönderen sistemdir. Çok hafif olduğu için saniyede yüz binlerce isteği işleyebilecek kadar yüksek bir hıza (throughput) sahiptir.

</details>

<details>
  <summary>Linux ve Docker Desteğinin Önemi</summary>

* **Linux Desteği:** Yeni nesil CLR'ın yetenekleri sayesinde .NET projeleri artık Windows sunuculara mahkum değildir. Aynı kod hiçbir değişikliğe uğramadan Linux sunucularda da çalışır. Bu da kurumsal şirketlere sunucu lisanslama (hosting) konusunda milyonlarca dolarlık tasarruf sağlar.
* **Docker Entegrasyonu:** Modern .NET; çok hafif, modüler ve Linux tabanlı olabilmesi sayesinde Docker konteyner (Container) mimarisine kusursuz uyum sağlar. Geliştirilen bir API, tek bir komutla minimal bir Linux/Docker imajı içine paketlenip bulut (Cloud/Kubernetes) sistemlerinde saniyeler içinde binlerce kopyaya çıkarılabilir (ölçeklenebilir).

</details>

<details>
  <summary>Managed Code (Yönetilen Kod) vs Unmanaged Code</summary>
  
* **Managed Code:** C# gibi .NET dilleriyle yazılan ve doğrudan **CLR'ın (Common Language Runtime)** koruması, denetimi ve kuralları altında çalışan kod türüdür. Bellek yönetimi ve güvenlik CLR tarafından otomatik olarak sağlanır. (Örn: Tüm elektronik güvenlik asistanlarına sahip yeni nesil akıllı bir araç kullanmak gibidir; sistem hata yapmanızı engeller).
* **Unmanaged Code:** C veya C++ gibi dillerle yazılan, CLR'ın dışında doğrudan işletim sistemi üzerinde çalışan koddur. Çok yüksek hız ve donanım kontrolü sağlar ancak tüm bellek yönetimi ve güvenlik sorumluluğu tamamen geliştiricinin omuzlarındadır. (Örn: Hiçbir güvenlik asistanı olmayan eski tip bir yarış arabasıdır; kontrol tamamen sizdedir ancak hata affetmez).

</details>

<details>
  <summary>Memory Management (Bellek Yönetimi) ve Garbage Collector</summary>
  
* **Bellek Sorunu (Memory Leak):** Uygulamalar çalışırken sürekli RAM'de veri (nesne) oluştururlar. İşlemi biten veriler RAM'den silinmezse hafıza dolar ve sistem çöker. Unmanaged dillerde bu silme işlemini kod ile manuel yapmak zorunludur.
* **Garbage Collector (Çöp Toplayıcı):** .NET CLR'ın içinde yer alan otomatik bellek temizleme mekanizmasıdır. Arka planda sürekli çalışarak RAM'i tarar ve program tarafından artık kullanılmayan/referansı kalmayan nesneleri tespit edip bellekten otomatik olarak siler.
* **Mantığı:** Restorandaki komi (temizlik görevlisi) gibidir. Geliştirici tıpkı bir müşteri gibi sadece işine odaklanır, masadan (kapsamdan) ayrıldığında arka plandaki komi (Garbage Collector) gelip o boşalan verileri RAM'den silerek sistemi her zaman ferah ve çalışır durumda tutar.

</details>

<details>
  <summary>NuGet Nedir? (Paket Yönetimi)</summary>
  
* **Tanım:** .NET ekosisteminin resmi paket yönetim sistemidir. Tıpkı telefonlardaki App Store veya Google Play Store gibi geliştiriciler için bir "Hazır Kod / Kütüphane Mağazası"dır.
* **Mantığı:** Yazılımcılar tekerleği yeniden icat etmemek için, başkalarının yazdığı (örneğin PDF oluşturma, veritabanına bağlanma veya ödeme alma) hazır kod bloklarını kendi projelerine NuGet üzerinden saniyeler içinde dahil ederler. Dışa bağımlılıkların (dependencies) tüm versiyon kontrolleri ve güncellemeleri tek bir merkezden yönetilir.

</details>

<details>
  <summary>Paket Yayınlama (Publishing)</summary>
  
* **Mantığı:** NuGet sadece dışarıdan paket indirme (consume) yeri değildir. Geliştiriciler, kendi yazdıkları başarılı ve tekrar kullanılabilir kod kütüphanelerini `.nupkg` formatında paketleyip `nuget.org` üzerinde yayınlayabilirler. Böylece bu paketler, şirket içindeki diğer takımlar veya tüm dünyadaki açık kaynak (open-source) toplulukları tarafından projelere dahil edilebilir.

</details>

<details>
  <summary>Versiyonlama Mantığı (Semantic Versioning - SemVer)</summary>

Yayınlanan paketlerin güncellemelerini takip etmek için **Major.Minor.Patch (Örn: 1.4.2)** kuralı kullanılır:

* **Patch (Yama - x.x.2):** Sadece mevcut hataların (bug) düzeltildiği güncellemelerdir. Eski kodları asla bozmaz, güvenle yükseltilebilir.
* **Minor (Küçük Özellik - x.4.x):** Sisteme yepyeni özelliklerin eklendiği ancak eski sistemin işleyişini ve fonksiyonlarını bozmayan (geriye dönük uyumlu) güncellemelerdir.
* **Major (Büyük ve Kırıcı Değişim - 1.x.x):** Mimarinin tamamen değiştiği, "Kırıcı Değişiklikler" (Breaking Changes) içeren güncellemelerdir. Bu güncelleme alındığında geliştiricinin kendi projesindeki kodları da yeni mimariye göre değiştirmesi (refactor) gerekir.

</details>

## 15. ASP.NET Core 

<details>
  <summary>ASP.NET Core Nedir?</summary>
  
* **Tanım:** .NET ekosistemi üzerinde çalışan; modern web uygulamaları, e-ticaret siteleri, mikro servisler ve REST API'ler geliştirmek için kullanılan açık kaynaklı bir web framework'üdür (çatısıdır).
* **Mantığı:** .NET bir temel motor ise, ASP.NET Core o motorun üzerine inşa edilen, dış dünyadan (internet tarayıcılarından, mobil cihazlardan) gelen HTTP isteklerini karşılayıp cevaplayan aerodinamik bir kasadır.

</details>

<details>
  <summary>Temel Avantajları</summary>
  
* **Yüksek Performans:** Eski monolitik sistemlerin aksine modülerdir (sadece ihtiyacınız olan paketleri yüklersiniz). İçine gömülü gelen **Kestrel** web sunucusu sayesinde son derece az RAM tüketir ve dünyadaki en yüksek tepki/istek hızlarına sahip framework'lerden biridir.
* **Cross-Platform (Çapraz Platform):** Geliştirilen bir web projesi Windows'a bağımlı değildir. Hiçbir kod değişikliği yapmadan macOS üzerinde geliştirilip, Linux sunucularda veya Docker konteynerleri içinde kusursuzca (ve lisans masrafı olmadan) çalıştırılabilir.
* **Açık Kaynak (Open Source):** Tüm kaynak kodları GitHub üzerinde barındırılır. Dünyanın dört bir yanındaki binlerce geliştiricinin (ve Microsoft dışı teknoloji devlerinin) ortak katkısıyla sürekli olarak güncellenir, hatalardan arındırılır ve modern kalır.

</details>

<details>
  <summary>MVC (Model-View-Controller) Mimari Deseni</summary>
  
* **Tanım:** Karmaşık yazılım projelerinde "karmaşayı önlemek" ve kodun bakımını kolaylaştırmak için projeyi üç bağımsız ana katmana bölen yazılım mimarisi şablonudur.
* **Mantığı:** Tasarım (HTML/CSS), veri işleme kuralları ve yönlendirme işlemleri birbirine karıştırılmaz. Her katman (klasör) sadece kendi sorumluluğunu yerine getirir. (Seperation of Concerns - Sorumlulukların Ayrılığı prensibi).

</details>

<details>
  <summary>MVC Katmanları ve Görevleri</summary>

* **Model (Veri ve İş Mantığı):** Uygulamanın beynidir. Veritabanı işlemleri (veriyi çekme, kaydetme) ve iş kuralları (hesaplamalar, doğrulamalar) burada yapılır. Görsel kısımla (ekranla) hiçbir ilgisi yoktur. *(Örn: Restoranın yemeği pişiren ve malzemeleri saklayan mutfağıdır).*
* **View (Görünüm / Kullanıcı Arayüzü):** Kullanıcının cihazında veya tarayıcısında gördüğü ekranlardır (HTML, CSS, butonlar vb.). Arka plandaki kodlardan habersizdir, sadece kendisine verilen veriyi son kullanıcıya şık bir şekilde sunmakla görevlidir. *(Örn: Restoranın şık masaları ve yemeğin görsel sunumudur).*
* **Controller (Yönlendirici / Köprü):** Gelen istekleri karşılayan orkestra şefidir. View ile Model asla birbirleriyle doğrudan konuşmaz. Controller, kullanıcıdan gelen isteği (tıklamayı) View'dan alır, işlenmesi için Model'e gönderir. Modelden gelen sonucu da alıp uygun bir View'a (ekrana) yansıtarak süreci tamamlar. *(Örn: Müşteriden siparişi alıp mutfağa ileten ve pişen yemeği masaya geri getiren garson).*

</details>

<details>
  <summary>Middleware ve Middleware Pipeline Nedir?</summary>
  
* **Middleware (Ara Yazılım):** Uygulamaya dışarıdan gelen HTTP isteklerini (Request) karşılayan, üzerinde belirli kontroller veya işlemler yapan ve gerekirse isteği reddedip cevabı (Response) geri döndüren küçük, bağımsız kod bloklarıdır. (Örn: Havalimanındaki bir X-Ray cihazı veya pasaport kontrol noktası).
* **Middleware Pipeline (İşlem Boru Hattı):** Birden fazla Middleware'in belirli bir sırayla arka arkaya dizildiği zincirdir. Dışarıdan gelen istek, hedefine (Controller'a) ulaşmadan önce bu koridordaki her bir kontrol noktasından sırayla geçmek zorundadır.

</details>

<details>
  <summary>Sık Kullanılan Middleware Örnekleri</summary>

* **Logging (Kayıt Tutma):** Sisteme gelen tüm isteklerin, hataların ve sürelerin arka planda bir dosyaya veya veritabanına kaydedilmesini sağlar. *(Havalimanı girişindeki her şeyi sessizce kaydeden güvenlik kamerasıdır).*
* **Authentication (Kimlik Doğrulama):** İsteği yapan kişinin iddia ettiği kişi olup olmadığını denetler (Kullanıcı Adı/Şifre veya Token kontrolü). *(Polisin "Sen kimsin?" diyerek pasaportunuzu kontrol etmesidir).*
* **Authorization (Yetkilendirme):** Kimliği doğrulanmış kişinin, ulaşmaya çalıştığı adrese yetkisinin (Role/Permission) olup olmadığını kontrol eder. *(VIP salonu görevlisinin, biletinizin o salona girmeye yetip yetmediğini kontrol etmesidir).*
* **Exception Handling (Hata Yönetimi):** Uygulamanın herhangi bir yerinde sistem çökerse veya hata fırlatılırsa, kullanıcının ekranına karmaşık kod hatalarının yansımasını engelleyen ve süreci şık bir "Sistemde geçici bir hata oluştu" mesajıyla toparlayan kurtarıcı katmandır. *(Havalimanındaki bir kriz anında, paniği önleyip süreci profesyonelce yöneten acil müdahale ekibi).*

</details>

<details>
  <summary>Dependency Injection (Bağımlılık Enjeksiyonu) Nedir?</summary>
  
* **Tanım:** Bir sınıfın (class) çalışması için ihtiyaç duyduğu diğer nesneleri (bağımlılıkları) kendi içinde `new` anahtar kelimesiyle sıfırdan üretmek yerine; bu nesnelerin dışarıdan merkezi bir sistem (IoC Container) tarafından o sınıfa hazır olarak verilmesi (enjekte edilmesi) prensibidir.
* **Mantığı ve Avantajı:** Bir aşçının kendi tavasını dökümhanede üretmesi yerine (bağımlılık yaratmak), sadece "Bana tava lazım" diyerek restoran yönetiminden (DI Container) hazır tava talep etmesidir. Bu sayede kodlar birbirinden bağımsız (Loosely Coupled) hale gelir, test edilebilirliği inanılmaz ölçüde artar ve sistemdeki karmaşa son bulur.

</details>

<details>
  <summary>Service Lifetimes (Yaşam Döngüleri): Transient, Scoped, Singleton</summary>

Dependency Injection sistemine kaydedilen nesnelerin hafızada (RAM) ne kadar süre tutulacağını ve ne sıklıkla yenileneceğini belirleyen 3 temel yaşam döngüsü vardır:

* **Transient (Kullan-At):** Nesne (servis) kim tarafından ne zaman talep edilirse edilsin, **her defasında sıfırdan yepyeni** bir kopya oluşturulur. İşlem bitince hemen silinir. *(Örn: Her isteyene yepyeni verilen kağıt peçete).*
* **Scoped (İstek Başına):** Gelen her bir HTTP İsteği (Request) için sadece bir tane kopya oluşturulur. O istek (request) uygulamanın içinde dolaştığı sürece herkes aynı kopyayı kullanır. İstek sonlanınca silinir. Web projelerinde veritabanı (DbContext) bağlantıları için standart yöntemdir. *(Örn: Bir müşteri masasına açılan adisyon fişidir. Müşteri kalkana kadar tüm garsonlar o masanın aynı fişine işlem yapar).*
* **Singleton (Tek Ortak Kopya):** Uygulama sunucuda ilk başladığı anda nesne 1 kez oluşturulur. Sunucu kapanana kadar gelen tüm kullanıcılara ve tüm HTTP isteklerine **aynı kopya** (aynı RAM adresi) verilir. *(Örn: Restorandaki ortak çay kazanıdır. Gün boyunca herkes aynı kazanı paylaşır).*

</details>