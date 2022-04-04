# PEMOGRAMAAN WEB

Diyan Arum Maheswari (312010133)

Teknik Informatika - UNIVERSITAS PELITA BANGSA
______________________________________________

## MEMBUAT BOX ELEMENT

Pertama, disini saya akan membuat sebuah dokumen dasar Htmlnya terlebih dahulu, sebelum nantinya akan saya tambahkan kode untuk membuat sebuah Box Element.

[menambahkan_gambar](img/BOX%20ELEMENT%20POLOS.png)

Berikut codingan yang saya gunakan untuk membuat sebuah dokumen dasar dengan judul Box Element dari Html.

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title> Element</title>
</head>
<body>
    <header>
        <h1>Box Element</h1>
    </header>
</body>
</html>    
```

Setelah membuat dasarnya seperti diatas, selanjutnya tambahkan sebuah kode untuk membuat Box Element dengan tag div seperti dibawah ini:

[menambahkan_gambar](img/BOX%20ELEMENT%20DIV.png)

Dengan menggunakan kode berikut:

```html
<section>
    <div class="div1">Div 1</div>
    <div class="div2">Div 2</div>
    <div class="div3">Div 3</div>
</section>
```
[menambahkan_gambar](img/BOX%20ELEMENT%20DIV%20WARNA.png)

Dan jika kalian ingin divnya lebih berwarna atau lebih bervariasi lagi seperti gambar diatas, kalian dapat menggunakan kode dibawah ini pada bagian headnya untuk membuat sebuah deklarasi CSS Float Property.

```html
<style>
    div {
        float:left;
        padding: 10px;
    }
    .div1 {
        background: hsl(334, 65%, 78%);
    }
    .div2 {
        background: rgb(212, 103, 145);
    }
    .div3 {
        background: rgb(173, 32, 82);
    }
</style>
```

## PENGATURAN CLEARFIX ELEMENT

Setelah membuat Box Element dengan tag div yang sudah di variasikan, selajutnya yang akan kita lakukan yaitu melakukan Clearfix atau pengaturan lanjutan untuk Box Element yang sebelumnya sudah dilakukan Float Element seperti diatas dengan menambahkan div lainnya setelah Div3 seperti berikut.

```html
<section>
    <div class="div1">Div 1</div>
    <div class="div2">Div 2</div>
    <div class="div3">Div 3</div>
    <div class="div4">Div 4</div>
</section>
```

[menambahkan_gambar](img/DIV%20KE-4.png)

Kemudian untuk mengaturnya menjadi seperti gambar diatas, kalian dapat memasukan kode berikut:

```html
.div4 {
        background-color: rgb(209, 135, 205);
        clear: left;
        float: none;
}
```

## MEMBUAT LAYOUT SEDERHANA

Untuk dapat membuat sebuah Layout Sederhana, langkah awal yang perlu dilakuan ialah membuat sebuah sebuah folder baru yang kemudian didalamnya terdapat sebuah file baru berbasis html dan juga css.

[menambahkan_gambar](img/LAYOUT%20AWAL.png)

Berikut kode yang saya gunakan untuk membuat folder baru tersebut yang nantinya akan nampak seperti gambar diatas.

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Layout Sederhana</title>
    <link rel="stylesheet" href="style.css">
</head>

<header>
    <h1>Layout Sederhana</h1>
</header>
<nav>
    <a href="home.html" class="active">Home</a>
    <a href="artikel.html">Artikel</a>
    <a href="about.html">About</a>
    <a href="kontak.html">Kontak</a>
</nav>
<section id="hero"></section>
<section id="wrapper">
    <section id="main"></section>
    <aside id="sidebar"></aside>
</section>
<footer>
    <p>&copy; 2021 - Universitas Pelita Bangsa</p>
</footer>
    
<body>
    <div id="container">

    </div>
</body>
</html>
```

[menambahkan_gambar](img/LAYOUT%20CSS.png)

Setelahnya, kalian dapat menambahkan kode lainnya pada file CSS untuk dapat membuat layout diatas dengan kode berikut:

