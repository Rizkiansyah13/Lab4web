# Praktikum 2
# Pemrograman Web
```
Muhammad Rizkiansyah
311910071
TI.19.C.1
Universitas Pelita Bangsa
```
## 1. Membuat dokumen HTML
Buatlah dokumen HTML seperti berikut
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>CSS Dasar</title>
</head>
<body>
    <header>
      <h1>CSS Internal dan <i>Inline CSS</i></h1>
    </header>
    <nav>
      <a href="lab2_css_dasar.html">CSS Dasar</a>
      <a href="lab2_css_eksternal.html">CSS Eksternal</a>
      <a href="lab1_tag_dasar.html">HTML Dasar</a>
    </nav>
    <!-- CSS ID Selector -->
    <div id="intro">
      <h1>Hello World</h1>
      <p>Kami sedang belajar HTML dan CSS dasar, pada mata kuliah <b>Pemrograman Web</b> di <i>Universitas Pelita Bangsa</i>. Pelajaran pertama yang kami dapat adalah membuat tampilan web sederhana dalam rangka mengenal tag-tag dasar HTML dan CSS.</p>
      <!-- CSS Class Selector -->
      <a class="button btn-primary" href="#intro">Informasi selengkapnya.</a>
    </div>
</body>
</html>
```
![LANGKAH 1 P2](https://user-images.githubusercontent.com/81758407/113469141-7a5e0a80-9475-11eb-89f0-98614553be3e.PNG)

## 2. Mendeklarasikan CSS Internal
Kemudian tambahkan deklarasi CSS internal seperti berikut pada bagian head dokumen.
```
<head>
    <title>CSS Dasar</title>
    <style>
        body {
            font-family:'Open Sans', sans-serif;
        }
        header {
            min-height: 80px;
            border-bottom:1px solid #77CCEF;
        }
        h1 {
            font-size: 24px;
            color: #0F189F;
            text-align: center;
            padding: 20px 10px;
        }
        h1 i {
            color:#6d6a6b;
        }
    </style>
</head>
```
![LANGKAH 2 P2](https://user-images.githubusercontent.com/81758407/113469337-f86ee100-9476-11eb-82cf-d6f3ae1d64f2.PNG)

## 3. Menambahkan Inline CSS
Kemudian tambahkan deklarasi inline CSS pada tag <p> seperti berikut. 

```
<p style="text-align: center; color: #ccd8e4;">
```
![LANGKAH 3 P2](https://user-images.githubusercontent.com/81758407/113469450-bc884b80-9477-11eb-8da8-0fbf5ee62bee.PNG)

## 4. Membuat CSS Eksternal
Buatlah file baru dengan nama style_eksternal.css kemudian buatlah deklarasi CSS seperti berikut.
```
nav {
    background: #20A759;
    color:#fff;
    padding: 10px;
}
nav a {
    color: #fff;
    text-decoration: none;
    padding:10px 20px;
}
nav .active,
nav a:hover {
    background: #0B6B3A;
}
```
![css](https://user-images.githubusercontent.com/81758407/113469546-85ff0080-9478-11eb-880f-724cc1db740d.PNG)
Kemudian tambahkan tag <link> untuk merujuk file css yang sudah dibuat pada bagian <head>
    
```    
<head>
    <!-- menyisipkan css eksternal -->
    <link rel="stylesheet" href="style_eksternal.css" type="text/css">
</head>
```
![LANGKAH 4 P2](https://user-images.githubusercontent.com/81758407/113469571-b8a8f900-9478-11eb-9df0-f1d1c1cbb613.PNG)

## 5. Menambahkan CSS Selector
Selanjutnya menambahkan CSS Selector menggunakan ID dan Class Selector. Pada file
style_eksternal.css, tambahkan kode berikut.
```
/* ID Selector */
#intro {
    background: #418fb1;
    border: 1px solid #099249;
    min-height: 100px;
    padding: 10px;
}
#intro h1 {
    text-align: left;
    border: 0;
    color: #fff;
}
/* Class Selector */
.button {
    padding: 15px 20px;
    background: #bebcbd;
    color: #fff;
    display: inline-block;
    margin: 10px;
    text-decoration: none;
}
.btn-primary {
    background: #E42A42;
}
```
![LANGKAH 5 P2](https://user-images.githubusercontent.com/81758407/113486609-effdc100-94dd-11eb-8be2-20d12dcb8fbc.PNG)


## Pertanyaan dan Tugas
1. Lakukan eksperimen dengan mengubah dan menambah properti dan nilai pada kode CSS dengan mengacu pada CSS Cheat Sheet yang diberikan pada file terpisah dari modul ini.

```
saya melakukan eksperimen menambah kolom nav, merubah nilai padding pada nav a dan merubah warna.
```
![soal 1](https://user-images.githubusercontent.com/81758407/113593695-ea7cb400-9660-11eb-96fc-6aec21b1d022.PNG)

2. Apa perbedaan pendeklarasian CSS elemen h1 {...} dengan #intro h1 {...}? berikan penjelasannya!
```
Pada pendeklarasian CSS elemen h1 mengubah tampilan seluruh elemen yang memiliki tag h1, sedangkan #intro h1 hanya mengubah tampilan elemen h1 yang memiliki id #intro.
```
3. Apabila ada deklarasi CSS secara internal, lalu ditambahkan CSS eksternal dan inline CSS pada elemen yang sama. Deklarasi manakah yang akan ditampilkan pada browser? Berikan penjelasan dan contohnya!
```
Pendeklarasikan CSS pada elemen yang sama namun dengan isi deklarasi yang berbeda, maka semua deklarasi CSS tersebut akan ditampilkan. Namun jika isi dari ketiga deklarasi CSSnya sama semua, maka browser hanya akan menampilkan salah satunya, dengan urutan Inline CSS, Eksternal CSS, dan yang terakhir Internal CSS.
```
4. Pada sebuah elemen HTML terdapat ID dan Class, apabila masing-masing selector tersebut terdapat deklarasi CSS, maka deklarasi manakah yang akan ditampilkan pada browser? Berikan penjelasan dan contohnya! ( <p id="paragraf-1" class="text-paragraf"> ).

```
Kedua deklarasi tersebut akan tampil, namun selector ID yang akan tampil jika deklarasinya ada yang sama antara ID dan Class.
