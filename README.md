# :octocat: Bootstrap 4 :b: 



[![Build Status](https://travis-ci.org/joemccann/dillinger.svg?branch=master)](https://travis-ci.org/joemccann/dillinger)

#### :round_pushpin: Bootstrap nedir ve nasıl kullanılr? Bootstrap 4 ile modern responsive web siteleri nasıl yapılır?

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
- Responsive tasarımın etkin olabilmesi için aşağıdaki responsive meta etiketini [<head>]() kısmına eklememiz gerekiyor.
```sh
  <meta name="viewport" content="width=device-width, initial-scale=1">
```
- [width = device-width]() özelliği cihazın ekran genişliğini algılayıp sayfanın genişliğini bu değere eşitlemesi ile alakalıdır.
- [initial-scale = 1]() ise sayfa ölçeklendirmesini (zoom) ayarlar.
- Bootstrap Kurulumu için ilk olarak bootstrap css ve javascript dosyalarını sayfamıza eklememiz gerekiyor.- Bootstrap "css class" larını kullanabilmek için ["bootstrap.min.css"]() dosyasının "cdn" adresini html sayfamızın "<head>" kısmına eklememiz gerekiyor.

```sh
<link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.1.3/css/bootstrap.min.css">
```
- ["Bootstrap Javascript Component"]() leri kullanabilmel için ise aşağıdaki javascript kütüphanelerini "</body>" kapanış etiketinin hemen üstüne eklememiz gerekiyor.

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
- her kolon ".col-* " sınıfı ile belirlenir.
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

- @media query' ler ile tarayıcının o anki genişliğini alabiliyoruz ve aldığımğz bu değerlere göre "<div>" etiketlerini yani bootstrap açısından baktığımızda oluşturduğumuz her kolonun yan yana ya da alt alta alabiliriz.

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
 