```css
/* import google font */
@import
url('https://fonts.googleapis.com/css2?family=Open+Sans:ital,wght@0,300;0,400;0,600;0,700;0,800;1,300;1,400;1,600;1,700;1,800&display=swap');
@import
url('https://fonts.googleapis.com/css2?family=Open+Sans+Condensed:ital,wght@0,300;0,700;1,300&display=swap');

/* Reset CSS */
* {
    margin: 0;
    padding: 0;
}

body {
    line-height:1;
    font-size:100%;
    font-family:'Open Sans', sans-serif;
    color:#7f1616;
}

#container {
    width: 980px;
    margin: 0 auto;
    box-shadow: 0 0 1em #000000;
}

/* header */
    header {
    padding: 20px;
}

header h1 {
    margin: 20px 10px;
    color: #b5b5b5;
}
```

## MEMBUAT NAVIGASI

[menambahkan_gambar](img/NAVIGASI.png)

Untuk dapat melakukan sebuah pengaturan navigasi seperti diatas kalian dapat menambahkan kode berikut pada file CSS sebelumnya.

```css
/* navigasi */
nav {
    display: block;
    background-color: #7c0a41;
}
    
nav a {
    padding: 15px 30px;
    display: inline-block;
    color: #ffffff;
    font-size: 14px;
    text-decoration: none;
    font-weight: bold;
}

nav a.active,
nav a:hover {
    background-color: #933b61;
}
```

## PEMBUATAN HERO PANEL

[menambahkan_gambar](img/HERO%20PANEL.png)

Dalam pembuatan Hero Panel kalian perlu memasukan kode Html dan juga CSS seperti berikut ini:

```html
<section id="hero">
    <h1>Hello World!</h1>
    <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vestibulum lorem
elit, iaculis innisl volutpat, malesuada tincidunt arcu. Proin in leo fringilla,
vestibulum mi porta, faucibus felis. Integer pharetra est nunc, nec pretium nunc
pretium ac.</p>
    <a href="home.html" class="btn btn-large">Learn more &raquo;</a>
</section>
```

```css
/* Hero Panel */
#hero {
    background-color: #d4a7b6;
    padding: 50px 20px;
    margin-bottom: 20px;
}

#hero h1 {
    margin-bottom: 20px;
    font-size: 35px;
}

#hero p {
    margin-bottom: 20px;
    font-size: 18px;
    line-height: 25px;
}
```


## PENGATURAN LAYOUT MAIN DAN SIDEBAR

[menambahkan_gambar](img/MAIN%20AND%20SIDEBAR.png)

 Selanjutnya, melakukan sebuah pengaturan main content dan sidebar seperti diatas, dengan menambahkan kode CSS float berikut ini:

 ```css
 /* main content */
#wrapper {
    margin: 0;
}

#main {
    float:inline-end;
    width: 640px;
    padding: 20px;
}

/* sidebar area */
#sidebar {
    float:left;
    width: 260px;
    padding: 20px;
}
```

## PEMBUATAN SIDEBAR WIDGET

[menambahkan_gambar](img/SIDEBAR%20WIDGET.png)

Tambahkan element lain dalam sidebar dan kemudian tambahkan CSSnya seperti gambar diatas dengan kode berikut:

```html
<aside id="sidebar">
    <div class="widget-box">
        <h3 class="title">Widget Header</h3>
        <ul>
            <li><a href="#">Widget Link</a></li>
            <li><a href="#">Widget Link</a></li>
            <li><a href="#">Widget Link</a></li>
            <li><a href="#">Widget Link</a></li>
            <li><a href="#">Widget Link</a></li>
        </ul>
    </div>
    <div class="widget-box">
        <h3 class="title">Widget Text</h3>
        <p>Vestibulum lorem elit, iaculis in nisl volutpat, malesuada tincidunt
    arcu. Proin in leo fringilla, vestibulum mi porta, faucibus felis. Integer
    pharetra est nunc, nec pretium nunc pretium ac.</p>
    </div>
</aside>
```

