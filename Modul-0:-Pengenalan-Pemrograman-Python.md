## Daftar Isi
- [Pengenalan Pemrograman](#apa-itu-pemrograman)

- [IDE (Integrated Development Environment)](#ide-intregated-development-environment)

- [Pengenalan Bahasa Python](#pengenalan-bahasa-python)

    + [Statement](#statement)
    + [Program "Hello, world."](#program-hello-world)
    + [Struktur Program](#struktur-program)
    + [Komentar](#komentar)

- [Keyword dan Identifier](#keyword-dan-identifier)

    + [Keyword](#keyword)
    + [Identifier](#identifier)

- [Variabel](#variabel)

    + [Pengenalan Variabel](#pengenalan-variabel)
    + [Deklarasi dan Pengisian nilai Variabel](#deklarasi-dan-pengisian-nilai-variabel)

- [Konstanta dan Literal](#konstanta-dan-literal)

    + [Konstanta dalam Python](#konstanta-dalam-python)
    + [Literal dalam Python](#literal-dalam-python)

- [Tipe Data Dasar](#tipe-data-dasar)

    + [Tipe data Numerik](#tipe-data-numerik)
    + [Tipe data String](#tipe-data-string)
    + [Casting tipe data dasar](#casting-tipe-data-dasar)

- [Input dan Output Dasar](#input-dan-output-dasar)

    + [Output Dasar](#output-dasar)
    + [Input Dasar](#input-dasar)

- [Operator](#operator)

    + [Operator Assignment](#operator-assignment)
    + [Operator Aritmatika](#operator-aritmatika)
    + [Operator Relasional](#operator-relasional)
    + [Operator Logika](#operator-logika)
    + [Operator Bitwise](#operator-bitwise)
    + [Operator Gabungan](#operator-gabungan)
    + [Operator Lain](#operator-lain)

# Apa itu Pemrograman?
Bayangkan ada Seorang Ibu yang memberikan tugas tertulis di pintu kulkas kepada anaknya Bernama Ani seperti di bawah ini :
```
Buat Ani :

Mamah liburan bentar ya ke Jogja kamu jaga Rumah. 
Setiap 2 Minggu sekali Rumah disapu, Cuci Pakaian deterjennya 2 liter / 1kg baju ya
```
Dari Contoh di atas kita dapat menilai bahwa Ibunya Ani :
- Memberikan perintah kepada Ani untuk melakukan suatu pekerjaan
- Pekerjaan yang dilakukan dapat berulang kali

Dari kasus di atas yang dilakukan Ibu kepada Ani disebut sebagai **pemrograman**. Hanya saja, dalam konteks Mata Kuliah ini Ibu adalah kita / programmer (orang yang menulis program) lalu Ani adalah Komputer.

Secara teknis, **pemrograman** adalah proses menulis dan merancang serangkaian instruksi untuk mengarahkan komputer dalam menjalankan tugas-tugas tertentu. Di sisi lain, komputer tidak mengerti bahasa manusia, sehingga untuk memberikan perintah kepada komputer, kita harus menuliskannya dalam bahasa pemrograman. Proses penulisan perintah tersebut disebut **coding/pengkodean**. Pada modul ini dan kedepan, kalian akan belajar mengenai dasar pemrograman menggunakan Bahasa Pemrograman Python.

# IDE (Integrated Development Environment)

Sebelum memulai menulis kode (atau *ngoding*), kita membutuhkan IDE untuk menyederhanakan proses pengkodean. Apa itu IDE? Sederhananya, IDE atau Intregated Development Environment adalah aplikasi editor kode. Berikut ini adalah daftar aplikasi IDE yang dapat digunakan pada bahasa python:

- [Visual Studio Code (VS Code)](https://code.visualstudio.com/)
- [PyCharm](https://www.jetbrains.com/pycharm/download/)

Python menggunakan interpreter untuk menjalankan kode, interpreter adalah program yang menjalankan kode Python secara langsung dengan cara membaca kode sumber Python (file .py) baris demi baris, menerjemahkannya menjadi bytecode, dan langsung mengeksekusinya. Berikut adalah tautan untuk mendownload interpreter Python:

- [Python](https://www.python.org/)

Setelah melakukan install interpreter, untuk mengecek versi dari python dan mengecek apakah python sudah aktif, dapat dicoba menggunakan command seperti dibawah, menggunakan **command prompt**.

```
C:\Users>python --version
Python 3.11.3

C:\Users>python
Python 3.11.3 (tags/v3.11.3:f3909b8, Apr  4 2023, 23:49:59) [MSC v.1934 64 bit (AMD64)] on win32
Type "help", "copyright", "credits" or "license" for more information.
>>> print("Hello World")
Hello World
>>>
```

Atau dengan mudah, kalian dapat mencoba - coba run kode python menggunakan **Google Colaboratory** (untuk sekarang, hanya disarankan sebagai platform mencoba coba). Berikut cara menggunakan Google Colaboratory, jika kalian Pertama kali menggunakan:
- Buka Google Drive kalian pada [https://drive.google.com/drive/home](https://drive.google.com/drive/home)
- Kemudian Tekan **`+ Baru`**, **`Lainnya`**, **`Hubungkan Aplikasi Lainnya`**.(Tombol akan berbeda jika menggunakan bahasa lain, sesuaikan saja)
- Kemudian telusuri `Colaboratory` dan install.
- Setelah Google Colab Terinstall kalian dapat menggunakannya melalui **`+ Baru`**, **`Lainnya`**, **`Colaboratory`**, dan Google Colab siap digunakan.

**Note :** kalian tetap disarankan menggunakan IDE + interpreter, selama mata kuliah ini. Karena Google Colab menghasilkan file .ipynb bukan .py.
# Pengenalan Bahasa Python

## Statement

Dalam suatu program, sebuah **statement** atau pernyataan adalah intruksi/perintah yang mempunyai makna tertentu sehingga menyebabkan program tersebut dapat melakukan suatu tindakan.

Analoginya, untuk berbicara kepada seseorang, kita menggunakan bahasa tertentu yang dapat dimengerti, sehingga kita dapat menyampaikan apa yang ingin disampaikan. Nah, seperti itulah statement. Apa yang kita sampaikan kepada orang lain layaknya statement pada program yang kita sampaikan kepada komputer.

## Program "Hello, world."

Mari kita mulai dengan membuat program sederhana, yakni program untuk menampilkan kalimat **“Hello, world!”** pada layar (konsol). Berikut adalah kode program tersebut.

```python
print("Hello, world!\n")
```

Salinlah kode di atas pada IDE, kemudian run kode dengan `python <nama_file_python.py>`. Proses running akan menghasilkan output sebagai berikut.

```
Hello, world!
```

## Struktur Program

Python merupakan bahasa pemrograman yang sangat sederhana dan mudah dipahami. Struktur program Python dirancang untuk memudahkan penulisan dan pemahaman kode. Berikut adalah beberapa poin penting mengenai struktur program Python: 

1. **Baris Perintah**:
Python adalah bahasa yang berbasis baris perintah. Ini berarti bahwa setiap baris kode biasanya mewakili satu perintah atau statement. Python akan menjalankan perintah tersebut secara berurutan, dari atas ke bawah.

2. **Indentasi**:
    Struktur blok kode dalam Python ditentukan oleh indentasi. Berbeda dengan banyak bahasa pemrograman lain yang menggunakan tanda kurung {} atau keyword khusus untuk menandai blok kode, Python menggunakan indentasi (spasi atau tab) untuk mengelompokkan baris-baris kode yang terkait.

    Indentasi yang konsisten sangat penting dalam Python, karena Python menggunakan indentasi untuk menentukan batasan blok kode seperti fungsi, kondisi, dan loop. Jika indentasi tidak konsisten, Python akan menghasilkan kesalahan (error) yang menjelaskan bahwa ada masalah dengan struktur kode. Berikut contoh penggunaan indentasi pada pada code:
    ```python
    if <Ekspresi/Kondisi>:
        # Kode yang akan dieksekusi jika kondisi tersebut benar
    ```

## Komentar

**Komentar** (_comment_) adalah bagian dari program yang tidak akan dieksekusi. Komentar sangat berguna untuk mendeskripsikan program yang dibuat, misalnya saja untuk menjelaskan bagian dari kode agar mudah dipahami oleh programmer lainnya. Terdapat dua jenis komentar dalam bahasa Python.

### Komentar Single-Line

Seperti namanya, komentar single-line hanya bekerja pada satu baris. Komentar single-line diawali dengan simbol `#` . Semua karakter (pada satu baris) dibelakang simbol `#` akan diabaikan.

```python
# Ini adalah komentar single-line  
  
# Fungsi untuk mencetak ke layar  
print("HALO\n");  

```

### Komentar Multi-Line

Sedangkan komentar multi-line dapat bekerja pada lebih dari satu baris. Pasangan simbol `'''` atau `"""` digunakan untuk membuat komentar multi-line. Semua karakter yang berada di antara dua simbol tersebut akan diabaikan.

```python
'''
Ini adalah komentar multi-line 
Semua yang berada di sini akan 
diabaikan 
''' 
```
Atau kita dapat membuat dengan komentar *Single-Line* yang berulang.

```python
# Ini adalah komentar multi-line 
# Semua yang berada di sini akan 
# diabaikan 
```
**Tips** : pada IDE kita dapat menambahkan/menghapus komentar *Multi-Line* dengan mem-blok semua baris yang akan dicomment dan menekan `ctrl` atau `command` + `/`

[< Kembali ke Daftar Isi](#daftar-isi)


# Keyword dan Identifier

## Keyword

**Keyword** merupakan kata khusus yang telah dipesan (reserved) pada bahasa pemograman. Kata-kata ini digunakan untuk menentukan sintaks dan struktur program, dan tidak dapat digunakan sebagai nama identifier. Berikut adalah daftar keyword dalam Python:

| Keyword   | Keyword   | Keyword   | Keyword   |
|-----------|-----------|-----------|-----------|
| `False`   | `await`   | `else`    | `import`  |
| `None`    | `break`   | `except`  | `in`      |
| `True`    | `class`   | `finally` | `is`      |
| `and`     | `continue`| `for`     | `lambda`  |
| `assert`  | `def`     | `from`    | `nonlocal`|
| `async`   | `del`     | `global`  | `not`     |
| `if`      | `raise`   | `return`  | `while`   |
| `elif`    | `try`     | `with`    | `yield`   |
| `or`      | `pass`    | `print`   | `exec`    |

## Identifier

**Identifier** adalah nama yang digunakan untuk merujuk pada entitas dalam kode, seperti variabel, fungsi, kelas, dan objek. Di Python, aturan penamaan identifier adalah sebagai berikut:

1. **Tidak Boleh Menjadi Keyword**:
   - Nama identifier tidak boleh sama dengan keyword Python yang telah ditentukan.

2. **Karakter yang Diperbolehkan**:
   - Identifier hanya boleh terdiri dari huruf (baik huruf besar maupun kecil), digit, dan simbol underscore (`_`).

3. **Tidak Boleh Mengandung Whitespace**:
   - Identifier tidak boleh mengandung spasi atau karakter whitespace lainnya.

4. **Harus Dimulai dengan Huruf atau Underscore**:
   - Identifier harus dimulai dengan huruf atau simbol underscore, dan tidak boleh dimulai dengan digit. Misalnya, `variable_name` atau `_variable`.

5. **Case-Sensitive**:
   - Python bersifat case-sensitive, artinya `variable`, `Variable`, dan `VARIABLE` dianggap sebagai identifier yang berbeda.


[< Kembali ke Daftar Isi](#daftar-isi)

# Variabel

## Pengenalan Variabel

**Variabel** adalah suatu tempat yang digunakan untuk menampung data atau nilai pada memori yang mempunyai nilai yang dapat berubah–ubah selama proses program. Dalam bahasa Python, kita tidak perlu mendeklarasikan tipe data terlebih dahulu seperti pada bahasa lain(C, Java, etc), karena Python adalah bahasa yang dinamis.

Sebagai analogi, variabel adalah seperti wadah yang bisa menampung apa saja, dan isi wadah tersebut bisa berupa angka, teks, atau objek lainnya.

## Deklarasi dan Pengisian nilai Variabel

Pada bahasa Python, deklarasi dan pengisian nilai pada variabel dilakukan sekaligus tanpa harus menentukan tipe datanya secara eksplisit. Anda cukup menuliskan nama variabel, kemudian memberikan nilai menggunakan operator assignment (=).

```python
x = 10
y = 'P'
```
Pada contoh di atas:
- Variabel x menyimpan nilai `10`.
- Variabel y menyimpan nilai `'P'`.

Python secara otomatis akan mengenali tipe data berdasarkan nilai yang diberikan. Misalnya, `x` akan dianggap sebagai `int` (integer) karena nilainya berupa bilangan bulat, dan `y` akan dianggap sebagai `string` karena nilainya merupakan teks, meskipun hanya terdiri dari satu karakter.

```python
x = 10
y = 'P'

print(type(x))
print(type(y))
```
Jalankan kode diatas untuk mengetahui tipe data dari variabel, akan diperoleh output sebagai berikut:
```
<class 'int'>
<class 'str'>
```

[< Kembali ke Daftar Isi](#daftar-isi)

# Konstanta dan Literal

## Konstanta dalam Python

**Konstanta** adalah variabel yang nilainya tidak dapat diubah selama program berjalan. Meskipun Python tidak memiliki konstanta bawaan seperti beberapa bahasa pemrograman lain, kita dapat mendefinisikan konstanta dengan menggunakan **konvensi/kesepakatan penamaan huruf kapital**.

### Aturan dalam Mendeklarasikan Konstanta:
- Gunakan huruf besar (UPPERCASE) untuk mendefinisikan konstanta. Misalnya: `PI = 3.14`.
- Nama konstanta tidak boleh dimulai dengan angka.
- Gunakan kombinasi huruf, angka, dan underscore (_), tetapi hindari karakter khusus lainnya.

### Contoh:
```python
PI = 3.14
GRAVITY = 9.8
```

## Literal dalam Python

**Literal** adalah data yang ditulis secara langsung dalam kode program. Python mendukung beberapa jenis literal:

### 1. Literal Numerik

Literal numerik adalah nilai numerik yang tidak dapat diubah, dan dibagi menjadi tiga kategori:

- **Integer**: Bilangan bulat. Contoh: `a = 30`
- **Float**: Bilangan desimal. Contoh: `b = 40.67`
- **Kompleks**: Bilangan kompleks. Contoh: `c = 10+4j`

```python
# Contoh literal numerik
a = 30
b = 40.67
c = 10 + 4j

print(a)
print(b) 
print(c)  
```
Output :
```
30
40.67
(10+4j)
```

### 2. Literal String

Literal string adalah kumpulan karakter yang dikelilingi oleh tanda kutip. String dapat ditulis menggunakan tanda kutip tunggal, ganda, atau triple (untuk multi-baris).
```python
string = 'Hello World'
multi_line = '''Hello,
World!'''
char = 'A'

print(string) 
print(multi_line)
print(char)
```
Output:
```
Hello World
Hello,
World!
A
```
**Note :** Sebenarnya Multi-Line Comment pada pembahasan sebelumnya merupakan literal string yang tidak di-assign ke variable apapun, sehingga python akan mengabaikannya.

Selain karakter normal, terdapat karakter khusus dalam bahasa python yang mempunyai fungsi-fungsi khusus atau karakter yang tidak bisa begitu saja dituliskan dengan bentuk aslinya. Misalnya, “new line” direpresentasikan dengan ‘\n’ atau simbol backslash direpresentasikan dengan ‘\’. Karakter-karakter tersebut disebut dengan escape sequence.

| Escape Sequence | Karakter            |
|-----------------|---------------------|
| `\b`            | Backspace           |
| `\f`            | Form feed           |
| `\n`            | Newline             |
| `\r`            | Return              |
| `\t`            | Tab horisontal      |
| `\v`            | Tab vertikal        |
| `\\`            | Backslash           |
| `\'`            | Tanda petik         |
| `\"`            | Tanda petik dua     |


Dapat dicoba dengan kode berikut
```python
print("Hello\b World")  # Output: Hell World (menghapus satu karakter sebelum '\b')

print("Hello\fWorld")  # Output: HelloWorld (melanjutkan setelah Form Feed)

print("Hello\nWorld")  # Output: Hello
                       #         World

print("Hello\rWorld")  # Output: World (mengganti bagian sebelum '\r' dengan yang setelahnya)

print("Hello\tWorld")  # Output: Hello   World (menambahkan tab horizontal)

print("Hello\vWorld")  # Output: HelloVertical TabWorld (menambahkan tab vertikal)

print("Hello\\World")  # Output: Hello\World

print('It\'s a beautiful day')  # Output: It's a beautiful day

print("He said, \"Hello!\"")  # Output: He said, "Hello!"
```
### 3. Literal Boolean

Literal boolean hanya memiliki dua nilai: `True` dan `False`, di mana `True` dianggap sebagai 1 dan `False` dianggap sebagai 0.

```python
boolean1 = True
boolean2 = False
```

### 4. Literal Khusus 
Python juga menyediakan literal khusus yang disebut **None**, yang digunakan untuk menunjukkan bahwa suatu variabel belum memiliki nilai. 

```python
LiteralKhusus = None
```

[< Kembali ke Daftar Isi](#daftar-isi)

# Tipe Data Dasar

## Tipe data **Numerik**
Tipe data Numerik digunakan untuk merepresentasikan bilangan (baik bulat maupun pecahan). Bahasa Python menyediakan empat tipe numerik yang berbeda:
- `int` (signed integer): Tipe data untuk bilangan bulat, baik positif maupun negatif. Tidak ada batasan ukuran memori yang tetap untuk int di Python, karena Python secara otomatis menangani besar kecilnya nilai integer.
- `float` (nilai pecahan floating point): Tipe data untuk bilangan real dengan nilai pecahan. Float menyediakan jangkauan nilai kurang lebih &plusmn;1.7 x 10<sup>&plusmn;308</sup>.
- `complex` (bilangan kompleks): Tipe data untuk bilangan yang memiliki bagian riil dan imajiner.

```python
a=15000000
print("Tipe data", a, " adalah ", type(a))

b=20.846
print("Tipe data", b, " adalah ", type(b))

c=i+3j
print("Tipe data", c, " adalah ", type(c))
```
Output:
```
Tipe data 15000000  adalah  <class 'int'>
Tipe data 20.846  adalah  <class 'float'>
Tipe data (1+3j)  adalah  <class 'complex'>
```

## Tipe data **String**
Tipe data **String** merupakan Tipe data untuk merepresentasikan teks atau karakter. String bisa berupa satu karakter atau rangkaian karakter. String dapat ditulis menggunakan tanda kutip tunggal, ganda, atau triple (untuk multi-baris). String juga dapat diperlakukan seperti `list` dari karakter yang tidak bisa diubah (list akan dibahas lebih detail pada modul kedepan).

penggunaanya silahkan buka [Literal String](#2-literal-string)

## Tipe data **Boolean**
Tipe data Boolean merupakan tipe data yang hanya memiliki 2 nilai, **`True`** atau **`False`**. 

## Casting tipe data dasar
Casting merupakan proses konversi dari satu tipe data ke tipe data lain. Biasanya dibutuhkan dengan tujuan kompabilitas, konsistensi, maupun fleksibilitas. Pada python casting dilakukan menggunakan fungsi built-in dari python, seperti `int()`, `float()`, `complex()`, `str()`. Berikut contoh penggunaan casting:

```python
# int()
x = 10.75
y = int(x)
print(y)  # Output: 10, akan ditaksir ke bilangan bulat terbesar yang lebih kecil dari x
z = "123"
w = int(z)
print(w)  # Output: 123

# float()
a = 5
b = float(a)
print(b)  # Output: 5.0
c = "3.14"
d = float(c)
print(d)  # Output: 3.14

# str()
e = 42
f = str(e)
print(f,type(f))  # Output: '42'
g = 3.14
h = str(g)
print(h,type(h))  # Output: '3.14'

# bool() akan menganggap jika variable memiliki value/isi adalah True
i = 42
j = bool(i)
print(j)  # Output: True
k = 0
l = bool(k)
print(l)  # Output: False
M = ''
N = bool(M)
print(N)  # Output: False

```
Output:
```
10
123
5.0
3.14
42 <class 'str'>
3.14 <class 'str'>
```

**Note :** Kita juga dapat melakukan casting pada tipe data collection pada modul kedepan.

[< Kembali ke Daftar Isi](#daftar-isi)

# Input dan Output Dasar

Program yang kita buat dapat dijadikan program yang interaktif. Kita dapat menginstruksikannya untuk menerima input (dari keyboard) lalu menampilkan hasil output (pada konsol layar).

## Output Dasar

### Fungsi `print()`

Untuk mencetak output pada konsol di Python, kita menggunakan fungsi print(). Fungsi ini dapat menerima string sebagai argumen.

```python
print("Ini adalah sebuah string")
```

Output

```
Ini adalah sebuah string
```
Secara default, fungsi print akan menulis isinya ke baris baru/new-line(\n).
```python
print("ini baris 1")
print("ini baris 2")
```

Output:

```python
ini baris 1
ini baris 2
```
Apabila kita tidak menginginkan output pada baris baru, kita dapat merubah karakter terakhir dari print dengan menggunakan parameter `end=`.
```python
print("ini baris 1",end=' ') # karakter akhir dari print diubah menjadi ' '
print("ini baris 2")
```
Output:
```
ini baris 1 ini baris 2
```
Kita juga dapat menambahkan escape sequence pada string. Misalkan, kita ubah statement `print()` di atas menjadi:

```python
print("Ini adalah sebuah string\nAku adalah new-line\n\tAku adalah karakter \\tab")
```  
 
```
Ini adalah sebuah string
Aku adalah new-line
    Aku adalah karakter \tab
```

Potongan-potongan kode di atas adalah contoh untuk mencetak string tetap. Lalu bagaimana jika kita ingin mencetak string bersama dengan nilai dari suatu variabel?


### Output Dengan Format Specifier

Untuk mencetak nilai dari suatu variabel, kita dapat menggunakan format string dalam fungsi print(). Di Python, kita menggunakan format string atau f-string untuk memasukkan nilai variabel ke dalam string.

Misalnya saja, kita mempunyai dua variabel bertipe int dan str yakni a = 2 dan b = 'X'. Kita hendak mencetak nilai dari a dan b, maka banyak cara yang dapat dilakukan, sebagai berikut:

```python
a = 2
b = 'X'

print(f"nilai a adalah {a}, nilai b adalah {b}")
print("nilai a adalah {}, nilai b adalah {}".format(a,b))
print("nilai a adalah " + str(a) + ", nilai b adalah " + str(b)) # penggabungan string
print("nilai a adalah", a, ", nilai b adalah", b) # multiple argument
```

Output:

```
nilai a adalah 2, nilai b adalah X
nilai a adalah 2, nilai b adalah X
nilai a adalah 2, nilai b adalah X
nilai a adalah 2 nilai b adalah X
```
Semua metode `print()` menghasilkan output yang sama, kecuali metode multiple argument. Hal ini disebabkan karena ketika variabel dimasukkan sebagai argumen dalam `print()`, Python secara otomatis menambahkan spasi di antara argumen-argumennya. Oleh karena itu, **pilihlah salah satu metode untuk output yang paling sesuai dengan kebutuhan Kalian**.

## Input Dasar

### Fungsi `input()`

Untuk menerima data atau nilai dari pengguna dalam Python, kita menggunakan fungsi `input()`. Fungsi ini membaca data dari keyboard hingga *new-line* (*enter*) dan mengembalikannya sebagai **string**. Jika ingin memanfaatkan nilai dari fungsi `input()` maka perlu dilakukan *casting* maupun manipulasi dari string.
```python
# Mengambil input kemudian dicasting menjadi integer
n = int(input("Masukkan sebuah bilangan bulat: "))

print(f"n mempunyai nilai = {n}")
```
Tampilan konsol:
```
Masukkan sebuah bilangan bulat: 21
n mempunyai nilai = 21
```

Kemudian, bagaimana cara menerima lebih dari 1 input pada baris yang sama? apabila fungsi `input()` akan membaca hingga *new-line*?

### Fungsi `input()` dengan manipulasi string
Untuk mengatasi masalah tersebut kita perlu melakukan manipulasi string yang diperoleh dari hasil `input()`. Manipulasi tersebut dengan menggunakan fungsi `split()`, yakni fungsi untuk memisah string berdasarkan suatu karakter tertentu. (Fungsi - fungsi dari string yang lain akan dijelaskan lebih detail pada modul kedepan). Berikut adalah contoh apabila program menerima tiga input pada satu baris:

```python
# Mengambil input kemudian dipisah dengan karakter spasi ' ' dan dicasting ke integer
a, b, c = input().split(' ') # a, b, c masih dalam bentuk string
a = int(a)
b = int(b)
c = int(c)
# line-line diatas dapat diubah dengan satu line dibawah.
# a, b, c = map(int,input().split(' '))
# fungsi map() digunakan untuk menjalankan fungsi `int()` ke setiap bagian input().split(' ')
print(f"a b c mempunyai nilai = {a}, {b}, {c}")
```
Tampilan konsol:
```
21 12 50
a b c mempunyai nilai = 21, 12, 50
```

Dari kode tersebut kita sudah bisa memasukkan tiga input dalam satu baris, dengan dimasukkan pada 3 variabel. Bagaimana bila jumlah input dalam baris dinamis/berubah ubah? 
Hal tersebut dapat diatasi dengan memanfaatkan **perulangan dan list** pada modul kedepan.

[< Kembali ke Daftar Isi](#daftar-isi)

# Operator

**Operator** dalam Python dapat dipahami sebagai sesuatu yang digunakan untuk melakukan operasi pada operan (variabel/nilai). Misalnya, operator `+` digunakan untuk operasi penjumlahan.

Berdasarkan jumlah operannya, operator dibagi menjadi tiga jenis, yaitu:

- **Unary** – yaitu operator yang bekerja pada satu operan, misalnya `-5`.
- **Binary** – yaitu operator yang bekerja pada dua operan, misalnya `2 + 3`.
- **Ternary** – yaitu operator yang bekerja pada tiga operan. (Operator kondisional pada modul selanjutnya).

Berdasarkan kegunaannya, berikut adalah jenis-jenis operator dalam bahasa Python.

## Operator Assignment

**Operator Assignment** digunakan untuk menetapkan nilai ke variabel. Simbol yang digunakan adalah `=`.

Contoh:

```python
x = 4
y = 3
x = x + y  # x = 7
y = x + x  # y = 14
```

## Operator Aritmatika

**Operator Aritmatika** digunakan untuk melakukan operasi matematika dasar seperti penjumlahan, pengurangan, dan sebagainya.

| Simbol | Operasi                                               | Contoh    |
|:------:| ----------------------------------------------------- | :-------: |
| +      | Penjumlahan pada dua operan                           | `a + b`   |
| -      | Pengurangan pada dua operan                           | `a - b`   |
| *      | Perkalian pada dua operan                             | `a * b`   |
| /      | Pembagian pada dua operan                             | `a / b`   |
| %      | Modulo (sisa pembagian)                               | `a % b`   |
| **     | Eksponensial (pangkat)                                | `a ** b`  |
| //     | Pembagian bulat ke bawah (floor division)             | `a // b`  |

## Operator Relasional

**Operator Relasional** digunakan untuk memeriksa relasi dan membandingkan nilai dari dua operan. Jika benar akan menghasilkan nilai **TRUE** (direpresentasikan angka 1), jika salah maka akan menghasilkan nilai **FALSE** (direpresentasikan angka 0).

Berikut adalah operator relasional dalam bahasa *python*.

| Operator | Simbol   | Keterangan                                                                                         | Contoh                                        |
| -------- | :------: | -------------------------------------------------------------------------------------------------- | --------------------------------------------- |
| Sama dengan           | ==     | Memeriksa apakah dua operan sama nilainya.                                              | `5 == 2` (False)<br>`5 == 5` (True)           |
| Tidak Sama dengan     | !=     | Memeriksa apakah dua operan berbeda nilainya.                                           | `5 != 2` (True)<br>`5 != 5` (False)           |
| Lebih besar           | >      | Memeriksa apakah operan pertama lebih besar dari yang kedua.                            | `5 > 2` (True)<br>`5 > 5` (False)             |
| Lebih kecil           | <      | Memeriksa apakah operan pertama lebih kecil dari yang kedua.                            | `5 < 2` (False)<br>`5 < 5` (False)<br>`2 < 4` (True)|
| Lebih besar sama dengan | >=   | Memeriksa apakah operan pertama lebih besar atau sama dengan yang kedua.                | `5 >= 2` (True)<br>`5 >= 5` (True)            |
| Lebih kecil sama dengan | <=   | Memeriksa apakah operan pertama lebih kecil atau sama dengan yang kedua.                | `5 <= 2` (False)<br>`5 <= 5` (True)           |
## Operator Logika

**Operator Logika** digunakan untuk melakukan tes pada kondisi/ekspresi, apakah kondisi tersebut benar atau salah. Operator logika hanya akan menghasilkan nilai **TRUE** (jika benar) atau **FALSE** (jika salah). TRUE direpresentasikan oleh angka 1, sedangkan FALSE oleh angka 0.

Operator-operator logika dalam bahasa *python* adalah sebagai berikut.

| Operator | Simbol | Keterangan                                                                                              | Contoh                               |
| -------- |:------:| ------------------------------------------------------------------------------------------------------- | ------------------------------------ |
| Logical NOT       | `not`  | Membalikkan nilai kebenaran kondisi.                                                          | `not True` (False)<br>`not False` (True)|
| Logical AND       | `and`  | Menghasilkan `True` jika kedua operan bernilai `True`.                                        | `True and True` (True)<br>`True and False` (False)|
| Logical OR        | `or`   | Menghasilkan `True` jika salah satu operan bernilai `True`.                                   | `True or False` (True)<br>`False or False` (False)|

> Operator Logika **NOT** merupakan operator unary yang artinya hanya pada bekerja pada satu operan

Operator logika pada umumnya digunakan bersamaan dengan operator relasional untuk melakukan tes pada ekspresi yang berhubungan dengan kebenaran suatu kondisi. Penggunaan paling umum adalah untuk melakukan percabangan (akan dipelajari di bagian selanjutnya).

Contoh:

```c
int a, b, c, d;  
a = 11;  
b = 24;  
c = 11;  
d = ((a == c) && (b > a));               // 1 (TRUE)  
d = ((a >= b) || (a < c));               // 0 (FALSE)  
d = ((b != b) || (b > c)) && (c == a);   // 1 (TRUE) 
```

## Operator Bitwise

**Operator Bitwise**, seperti namanya digunakan untuk melakukan operasi pada dua operan dalam skala biner (bilangan basis 2). Sebelum mempelajari lebih lanjut cara kerja operasi bitwise, sebaiknya kamu harus paham terlebih dahulu mengenai bilangan dalam basis biner.

Terdapat 6 jenis operator bitwise, yakni **AND**, **OR**, **XOR**, **COMPELEMENT**, **SHIFT LEFT**, dan **SHIFT RIGHT**. Untuk lebih memahami perbedaan cara kerja operator bitwise, perhatikan tabel berikut.
| Operator | Simbol | Keterangan                                                                                                                              |
| -------- | :----: | --------------------------------------------------------------------------------------------------------------------------------------- |
| Bitwise AND       | &      | Melakukan operasi AND pada tiap bit.                                                                                         |
| Bitwise OR        | \|     | Melakukan operasi OR pada tiap bit.                                                                                          |
| Bitwise XOR       | ^      | Melakukan operasi XOR pada tiap bit.                                                                                         |
| Bitwise NOT       | ~      | Membalikkan tiap bit dari 1 ke 0 dan sebaliknya.                                                                              |
| Shift Left        | <<     | Menggeser bit ke kiri sebanyak n posisi.                                                                                      |
| Shift Right       | >>     | Menggeser bit ke kanan sebanyak n posisi.                                                                                     |


**Contoh penggunaan operator bitwise:**

Misal 12 dan 5. Representasi 12 dan 5 dalam basis biner adalah 12 = (1100) dan 5 = (0101). Maka, operasi bitwise adalah sebagai berikut.

+ **Bitwise AND**

    ```
    12 = (1100)
     5 = (0101)
    ------------ &
     4 = (0100)
    ```

+ **Bitwise OR**

    ```
    12 = (1100)
     5 = (0101)
    ------------ | 
    13 = (1101)
    ```

+ **Bitwise XOR**

    ```
    12 = (1100)
     5 = (0101)
    ------------ ^
     9 = (1001)
    ```

+ **Bitwise COMPLEMENT**

    ```
     12 = (1100)
    ~12 = (0011)
    ```

+ **Bitwise SHIFT LEFT**

    Misal kita hendak menggeser bit bilangan 13 ke kiri sebanyak 2, maka 13 << 2.

    ```
         13 = (001101)
    13 << 2 = (110100) 
    ```

    Bisa diperhatikan, bit paling kanan setelah digeser akan diisi oleh 0. Maka hasil dari 13 << 2 = 52.

+ **Bitwise SHIFT RIGHT**

    Misal kita hendak menggeser bit bilangan 13 ke kanan sebanyak 2, maka 13 >> 2.

    ```
         13 = (001101)
    13 >> 2 = (000011)
    ```

    Bisa diperhatikan, bit paling kiri setelah digeser akan diisi oleh 0. Maka hasil dari 13 >> 2 = 3.

## Operator Gabungan

**Operator Gabungan** adalah operator yang terdiri dari gabungan dua operator. Tujuan dari operator gabungan adalah untuk mempersingkat penulisan kode. Berikut adalah operator gabungan dalam bahasa python.

| Operator | Contoh    | Ekuivalen Dengan        |
| :------: | :-------: | :---------------------: |
| +=       | `a += b`  | `a = a + b`             |
| -=       | `a -= b`  | `a = a - b`             |
| *=       | `a *= b`  | `a = a * b`             |
| /=       | `a /= b`  | `a = a / b`             |
| %=       | `a %= b`  | `a = a % b`             |
| **=      | `a **= b` | `a = a ** b`            |
| //=      | `a //= b` | `a = a // b`            |
| &=       | `a &= b`  | `a = a & b`             |
| \|=      | `a \|= b` | `a = a \| b`            |
| ^=       | `a ^= b`  | `a = a ^ b`             |
| >>=      | `a >>= b` | `a = a >> b`            |
| <<=      | `a <<= b` | `a = a << b`            |

## Operator Lain

Selain operator-operator yang telah dijelaskan sebelumnya, terdapat beberapa operator lain yang terdapat pada bahasa python. Berikut penjelasannya.

### Operator Koma (`,`)

Koma dalam Python digunakan sebagai separator untuk memisahkan elemen dalam tuple, list, dan argument pada fungsi. Tidak digunakan sebagai operator.

```python
a, b, c = 1, 2, 3  # Multiple assignment
```

### Operator Subscript (`[]`)

Operator ini biasa digunakan untuk mengakses elemen dalam list, tuple, atau string.

_Operator lain yang belum ter-cover pada modul ini akan dibahas pada modul-modul selanjutnya._

[< Kembali ke Daftar Isi](#daftar-isi)

Referensi
- https://github.com/AlproITS/DasarPemrograman/wiki/Modul-0:-Pengenalan-Pemrograman
- https://www.toppr.com/guides/python/python-introduction/variables-constants-literals/python-variables-constants-and-literals/
- https://www.scholarhat.com/tutorial/python/data-types-in-python
- https://www.geeksforgeeks.org/python-bitwise-operators/

