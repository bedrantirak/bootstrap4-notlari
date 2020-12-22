# Bootstrap 4



[![Build Status](https://travis-ci.org/joemccann/dillinger.svg?branch=master)](https://travis-ci.org/joemccann/dillinger)

##### :one: Bootstrap nedir ve nasıl kullanılr? Bootstrap 4 ile modern responsive web siteleri nasıl yapılır?

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
  
##### :two: Bootstrap 4 kütüphanesini nasıl kullanırım? Bootstrap css ve javascript dosyalarını sayfama nasıl ekleyebilirim? 

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