```css
/* widget */
.widget-box {
    border:1px solid rgb(0, 0, 0);
    margin-bottom:20px;
}

.widget-box .title {
    padding:10px 16px;
    background-color:#5f1f1f;
    color:rgb(255, 255, 255);
}

.widget-box ul {
    list-style-type:none;
}

.widget-box li {
    border-bottom:1px solid rgb(2, 2, 2);
}

.widget-box li a {
    padding:10px 16px;
    color:rgb(89, 19, 19);
    display:block;
    text-decoration:none;
}

.widget-box li:hover a {
    background-color:rgb(207, 114, 114);
}

.widget-box p {
    padding:15px;
    line-height:25px;
}
```

## PENGATURAN FOOTER

![menambahkan_gambar](img/FOOTER%20SIDEBAR.png)

Gunakan kode berikut ini untuk dapat mendapat hasil seperti itu.

```css
/* footer */
footer {
    clear:both;
    background-color:#1d1d1d;
    padding:20px;
    color:#eee;
}
```

Setelah selesai dengan Footer, selanjutnya menambahakn elemen lainnya pada Main Content dengan menambahkan kode html dan CSS seperti dibawah ini:

```html

# QUESTION AND TASK

1. Buatlah form yang menampilkan dropdown menu dan listbox dengan multiple selection.

![menambahkan_gambar](img/TASK.png)

Untuk dapat membuat tampilan seperti gambar diatas, disini saya menggunaka kode-kode seperti dibawah ini:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>HTML Lanjutan</title>
</head>
<body>
    <header>
        <h1 style="color:rgb(109, 15, 59); text-align:center"> CONCERT TICKET REGISTRATION</h1>
    </header>
</body>
</html>

<form action="proses.php" method="post">
    <fieldset>
        <legend> <h4 style="text-align: center">Data Audience</h4></legend>
    
    
    <p>
    <label for="Name">Name</label>
    <input type="text" id="Name" name="Name">
    </p>


    <p>
    <label for="adress">Adress</label>
    <textarea id="adress" name="adress" cols="50" rows="1"></textarea>
    </p>


    <p>
    <label for="identity number">Identity Number</label>
    <textarea id="identity number" name="identity number" cols="20" rows="1"></textarea>
    </p>


    <p>
        <label>Ages</label>
        <input id="ag_u17" type="radio" name="under 17" value="ag_u17" /><label
        for="ag_u17">Under (-17)</label>
        <input id="ag_ov" type="radio" name="over 17" value="ag_ov" /><label
    
        for="ag_ov">Over (+17)</label>
    </p>
    


<p>
    <!-- Dropdown Menu -->
    <h3>Seat (Dropdown)</h3>
    <label>Choose your Seat</label>
   <select name="Choose your Seat" id="Choose your Seat">
       <option value="Seat">---------Choose Here---------</option>
       <option value="VVIP (Standing 4.500.000)">VVIP (Standing 4.500.000)</option>
       <option value="Red (Standing 3.000.000)">Red (Standing 3.000.000)</option>
       <option value="Purple (Standing 2.000.000)">Purple (Standing 2.000.000)</option>
       <option value="Pink (Standing 1.500.000)">Pink (Standing 1.500.000)</option>
       <option value="Yellow (Standing 1.000.000)">Yellow (Standing 1.000.000)</option>
   </select> 
</p>


<p>
    <label for="Ticket">Ticket</label>
    <textarea id="Ticket" name="Ticket" cols="20" rows="1"></textarea>
    </p>


<p>
    <!-- Dropdown Menu -->
    <h3>Payment (Multiple Selection) </h3>
    <label>Choose your Payment</label>
   <select name="Choose your Payment" id="Choose your Payment">
       <option value="Payment">---------Choose Here---------</option>
       <option value="Bank Transfer">Bank Transfer</option>
       <option value="Credit Card">Credit Card</option>
   </select> 
</p>




<style>
    form p > label {
    display: inline-block;
    width: 100px;
    }
    form input[type="text"], form textarea {
    border: 1px solid #99053e;
    }
    form input[type="submit"] {
    border: 1px solid #940b22;
    background-color: #75163a;
    color: #ffffff;
    font-weight: bold;
    padding: 5px 15px;
    }
</style>

<p><input type="submit" value="Checkout"></p>
</fieldset>
</form>
```

# <P align="center"> THANK'S FOR YOUR ATTENTION!! SEE YOU!!
