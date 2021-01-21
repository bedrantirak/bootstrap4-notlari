# :rocket: Bootstrap 4 :b: 



[![Build Status](https://travis-ci.org/joemccann/dillinger.svg?branch=master)](https://www.linkedin.com/in/bedran-t%C4%B1rak-1a4bb9146/)

#### :round_pushpin: Bootstrap nedir ve nasıl kullanılır? Bootstrap 4 ile modern responsive web siteleri nasıl yapılır?

  - Bootstrap 4 Front-End Geliştiricilerin kullandığı ücretsiz ve son derece popüler bir Css ve Javascript kütüphanesidir.
  - Bootstrap sayesinde masaüstü, tablet, mobil cihaz ve tüm tarayıcılara uyumlu web web sitelerini kolaylıkla geliştirebiliriz. Üstelik ayrı tasarımlar yapmamıza gerek kalmıyor.
  - Bootstrap içerisinde kullanabileceğimiz bir sürü hazır css class' ları vardır. Bu class' lar sayesinde rutin işlerimiz için sürekli css kodları yazmamız gerekmiyor tek yapmamız gereken bootstrap içerisindeki hazır css class ismini bilmemiz ve ilgili etikete eklememizdir.
  - Bootstrap' in [resmi web sitesini](https://getbootstrap.com/docs/4.0/getting-started/introduction/)  ziyaret edip kullanımlara göz atmanızı tavsiye ederim.
  ####  Örneğin;
```sh
  <div class="container  mt-3">
     <div class="alert  alert-primary">
         Alert Primary
            </div>
    </div>
```
[Demo](https://codepen.io/bedrantirak/pen/eYdEwjp)

##### .container :
- Bu class sayesinde sağdan ve soldan boşluk bırakılır. Normalde bu işlemi margin: 0 auto; ile yapabilirdik ancak bu kullanım işlerimizi gayet basitleştirdi.
##### .mt-3 : 
- Bu class sayesinde margin-top ile <div> içeriğini yukarıdan aşağıya almış oluyoruz.
##### .alert  .alert-primary :
- Classları sayesinde güzel görünümlü bir uyarı kutusu oluşturmuş oluyoruz.
  
#### :round_pushpin: Bootstrap 4 kütüphanesini nasıl kullanırım? Bootstrap css ve javascript dosyalarını sayfama nasıl ekleyebilirim? 

- Bootstrap 4 kütüphanesini [mobile cihazları(mobile-first)]() hedef alan [responsive]() bir yapıya sahiptir.
- Responsive tasarımın etkin olabilmesi için aşağıdaki responsive meta etiketini "head" kısmına eklememiz gerekiyor.
```sh
  <meta name="viewport" content="width=device-width, initial-scale=1">
```
- [width = device-width]() özelliği cihazın ekran genişliğini algılayıp sayfanın genişliğini bu değere eşitlemesi ile alakalıdır.
- [initial-scale = 1]() ise sayfa ölçeklendirmesini (zoom) ayarlar.
- Bootstrap Kurulumu için ilk olarak bootstrap css ve javascript dosyalarını sayfamıza eklememiz gerekiyor.
- Bootstrap "css class" larını kullanabilmek için ["bootstrap.min.css"]() dosyasının "cdn" adresini html sayfamızın "head" kısmına eklememiz gerekiyor.

```sh
<link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.1.3/css/bootstrap.min.css">
```
- ["Bootstrap Javascript Component"]() leri kullanabilmek için ise aşağıdaki javascript kütüphanelerini "/body" kapanış etiketinin hemen üstüne eklememiz gerekiyor.

```sh
<script src="https://code.jquery.com/jquery-3.3.1.min.js"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/popper.js/1.14.3/umd/popper.min.js"></script>
<script src="https://stackpath.bootstrapcdn.com/bootstrap/4.1.3/js/bootstrap.min.js"></script>
```
- Bootstrap css class' ları va javascript component' lerini kullanabileceğimiz bir html iskeletini aşağıda olduğu gibi alıp kullanabilirsiniz ek bir ayarlama yapmanıza gerek yoktur.

```sh
 <!doctype html>
<html lang="en">
  <head>
    <!-- Required meta tags -->
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1, shrink-to-fit=no">

    <!-- Bootstrap CSS -->
    <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.1.3/css/bootstrap.min.css">

    <title></title>
  </head>
  <body>
    <h1>Hello, world!</h1>

   
    <script src="https://code.jquery.com/jquery-3.3.1.min.js"></script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/popper.js/1.14.3/umd/popper.min.js"></script>
    <script src="https://stackpath.bootstrapcdn.com/bootstrap/4.1.3/js/bootstrap.min.js"></script>
  </body>
</html>
```
#### :round_pushpin: Bootstrap 4 Grid Sistem nedir ve nasıl kullanılır ?
- Bootstrap 4 ile içeriklerimizi ".container" ya da ".container-fluid" sınıfları içine almamız gerekiyor.

[![Container Status](https://sadikturan.com/img/course/boostrap4-container.jpg)]()

- ".container" ile responsive olarak yani tarayıcı genişliğine göre ".container" class' ı sayfamızın alacağı sabit genişliği belirler.
```sh
<div class="container">
</div>
```
- ".container-fluid" ile tarayıcının genişliğini hesaba katmadan tam ekran genişliğinde bir sayfamız olur.
```sh
<div class="container-fluid">
</div>
```
##### Bootstrap 4 Grid sistemi ile;
- Her satır ".row" class' ı
- Her kolon ".col-* " sınıfı ile belirlenir.
- Her ".row" yani her satır için içerisinde toplam "12 kolon" bulunmaktadır. Toplamda 12 kolonu farklı oranlarda birleştirip kullanabiliriz.

[![Gris Sistem](https://sadikturan.com/img/course/boostrap4-grid-sistem.jpg)]()

- Aşağıdaki örneklerden "herbir satırı" sırasıyla "3,2,4" eşit parçaya bölmüş oluruz.
```sh
<div class="row">
  <div class="col"></div>
  <div class="col"></div>
  <div class="col"></div>
</div>

<div class="row">
  <div class="col"></div>
  <div class="col"></div> 
</div>

<div class="row">
  <div class="col"></div>
  <div class="col"></div> 
  <div class="col"></div>
  <div class="col"></div>
</div>
```
[Demo](https://codepen.io/bedrantirak/pen/LYRzPWw)

- Örnekte herhangi bir bootstrap responsive ön eki (.sm, md, lg, xl) kullanıldığından dolayı ".col" class' ı ile satırlar tarayıcının her genişliğinde yan yana olacaktır.

- Grid sistemin en büyük avantajı responsive bir yapıya sahip olmasıdır yani tarayıcı genişliğine göre her bir kolonu yan yana ya da alt alta alabiliriz.

- @media query' ler ile tarayıcının o anki genişliğini alabiliyoruz ve aldığımğz bu değerlere göre "div" etiketlerini yani bootstrap açısından baktığımızda oluşturduğumuz her kolonun yan yana ya da alt alta alabiliriz.

- Eğer ki satırda yer varsa yan yana, satırda yer kalmadıysa alt satıra alabiliyoruz ki; masaüstü bilgisayarda açılan bir sitenin görünümü yatayda yer kaplarken, mobile bir cihazda açılan site tasarımındaki her kolonun alt alta gelmesi daha iyi bir görünüm sağlayacaktır.

- Bootstrap 4 aşağıdaki media query değerlerini kullanmaktadır.

```sh
// Small devices (landscape phones, 576px ve yukarısı)
@media (min-width: 576px) { ... }

// Medium devices (tablets, 768px ve yukarısı)
@media (min-width: 768px) { ... }

// Large devices (desktops, 992px ve yukarısı)
@media (min-width: 992px) { ... }

// Extra large devices (large desktops, 1200px ve yukarısı)
@media (min-width: 1200px) { ... }
```
Yani tarayıcı genişliği;

- 576px ve aşağısında mı? (.xs)(!! .xs class' ı bootstrap 4'de kullanılmamaktadır.)
 
- minimum 576px ve 768px aralığında mı? (.sm)

- minimum 768px ve 992px aralığında mı? (md)

- minimum 992px ve 1200px aralığında mı? (lg)

- ya da 1200px ve üstünde mi?(xl)

> Media query kullanarak sayısal değerlerle 
> uğraşmak yerine bootstrap 4 ile belirlenen
> ve her bir sayısal değere karşılık gelen class
> isimlerini kullanmak çok daha kolaydır. Bu class
> isimleri; ".xs(extra small)",".sm(small)",
> ".md(medium)",".lg(large)",".xl(extra large)"
> class' larıdır.

```sh
<div class="row">
  <div class="col-sm-3">.col-sm-3</div>
  <div class="col-sm-3">.col-sm-3</div>
  <div class="col-sm-3">.col-sm-3</div>
  <div class="col-sm-3">.col-sm-3</div>
</div>
```
[Demo](https://codepen.io/bedrantirak/pen/KKgXPYx)

- ".col-sm-3" class' ı ile 12 kolonluk satırı 4 eşit parçaya bölmüş oluruz. Ancak ".sm " class' ı eklediğimizden dolayı small cihazların altındaki çözünürlükte (576px) kolonlar alt alta gelecektir.

- Örnekte tarayıcının genişliğini azaltıp 575px' de her bir div' in alt alta geldiğini görebilirsiniz.

```sh
<div class="row">
   <div class="col-md-3">.col-md-3</div>
   <div class="col-md-9">.col-md-6</div>  
</div>
```
[Demo](https://codepen.io/bedrantirak/pen/xxEXxxG)

- ".col-md-3" ve ".col-md-9" sınıflarıyla ikiye böldüğümüz satır medium cihaz yani 768px' in altına indiği anda kolonlar alt alta gelecektir.

#### :round_pushpin: Bootstrap Typography nedir ve nasıl kullanılır? Bootstrap Text etiketlerini nasıl kullanırız? Text Truncate nedir?

- Bootstrap 4 varsayılan olarak 16px font-size (1rem), 24px line-height (1.5rem) , "Helvetica Neue", Helvetica, Arial, sans-serif font-family değerlerini kullanıyor. Ayrıca "p" etiketleri için "margin-top:0;" ve "margin-bottom:1rem (16px)" değerlerini kullanmaktadır. 

- Yani ek ayarlama yapmadan "bootstrap.min.css" dosyasını eklediğiniz her sayfada bu değerler etkin olacaktır.

-   "rem" değeri html' de 16px' lik değeri kullanır.

##### :point_right: Bootstrap 4 Başlık Etiketleri (Headings)
- h1,h2,h3,h4,h5,h6 
```sh
  <h1>h1. Bootstrap heading</h1>
  <h2>h2. Bootstrap heading</h2>
  <h3>h3. Bootstrap heading</h3>
  <h4>h4. Bootstrap heading</h4>
  <h5>h5. Bootstrap heading</h5>
  <h6>h6. Bootstrap heading</h6>
```
[Demo](https://codepen.io/bedrantirak/pen/PoGJqwZ)

- h1 => 2.5rem  (40px)
- h2 => 2rem    (32px)
- h3 => 1.75rem (28px)
- h4 => 1.5rem  (24px)
- h5 => 1.25rem (20px)
- h6 => 1rem    (16px)

- Bazen başlıkların yanında daha soluk bir yazı içeriği yani bir alt başlık oluşturmak isteyebiliriz.
```sh
<h3>
  Web Geliştirme
  <small class="text-muted">Html Css ve Javascript</small>
</h3>
```
[Demo](https://codepen.io/bedrantirak/pen/JjRrdow)

- ".text-muted" class' ı daha soluk bir renk kodu uygular.

- "!important" buradaki css kodunun mutlaka etkin olması yani başka bir color' ın bu css değerini ezmemesini garanti eder.
```sh
.text-muted {
    color: #6c757d!important;
}
```
- "small" etiketi için %80' lik bir font-size uygulanır. Yani o anda "small" etiketi hangi etiket içindeyse o etikete uygulanan font-size değerinin %80' ini kullanmış olur. Yani "small" etiketinin "h1" etiketi içinde olmasıyla "h4" etiketinin içinde olması arasında farklılık vardır.

- Ayrıca "small" etiketi yerine ".small" class' ınıda kullanabilirsiniz.
```sh
.small, small {
    font-size: 80%;
    font-weight: 400;
}
```
##### :point_right: Bootstrap 4 Display Heading

- Bootstrap 4 ile gelen display class' ları headings etiketlerinden farklı olarak daha ince bir font kalınlığı ile daha büyük font büyüklüğü kullanmamıza imkan tanır.

```sh
<h1 class="display-1">Display 1</h1>
<h1 class="display-2">Display 2</h1>
<h1 class="display-3">Display 3</h1>
<h1 class="display-4">Display 4</h1>
```
[Demo](https://codepen.io/bedrantirak/pen/MWjEwKQ)

- Tüm "bootstrap display" sınıflarının "h1" etiketine class şeklinde uygulandığına dikkat ediniz. Bu class' ları sadece "h" etiketleri için kullanmak zorunda da değiliz.

##### :point_right: Bootstrap 4 Text Elements

##### "mark";

- Bootstrap 4 "mark" etiketi içine alınan yazıya sarı bir arka zemin rengi ekleyerek yazıya dikkat edilmesi gerektiğini belirtiyor.

```sh
<p> Use the mark element to <mark>highlight</mark> text.</p>
```
[Demo](https://codepen.io/bedrantirak/pen/bGwooaR)

##### "blockquotes";

- Blockquotes etiketini bir paragraf içinde bir kısma daha dikkat çekmek için kullanırız. Örneğin makaleyi yazan kişi bir özet bilgi paylaşmak istediğinde "blockquotes" etiketi içine alabiliriz.

```sh
<div class="container">
   <p>
    Lorem ipsum dolor sit amet, consectetur adipisicing elit. Optio quos rem, ipsam praesentium est temporibus sint, minus quia quidem autem ea? Amet atque minus fugiat, sed necessitatibus voluptas beatae architecto?
  </p>
<blockquote class="blockquote">
  <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer posuere erat a ante.</p>
  <footer class="blockquote-footer">Someone famous in <cite title="Source Title">Source Title</cite></footer>
</blockquote>
<p>
    Lorem ipsum dolor sit amet, consectetur adipisicing elit. Optio quos rem, ipsam praesentium est temporibus sint, minus quia quidem autem ea? Amet atque minus fugiat, sed necessitatibus voluptas beatae architecto?
  </p>
</div>
```

[Demo](https://codepen.io/bedrantirak/pen/RwGLLBa)

##### Lists;

- ul, li

```sh
<ul class="list-unstyled">
  <li>Lorem ipsum dolor sit amet</li>  
  <li>Nulla volutpat aliquam velit
    <ul>
      <li>Phasellus iaculis neque</li>
      <li>Purus sodales ultricies</li>    
    </ul>
  </li>
  <li>Faucibus porta lacus fringilla vel</li>
  <li>Aenean sit amet erat nunc</li> 
</ul>
```

[Demo](https://codepen.io/bedrantirak/pen/qBaPPJW)

- "ul" etiketine uygulayacağımız ".list-unstyled" class' ı ile "padding-left:0, list-style:none, margin-top:0 ve margin-bottom:1rem (16px)" özelliklerini uygulayarak "ul" etiketi için kullandığımız rutin işleri bootstrap bizim adımıza yapmış olur.
  
##### Inline List Elements;

- Listelere uygulayacağımız bootstrap ".list-inline ve .list-inline-item" class' ları ile liste elemanlarımıza uygulanan varsayılan liste eleman tipini "list-style-type:none" yapar ayrıca liste elemanlarını yan yana almış oluruz.

```sh
<div class="container">
  
  <ul class="list-inline">
    <li class="list-inline-item">Lorem ipsum</li>
    <li class="list-inline-item">Phasellus iaculis</li>
    <li class="list-inline-item">Nulla volutpat</li>
  </ul>
</div>
```
[Demo](https://codepen.io/bedrantirak/pen/rNMGGRR)

- Her bir liste elemanının "display: inline-block;" olarak değiştirildiğine dikkat ediniz.

##### :point_right: Bootstrap 4 Text Transform Elements

- "text-lowercase"; karakterleri küçük harfe çevirir.

- "text-uppercase"; karakterleri büyük harfe çevirir.

- "text-lowercase"; tüm kelimelerin ilk harfini büyük harfe çevirir.

```sh
 <p class="text-uppercase"> Lorem ipsum dolor sit amet, consectetur </p>
 <p class="text-lowercase"> Lorem ipsum dolor sit amet, consectetur </p>
 <p class="text-capitalize">Lorem ipsum dolor sit amet, consectetur </p>
```

[Demo](https://codepen.io/bedrantirak/pen/jOMGGjK)

- bootstrap ".text-truncate" class' ı ile yazının sığmadığı yerlerde yazının sonuna "..." eklenmesini sağlayabilirsiniz.

```sh
<p style="width:150px;" class="text-truncate"> Lorem ipsum dolor sit amet, consectetur </p>    
 <p style="width:200px;" class="text-truncate"> Lorem ipsum dolor sit amet, consectetur </p>  
 <p style="width:500px;" class="text-truncate"> Lorem ipsum dolor sit amet, consectetur </p> 
```

[Demo](https://codepen.io/bedrantirak/pen/VwKMrZj)

#### :round_pushpin: Bootstrap 4 ile text hizalama işlemleri nasıl yapılır? Bootstrap text-align class' ları nedir ve nasıl kullanılır?

- Bootstrap 4 ile gelen "text-align" ve "display" kavramları için kullanabileceğimiz bazı bootstrap class' ları mevcuttur.

##### :point_right: Bootstrap 4' de Text Hizalama nasıl yapılır?

Bootsrap 4' de kullanabileceğimiz "text-align" özelliğinin alabileceği değerler;

- "text-justify" => block etiketi içindeki yazıları "iki yana" hizalar.

- "text-right" => block etiketi içindeki yazıları "sağa" hizalar.

- "text-left" => block etiketi içendeki yazıları "sola" hizalar.

```sh
<p class="text-justify">
   Lorem ipsum dolor sit amet, consectetur adipisicing elit.   
 </p>
  
 <p class="text-right">
   Lorem ipsum dolor sit amet, consectetur adipisicing elit. 
 </p>
  
 <p class="text-left">
   Lorem ipsum dolor sit amet, consectetur adipisicing elit. 
 </p>
```

[Demo](https://codepen.io/bedrantirak/pen/GRjMLLb)

##### :point_right: Bootstrap 4' de Display nasıl kullanılır?

Css display özelliği ile yazdığımız css kodlarını bootstrap 4 ile gelen hazır display class' ları ile çok daha kolay bir şekilde kullanabiliriz.

- Bir etiketi block bir etikete çevirmek için "d-block" class' ını kullanabiliriz.

- Bir etiketi inline bir etikete çevirmek için "d-inline" class' ını kullanabiliriz.

- Bir etiketi inline-block bir etikete çevirmek için "d-inline-block" class' ını kullanabiliriz.

```sh
<!-- Inline to Block -->
<span class="d-block bg-danger">d-block</span>
<span class="d-block bg-danger">d-block</span>

<br><br>

<!-- Block to Inline -->
<div class="bg-warning d-inline">d-inline</div>
<div class="bg-warning d-inline">d-inline</div>
     
<br><br>       

<!-- Inline Block-->
<div class="bg-primary d-inline-block">
	<h3>Product Name</h3>
	Description
</div>		
```

 [Demo](https://codepen.io/bedrantirak/pen/WNGZWVx)
 
- "display: none;" ile bir nesneyi görünmez hale getirebiliriz. Bu işlemi bootstrap ile yapmak istersek ".d-none" class' ını kullanmamız gerekir.

##### :point_right: Bootstrap 4' de Text Hizalama ve Display Özelliklerini Responsive Tasarımlar için nasıl kullanabilirim?

 - Örneğin kullanıcı sitemizi telefondan ziyaret ediyorsa yani tarayıcının genişliği mininum 576px ise bu durumda ilk media query aralığındaki css kodları çalışacaktır. Yani ziyaretçilerin hangi çözünürlük arasındaki tarayıcıya sahip olup olmadığını media query aracılığıyla sorgulatıp tespit etmemiz ve ona göre css kodu yazmamız gerekir. Telefondan gelen bir kullanıcı için kullandığımız font büyüklüğü ile geniş ekranlı bir tarayıcı kullanıcısının font büyüklüğü aynı olmamalıdır.
 
 - Tüm bu breakpoint sayısal değerlerini media query 'leri ile kullanmaktansa bootstrap 4 ile gelen hazır responsive ön ek class' ları kullanmamız çok daha kolay.
 - Small cihazlar için .sm
 - Medium cihazlar için .md
 - Large cihazlar için .lg
 - Eksta Large cihazlar için .xl
 
##### :point_right: Bootstrap responsive ön ekleri ile text hizalamayı nasıl yaparız?
- text-sm-right, text-md-right, text-lg-right, text-xl-right 

```sh
<p class="text-sm-right bg-primary">Right aligned on small or larger</p>
<p class="text-md-right bg-primary">Right aligned on medium or larger</p>
<p class="text-lg-right bg-primary">Right aligned on large or larger</p>
<p class="text-xl-right bg-primary">Right aligned on xl or larger</p>
```
[Demo](https://codepen.io/bedrantirak/pen/Exgwzyp)

- Aynı şekilde .text-left ve .text-justify class' larını responsive ön ekleri ile birlikte kullanabilirsiniz.

##### :point_right: Bootstrap responsive ön ekleri ile display class' larını nasıl kullanırız?
-
```sh
<div class="d-none">Hidden on all</div>
<div class="d-none d-sm-block">Hidden only on xs</div>
<div class="d-sm-none d-md-block">Hidden only on sm</div>
<div class="d-md-none d-lg-block">Hidden only on md</div>
<div class="d-lg-none d-xl-block">Hidden only on lg</div>
<div class="d-xl-none">Hidden only on xl</div>
```

[Demo](https://codepen.io/bedrantirak/pen/ZEpXNBr)

- "d-none" ile içerik her zaman gizlidir.

- "d-none d-sm-block" ile içerik sadece ekstra small cihazlarda gizlidir.

- "d-sm-none d-md-block" ile içerik sadece small cihazlarda gizlidir.

- "d-md-none d-lg-block" ile içerik sadece medium cihazlarda gizlidir.

- "d-lg-none d-xl-block" ile içerik sadece large cihazlarda gizlidir.

- "d-xl-none" ile içerik sadece ekstra large cihazlarda gizlidir.

#### :round_pushpin: Bootstrap 4 floating ve position özelliklerrini nasıl kulllanabilirim? 

```sh

```
##### :point_right: Bootstrap 4 ile Floating ve Position

- "Css floating" ve "Css position" özelliklerini Bootstrap 4 ile gelen hazır css class' ları yardımıyla çok daha kolay bir şekilde kullanabiliriz.

- Bir nesneyi sola hizalamak için ".float-left", sağa hizalamak için ise ".float-right" class' larını kullanabiliriz.

```sh
<div class="clearfix">
    <span class="float-left">Float left</span>
    <span class="float-right">Float right</span>
</div>
```
[Demo](https://codepen.io/bedrantirak/pen/QWKaLjN)

- Float uyguladığımız nesneler normal akış dışına çıkıyordu ve daha sonra gelen nesneler istemediğimiz şekilde görünüyordu ve bu sorunu ortadan kaldırmak için bir clear işlemi uygulamamız gerekiyordu. 

```sh
.clearfix::after {
    content: "";
    clear: both;
    display: table;
}
```

- bu şekildeki css kodunu bootstrap içerisinde ".clearfix" class' ı ile kullanıma sunmuşlar. Tek yapmamız gereken clearfix class' ını gerekli yerde kullanmamız.

- Tarayıcının genişliğine göre bir nesneyi sağa ya da sola hizalama işlemi yapmak isterseniz ".float-left" ve .float-right" class' larının responsive karşılıklarını kullanmanız gerekiyor.

- ".float-(r)-left" ve ".float-(r)-right" class' larındaki (r) işaretinin yerine responsive ekler (.sm, .md, .lg, xl ) gelmelidir.

```sh
<div class="float-sm-right">small ve daha büyük cihazlarda</div><br>
<div class="float-md-right">medium ve daha büyük cihazlarda</div><br>
<div class="float-lg-right">large ve daha büyük cihazlarda</div><br>
<div class="float-xl-right">ekstra large ve daha büyük cihazlarda</div><br>
<div class="float-none">Float none</div>
```
-  Responsive float class' larının etkisini görebilmek için tarayıcı genişliğini arttırıp azaltmanız gerekiyor.

##### :point_right: Bootstrap 4 ile Position Fixed ve Sticky Kullanımı

- Boostrap 4' de ".fixed-top" ve ".fixed-bottom" class' ları ile nesneleri sırasıyla yukarıda ya da aşağıda sabitleyebiliriz. Ayrıca ".sticky-top" class' ı ile relative bir nesneyi kaydırma çubuğu ile nesne üst pencereye getirdiğimiz anda en yukarıda sabitleyebiliriz.

```sh
<h3 class="fixed-top">Fixed Top</h3>
  <p>Lorem ipsum dolor sit amet...</p>
		
  <h3 class="sticky-top">Fixed Sticky</h3>
  <p>Lorem ipsum dolor sit amet...</p>
		
  <h3 class="fixed-bottom">Fixed Bottom</h3>
```
[Demo](https://codepen.io/bedrantirak/pen/xxEpKOj)

#### :round_pushpin: Boostrap 4 ile yazı rengi, link rengi, buton rengi ve zemin renkleri için css class' ları nelerdir ve bootstrap renk class' larını nasıl kullanıyoruz?

- Boostrap 4 css kütüphanesi ile web sayfalarımızda önceden belirlenmiş renk kodları içeren css sınıflarını kullanarak güzel görünümler oluşturabiliriz.

##### :point_right: Boostrap 4 ile Yazı Renkleri

- Bootstrap 4 ile yazıları renklendirmek için kullanabileceğimiz bootstrap text css class' ları aşağıdadır.

- ".text-muted" : This text is muted.

- ".text-primary" : This text is important.

- ".text-success" : This text indicates success.

- ".text-info" : This text represents some information.

- ".text-warning" : This text represents a warning.

- ".text-danger" : This text represents danger.

- ".text-secondary" : Secondary text.

- ".text-dark" : Default body color (often black).

- ".text-white" : This text is dark grey.

- ".text-body" : This text is light grey (on white background).

- ".text-light" : This text is white (on white background).

[Demo](https://codepen.io/bedrantirak/pen/MWjreEz)

##### :point_right: Bootstrap 4 ile Link Renkleri
- Bootstrap 4 ile linkleri renklendirmek için kullanabileceğimiz bootstrap link css class' ları aşağıdadır.
```sh
<div class="container">
  <h2>Bootstrap 4 ile Link Renkleri</h2>
  <p>** :hover olayı için link üzerine geliniz.</p>
  <a href="#" class="text-muted">Muted link.</a>
  <a href="#" class="text-primary">Primary link.</a>
  <a href="#" class="text-success">Success link.</a>
  <a href="#" class="text-info">Info link.</a>
  <a href="#" class="text-warning">Warning link.</a>
  <a href="#" class="text-danger">Danger link.</a>
  <a href="#" class="text-secondary">Secondary link.</a>
  <a href="#" class="text-dark">Dark grey link.</a>
  <a href="#" class="text-body">Body/black link.</a>
  <a href="#" class="text-light">Light grey link.</a>
</div>
```
[Demo](https://codepen.io/bedrantirak/pen/wvzXaxR)

##### :point_right: Bootstrap 4 ile Arkaplan Renkleri
- Bootstrap 4 ile background-color yani zemin rengi vermek için kullanabileceğimiz bootsrap background css class' ları aşağıdadır.
```sh
<div class="container">
  <h2>Bootstrap 4 ile Arkaplan Renkleri</h2>
  <p class="bg-primary text-white">This text is important.</p>
  <p class="bg-success text-white">This text indicates success.</p>
  <p class="bg-info text-white">This text represents some information.</p>
  <p class="bg-warning text-white">This text represents a warning.</p>
  <p class="bg-danger text-white">This text represents danger.</p>
  <p class="bg-secondary text-white">Secondary background color.</p>
  <p class="bg-dark text-white">Dark grey background color.</p>
  <p class="bg-light text-dark">Light grey background color.</p>
</div>
```
[Demo](https://codepen.io/bedrantirak/pen/xxEzGQq)

##### :point_right: Boostrap 4 ile Button Renkleri

- Bootstrap 4 ile button rengi vermek için kullanabileceğimiz bootsrap button css class' ları aşağıdadır.

```sh
<div class="container">
 <h2>Bootstrap 4 ile Button Renkleri</h2>
 <button type="button" class="btn">Basic</button>
 <button type="button" class="btn btn-primary">Primary</button>
 <button type="button" class="btn btn-secondary">Secondary</button>
 <button type="button" class="btn btn-success">Success</button>
 <button type="button" class="btn btn-info">Info</button> 
 <button type="button" class="btn btn-warning">Warning</button>
 <button type="button" class="btn btn-danger">Danger</button>
 <button type="button" class="btn btn-dark">Dark</button>
 <button type="button" class="btn btn-light">Light</button>
 <button type="button" class="btn btn-link">Link</button>
</div>
```
[Demo](https://codepen.io/bedrantirak/pen/XWjYbOj)

#### :round_pushpin: Bootstrap 4 ile Tablo Tasarımı Nasıl Yapılır?
- "<table>" etiketine sadece ".table" class' ını ekleyerek tablomuza padding ve yatay çizgileri eklemiş oluyoruz.

```sh
<table class="table">
  <tr>
     <th>Kurs</th>
     <th>Ders Sayısı</th> 
     <th>Öğrenci Sayısı</th>
  </tr>
  <tr>
     <td>Komple Uygulamalı Web Geliştirme Eğitimi</td>
     <td>325</td> 
     <td>3000</td>
  </tr>
  <tr>
    <td>Uygulamalı Programlama Eğitimi</td>
    <td>126</td> 
    <td>500</td>
  </tr>
</table>
```
[Demo](https://codepen.io/bedrantirak/pen/XWjBqQy)

- ".table-striped" class' ını ekleyerek tablomuzun her satırını farklı renk ile daha belirgin hale getirebiliriz.,
```sh
<table class="table table-striped">
  <tr>
    <td> </td>
  </tr> 
</table>
```
[Demo](https://codepen.io/bedrantirak/pen/zYKLjQy)

- ".table-bordered " class' ını ekleyerek tablomuza kenarlık ekleyebiliriz.
```sh
<table class="table table-bordered">
  <tr>
    <td> </td>
  </tr>  
</table>
```
[Demo](https://codepen.io/bedrantirak/pen/yLaqjdj)

- .table-hover class' ını ekleyerek her satır üzerine geldiğimizde satırı öne çıkaracak bir zemin rengi görünmesini sağlayabiliriz.
```sh
<table class="table table-hover">
  <tr>
    <td> </td>
  </tr>  
</table>
```
[Demo](https://codepen.io/bedrantirak/pen/OJRwZKp)

- ".table-borderless" class' ını ekleyerek tablonun tüm kenarlıklarını silebiliriz.
```sh
<table class="table table-borderless">
  <tr>
    <td> </td>
  </tr>  
</table>
```
- ".table-dark" class' ını ekleyerek siyah bir tablo elde edebiliriz.
```sh
<table class="table table-borderless table-dark">
  <tr>
    <td> </td>
  </tr>  
</table>
```

- ".table-sm" class' ını ekleyerek daha az padding değerine sahip tablo elde edebiliriz.
```sh
<table class="table table-sm">
  <tr>
    <td> </td>
  </tr>  
</table>
```

- Tablolar için kullanabileceğimiz bazı renk class' ları vardır. Bu class' ları "table", "tr" ya da "td" etiketlerine uygulayıp ister satır ister kolon istersek de tablonun kendisi için arkaplan rengi oluşturabiliriz.

- Bootstrap tablolar ile kullanabileceğimiz renk class' ları ".table-active, .table-primary, .table-secondary, .table-success, .table-danger, .table-warning, .table-info, .table-light, .table-dark" class' larıdır.

```sh
<table class="table">
    <thead>
      <tr>
        <th>Firstname</th>
        <th>Lastname</th>
        <th>Email</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td>Default</td>
        <td>Defaultson</td>
        <td>def@somemail.com</td>
      </tr>      
      <tr class="table-primary">
        <td>Primary</td>
        <td>Joe</td>
        <td>joe@example.com</td>
      </tr>
      <tr class="table-success">
        <td>Success</td>
        <td>Doe</td>
        <td>john@example.com</td>
      </tr>
      <tr class="table-danger">
        <td>Danger</td>
        <td>Moe</td>
        <td>mary@example.com</td>
      </tr>
      <tr class="table-info">
        <td>Info</td>
        <td>Dooley</td>
        <td>july@example.com</td>
      </tr>
      <tr class="table-warning">
        <td>Warning</td>
        <td>Refs</td>
        <td>bo@example.com</td>
      </tr>
      <tr class="table-active">
        <td>Active</td>
        <td>Activeson</td>
        <td>act@example.com</td>
      </tr>
      <tr class="table-secondary">
        <td>Secondary</td>
        <td>Secondson</td>
        <td>sec@example.com</td>
      </tr>
      <tr class="table-light">
        <td>Light</td>
        <td>Angie</td>
        <td>angie@example.com</td>
      </tr>
      <tr class="table-dark text-dark">
        <td>Dark</td>
        <td>Bo</td>
        <td>bo@example.com</td>
      </tr>
    </tbody>
 </table>
```
[Demo](https://codepen.io/bedrantirak/pen/dypjKPo)

- Bootstrap 4 ile responsive bir tablo oluşturmak için ".table-responsive" class' ını kullanmalıyız. Eğer tablomuz satırda tüm içeriğini gösteremezse bu durumda kaydırma çubukları gösterilir.

```sh
<div class="table-responsive">
    <table class="table">

    </table>
</div>
```
[Demo](https://codepen.io/bedrantirak/pen/ExgpRaJ)

#### :round_pushpin: Bootsrap 4 Image class' ları ile Resim Biçimlendirme İşlemleri

- Bootstrap 4 image class' ları ile köşeleri yuvarlatılmış resimleri ".rounded" class' ını kullanarak oluşturabiliriz.

- Bootstrap 4 image class' ları ile köşeleri tam yuvarlatılmış resimleri ".rounded-circle" class' ını kullanarak oluşturabiliriz.

- Bootstrap 4 image class' ları ile thumbnail resimleri ".img-thumbnail" class' ını kullanarak oluşturabiliriz.

- Bootstrap 4 .float-left ve .float-right class' ları ile resimleri sağa ya da sola hizalayabiliriz.

- Bootstrap 4 ile resmi ortalamak için .mx-auto (sağ ve soldan margin) ve .d-block class' larını kullanabiliriz.

- Bootstrap 4 ile responsive bir resim oluşturmak için .img-fluid class' ını kullanabiliriz. Bir resme .img-fluid eklediğimizde width:100%; ve height:auto; özelliklerini uygulamış oluyoruz dolayısıyla resmin genişliği içinde bulunduğu etiketin genişliğine göre ayarlanmış oluyor.

#### :round_pushpin: Boostrap Jumbotron nedir ve nasıl oluşturulur?

- Boostrap Jumbotron gri bir arka zemine sahip olan bir bölmedir ve genelde web sayfamızın amacını bildiren bir başlık ve açıklamayı barındırır.
- Jumbotron kısmını oluşturmak için .jumbotron class' ına sahip bir "div" etiketi oluşturmamız gerekiyor.
```sh
<div class="jumbotron">
  <h1>Bootstrap Tutorial</h1> 
  <p>Bootstrap is the most popular HTML, CSS and JS framework for developing </p> 
</div>
```
- Eğer ki satırı kaplayan bir bootstrap jumbotron oluşturmak isterseniz .jumbotron class' ından sonra .jumbotron-fluid class' ını da eklemelisiniz.

- Ayrıca jumbotron' un gri zemin rengi satırı kapladıktan sonra içeriğinde ortalanmasını yani aynı şekilde kenarlara kadar gelmemesi için .container class' ını kullanmalıyız.

```sh
<div class="jumbotron jumbotron-fluid">
  <div class="container">
    <h1>Bootstrap Tutorial</h1> 
    <p>Bootstrap is the most popular HTML, CSS and JS framework for developing</p> 
  </div>
</div>
```
#### :round_pushpin: Bootstrap alerts nedir ve nasıl kullanılır?

- Boostrap 4 alert class' ları ile amacınıza uygun mesaj içeriklerinizi gösterebilirsiniz.

- Örneğin kayıt işleminden sonra işlemin başarılı olduğunu söylemek için yeşil zemin rengine sahip bir alert kutusu ya da bir hata mesajını göstermek için kırmızı zemin rengine sahip bir alert kutusu kullanabilirsiniz.

- Alert kutularını oluşturmak için .alert class' ından sonra .alert-success, .alert-info, .alert-warning, .alert-danger, .alert-primary, .alert-secondary, .alert-light, .alert-dark class' larından birini kullanabilirsiniz.

```sh
<div class="alert alert-primary" role="alert">
  A simple primary alert—check it out!
</div>
<div class="alert alert-secondary" role="alert">
  A simple secondary alert—check it out!
</div>
<div class="alert alert-success" role="alert">
  A simple success alert—check it out!
</div>
<div class="alert alert-danger" role="alert">
  A simple danger alert—check it out!
</div>
<div class="alert alert-warning" role="alert">
  A simple warning alert—check it out!
</div>
<div class="alert alert-info" role="alert">
  A simple info alert—check it out!
</div>
<div class="alert alert-light" role="alert">
  A simple light alert—check it out!
</div>
<div class="alert alert-dark" role="alert">
  A simple dark alert—check it out!
</div>
```
[Demo](https://codepen.io/bedrantirak/pen/jOMvKvp)

- Alert kutusu içinde bir link oluşturmak için .alert-link class' ını kullanabiliriz.

```sh
<div class="alert alert-primary" role="alert">
  A simple primary alert with <a href="#" class="alert-link">an example link</a>. Give it a click if you like.
  </div>
```
[Demo](https://codepen.io/bedrantirak/pen/bGwxKmL)

- Kullanıcının alert kutusunu kapatması için bir icon ekleyebiliriz.
```sh
<div class="alert alert-warning alert-dismissible fade show" role="alert">
  <strong>Holy guacamole!</strong> You should check in on some of those fields below.
  <button type="button" class="close" data-dismiss="alert" aria-label="Close">
    <span aria-hidden="true">&times;</span>
  </button>
</div>
```
[Demo](https://codepen.io/bedrantirak/pen/eYdLKQo)

#### :round_pushpin: Bootstrap 4 Button Kullanımı

- Bootstrap 4 Buttons sınıfları ile a, button ya da input etiketleri için kullanabilecek olduğumuz bootstrap button class' ları ile güzel görünümlü butonları saniyeler içinde oluşturabiliriz.

```sh
<a href="#" class="btn btn-primary" role="button">Link Button</a>
<button type="button" class="btn btn-danger">Button</button>
<input type="button" class="btn btn-success" value="Input Button">
<input type="submit" class="btn btn-warning" value="Submit Button">
```
[Demo](https://codepen.io/bedrantirak/pen/VwKqyRx)

- Bootstrap 4 button oluşturmak için ilk olarak .btn class' ını ilgili etikete vermeliyiz ardından farklı stildeki butonlar için kullanabilecek olduğumuz button class' larından (.btn-primary, .btn-secondary, .btn-success, .btn-danger, .btn-warning, .btn-info, .btn-dark, .btn-light) bir tane seçmeliyiz.

```sh
<button type="button" class="btn">Basic</button>
<button type="button" class="btn btn-primary">Primary</button>
<button type="button" class="btn btn-secondary">Secondary</button>
<button type="button" class="btn btn-success">Success</button>
<button type="button" class="btn btn-info">Info</button>
<button type="button" class="btn btn-warning">Warning</button>
<button type="button" class="btn btn-danger">Danger</button>
<button type="button" class="btn btn-dark">Dark</button>
<button type="button" class="btn btn-light">Light</button>
<button type="button" class="btn btn-link">Link</button>
```

[Demo](https://codepen.io/bedrantirak/pen/xxEmpeX)

- Bootstrap 4 ile outline butonuda oluşturabiliriz.

```sh
<button type="button" class="btn btn-outline-primary">Primary</button>
<button type="button" class="btn btn-outline-secondary">Secondary</button>
<button type="button" class="btn btn-outline-success">Success</button>
<button type="button" class="btn btn-outline-info">Info</button>
<button type="button" class="btn btn-outline-warning">Warning</button>
<button type="button" class="btn btn-outline-danger">Danger</button>
<button type="button" class="btn btn-outline-dark">Dark</button>
<button type="button" class="btn btn-outline-light text-dark">Light</button>
```
[Demo](https://codepen.io/bedrantirak/pen/yLaGpWO)

- Bootstrap 4 ile farklı boyutlarda button oluşturmak için kullanabileceğimiz .btn-sm, .btn-large ve .btn-block class' ları vardır.

```sh
<button type="button" class="btn btn-primary btn-lg">Large</button>
<button type="button" class="btn btn-primary">Default</button>
<button type="button" class="btn btn-primary btn-sm">Small</button>
```
-  .btn-sm ile küçük bir buton .btn-large ile büyük bir buton oluşturabiliriz.

[Demo](https://codepen.io/bedrantirak/pen/VwKqyJd)

- .btn-block class' ı ile bir block eleman şeklinde yani satırı olduğu gibi kaplayan bir buton oluşturabiliriz.
```sh
<button type="button" class="btn btn-primary btn-block">Full-Width Button</button>
```
- .active class' ı ile butona tıklanmış hissi verebiliriz.

- .disabled class' ı ile butonu pasif hale getirebiliriz ancak a etiketi için .disabled sadece görüntü açısından pasif hissini verir.

```sh
<button type="button" class="btn btn-primary active">Active Primary</button>
<button type="button" class="btn btn-primary" disabled>Disabled Primary</button>
<a href="#" class="btn btn-primary disabled">Disabled Link</a>
```
[Demo](https://codepen.io/bedrantirak/pen/ExgGQYv)

#### :round_pushpin: Bootstrap Button Grupları Nasıl Oluşturulur?

- Boostrap 4 ile oluşturduğumuz butonları .btn-group class' ını kullanarak gruplayabiliriz.

```sh
<div class="btn-group">
  <button type="button" class="btn btn-primary">First</button>
  <button type="button" class="btn btn-primary">Second</button>
  <button type="button" class="btn btn-primary">Third</button>
</div>
```
  [Demo](https://codepen.io/bedrantirak/pen/ZEpZJKm)
 
 - Buton grupları oluşturduğumuzda buton boyutları için kullandığımız .btn-sm ve .btn-lg class' larını her bir butona tek tek vermektense gruba verip bütün butonların boyutlarını aynı yapabiliriz.
 
```sh
<div class="btn-group btn-group-lg">
  <button type="button" class="btn btn-primary">First</button>
  <button type="button" class="btn btn-primary">Second</button>
  <button type="button" class="btn btn-primary">Third</button>
</div>
```
[Demo](https://codepen.io/bedrantirak/pen/zYKXdzX)

- Butonları alt alta gruplayıp dikey bir menü görüntüsü oluşturmak için .btn-group yerine .btn-group-vertical class' ını kullanmalıyız.

```sh
<div class="btn-group btn-group-vertical">
  <button type="button" class="btn btn-primary">First</button>
  <button type="button" class="btn btn-primary">Second</button>
  <button type="button" class="btn btn-primary">Third</button>
</div>
```
[Demo](https://codepen.io/bedrantirak/pen/abmxyyg)

- Button grubu içindeki her hangi bir buton için bir dropdown menü oluşturabiliriz.

```sh
<div class="btn-group">
  <button type="button" class="btn btn-primary">First</button>
  <button type="button" class="btn btn-primary">Second</button>
  <div class="btn-group">
    <button type="button" class="btn btn-primary dropdown-toggle" data-toggle="dropdown">
       Third
    </button>
    <div class="dropdown-menu">
      <a class="dropdown-item" href="#">Fifth</a>
      <a class="dropdown-item" href="#">Six</a>
    </div>
 </div>
```
[Demo](https://codepen.io/bedrantirak/pen/PoGgKOj)
