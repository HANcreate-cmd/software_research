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