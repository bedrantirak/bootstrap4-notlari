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

##### :point_right: Bootstrap 4 Display Heading

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
  

