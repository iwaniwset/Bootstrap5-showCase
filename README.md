# Bootstrap5-showCase

## Instal Dependencies yang diperluka

- npm init -y
- buat folder `scss` kemudian buat file style.css
- install sass, fontawesome, postcss, autoprefixre, bootstrap
- pada package json tambahkan `"compile:sass": "sass --watch scss:assets/css"`
- kemudian pada terminal jalankan `npm run compile:sass` ini akan menjalankan script yg berada pada _package.json_ dan akan mengupdate perubahan yang terjadi pada file kita. mirip seperti `nodemon` di server _node.js_
- selain itu juga terbuat sebuah folder assets/css yang di dalamnya terdapat 2 file yakni `style.css` dan `style.css.map`

## Customisasi Bootstrap

- setelah itu buat folder baru `theming-kit.html` isi file tersebut dengan theming code berikut [theming-kit.html](https://github.com/MuriungiPatrick/Bootstrap-5-Theming-Kit/blob/main/theming-kit.html)
- kalian bisa coba menjalankan file `theming-kit.html` disini warna dari primary color adalah biru dan gray
- saya membuat file baru di dalam scss untuk memudahkan kita mencustomize variable yang akan kita gunakan, saya beri nama filenya \_custom.scss `Kalian bebas untuk menamainya sesuai selera kalian`
- jangan lupa untuk mengimport bootstrap.scss yang berada di node_modules ke dalam file \_custom.scss
- sekarang kita bisa mengkostumisasi variabel sesuai keinginan kalian.
- saya berikan contoh kita akan mengganti `primary color` & `secondary color`

### code 1

```Javascript
// file scss/_custom.scss

    // Theme Color
$orange:  #fd7e14 ;
$green:   #198754 ;

$primary:       $orange ;
$secondary:     $green ;

// IMPORT BOOTSTRAP 5
@import "../node_modules/bootstrap/scss/bootstrap.scss";
```

- link `style.css` yang berada di _assets_ dengan `theming-kit.html`, karena `style.css` yang berada di _scss_ nantinya akan di compile menjadi `style.css` yang berada di _assets_
- setelah di kustomisasi makan warna primary dan secondary akan berubah menjadi `orange` dan `green`
