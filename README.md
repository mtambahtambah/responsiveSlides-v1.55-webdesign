# responsiveSlides-v1.55-webdesign
responsiveSlides v1.55 

## `1` buat file namanya bebas 
kemudian isi file dengan ini:
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>responsiveSlides v1.55</title>

    <!--(1) link dan script -->
    
    <!--/(1) link dan script -->


    <!--(2) cara penggunaan script  -->
    <script>
    // anda bisa jugha menggunkan "$(window).load(function() {"
    $(function () {
    // Taruh skrip dibawah ------------------------
    
    
    // Taruh skrip diatas ------------------------
    });
    </script>
    <!--/(2) cara penggunaan script  -->

</head>
<body>
    <!--(3) tag html -->

    <!--/(3) tag html -->
</body>
</html>
```

## `2` masukan link dan script
```html
    <link rel="stylesheet" href="./responsiveslides.css">
    <link rel="stylesheet" href="./demo/demo.css">
    <script src="http://ajax.googleapis.com/ajax/libs/jquery/3.0.0/jquery.min.js"></script>
    <script src="./responsiveslides.min.js"></script>
```

## `3` cara penggunaan script
pilih dan tentukan :
```js
      // Slideshow 1
      $("#slider1").responsiveSlides({
        maxwidth: 800,
        speed: 800
      });

      // Slideshow 2
      $("#slider2").responsiveSlides({
        auto: false,
        pager: true,
        speed: 300,
        maxwidth: 540
      });

      // Slideshow 3
      $("#slider3").responsiveSlides({
        manualControls: '#slider3-pager',
        maxwidth: 540
      });

      // Slideshow 4
      $("#slider4").responsiveSlides({
        auto: false,
        pager: false,
        nav: true,
        speed: 500,
        namespace: "callbacks",
        before: function () {
          $('.events').append("<li>before event fired.</li>");
        },
        after: function () {
          $('.events').append("<li>after event fired.</li>");
        }
      });
```

## `4` masukan tag html
pilih dan tentukan:
```html

    <!-- Slideshow 1 -->
    <ul class="rslides" id="slider1">
      <li><img src="images/1.jpg" alt=""></li>
      <li><img src="images/2.jpg" alt=""></li>
      <li><img src="images/3.jpg" alt=""></li>
    </ul>



    <!-- Slideshow 2 -->
    <ul class="rslides" id="slider2">
      <li><a href="#"><img src="images/1.jpg" alt=""></a></li>
      <li><a href="#"><img src="images/2.jpg" alt=""></a></li>
      <li><a href="#"><img src="images/3.jpg" alt=""></a></li>
    </ul>



    <!-- Slideshow 3 -->
    <ul class="rslides" id="slider3">
      <li><img src="images/1.jpg" alt=""></li>
      <li><img src="images/2.jpg" alt=""></li>
      <li><img src="images/3.jpg" alt=""></li>
    </ul>

    <!-- Slideshow 3 Pager -->
    <ul id="slider3-pager">
      <li><a href="#"><img src="images/1_thumb.jpg" alt=""></a></li>
      <li><a href="#"><img src="images/2_thumb.jpg" alt=""></a></li>
      <li><a href="#"><img src="images/3_thumb.jpg" alt=""></a></li>
    </ul>



    <!-- Slideshow 4 -->
    <div class="callbacks_container">
      <ul class="rslides" id="slider4">
        <li>
          <img src="images/1.jpg" alt="">
          <p class="caption">This is a caption</p>
        </li>
        <li>
          <img src="images/2.jpg" alt="">
          <p class="caption">This is another caption</p>
        </li>
        <li>
          <img src="images/3.jpg" alt="">
          <p class="caption">The third caption</p>
        </li>
      </ul>
    </div>
```

## `5` Opsi yang dapat Anda sesuaikan
standar:
```js
  $(".rslides").responsiveSlides();
```
pilihan:
```js
$(".rslides").responsiveSlides({
  auto: true,          // Boolean: Menganimasikan secara otomatis, benar atau salah
  speed: 500,          // Integer: Kecepatan transisi, dalam milidetik
  timeout: 4000,       // Integer: Waktu antara transisi slide, dalam milidetik
  pager: false,        // Boolean: Tampilkan pager, benar atau salah
  nav: false,          // Boolean: Tampilkan navigasi, benar atau salah
  random: false,       // Boolean: Acak urutan slide, benar atau salah
  pause: false,         // Boolean: Jeda saat mengarahkan kursor, benar atau salah
  pauseControls: true,    // Boolean: Jeda saat mengarahkan kontrol, benar atau salah
  prevText: "Previous",   // String: Teks untuk tombol "sebelumnya"
  nextText: "Next",   // String: Teks untuk tombol "berikutnya"
  maxwidth: "",          // Integer: Lebar maksimum tayangan slide, dalam piksel
  navContainer: "",// Selector: Di mana kontrol harus ditambahkan, defaultnya adalah setelah 'ul'
  manualControls: "",     // Selector: Deklarasikan navigasi pager kustom
  namespace: "rslides",  // String: Ubah namespace default yang digunakan
  before: function(){}, // Fungsi: Sebelum panggilan balik
  after: function(){}   // Fungsi: Sesudah panggilan balik
});
```

## `6` contoh full sederhana
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>responsiveSlides v1.55</title>

    <!--(1) link dan script -->
    <link rel="stylesheet" href="./responsiveslides.css">
    <link rel="stylesheet" href="./demo/demo.css">
    <script src="http://ajax.googleapis.com/ajax/libs/jquery/3.0.0/jquery.min.js"></script>
    <script src="./responsiveslides.min.js"></script>
    <!--/(1) link dan script -->


    <!--(2) cara penggunaan script  -->
    <script>
    // anda bisa jugha menggunkan "$(window).load(function() {"
    $(function () {
    // Taruh skrip dibawah ------------------------
          // Slideshow 4
          $("#slider4").responsiveSlides({
        auto: false,
        pager: false,
        nav: true,
        speed: 500,
        namespace: "callbacks",
        before: function () {
          $('.events').append("<li>before event fired.</li>");
        },
        after: function () {
          $('.events').append("<li>after event fired.</li>");
        }
      });
    
    // Taruh skrip diatas ------------------------
    });
    </script>
    <!--/(2) cara penggunaan script  -->

</head>
<body>
    <!--(3) tag html -->
 <!-- Slideshow 4 -->
 <div class="callbacks_container">
    <ul class="rslides" id="slider4">
      <li>
        <img src="./demo/images/1.jpg" alt="">
        <p class="caption">This is a caption</p>
      </li>
      <li>
        <img src="./demo/images/2.jpg" alt="">
        <p class="caption">This is another caption</p>
      </li>
      <li>
        <img src="./demo/images/3.jpg" alt="">
        <p class="caption">The third caption</p>
      </li>
    </ul>
  </div>
    <!--/(3) tag html -->
</body>
</html>
```
