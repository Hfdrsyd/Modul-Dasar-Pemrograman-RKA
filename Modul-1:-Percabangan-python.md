## Daftar Isi

- [Control Flow](#control-flow)
- [Percabangan](#percabangan)
    + [If](#percabangan-if)
    + [If-Else](#percabangan-if-else)
    + [If-Else if](#percabangan-if-elseif)
    + [Switch-Case](#percabangan-switch-case)
    + [Operator Kondisional ( ? : )](#operator-kondisional--)
- [Soal Latihan](#soal-latihan)

# Control Flow
Control Flow adalah cara kita mengatur jalan penyataan, instruksi, dan pemanggilan fungsi  suatu program. Tanpa control flow, program kita hanya bergerak dari atas ke bawah saja (**sequential**). Dalam Python, control flow terdiri dari beberapa struktur, termasuk percabangan (**selection**) dan perulangan (**repetition**). Pada modul ini, kita akan fokus pada percabangan terlebih dahulu.

# Percabangan
Percabangan memungkinkan kita untuk menentukan kode manakah yang akan kita eksekusi berdasarkan suatu kondisi. Percabangan di bahasa C ada 4, yaitu `if`, `if-else`, `if-elif`, dan `switch`.

## Percabangan If

Sintaks yang digunakan dalam percabangan menggunakan `if` adalah sebagai berikut.

```python
if <Ekspresi/Kondisi>:
    // Blok Kode yang akan dieksekusi jika kondisi tersebut benar
```

Cara kerja percabangan `if` yaitu memeriksa dan mengevaluasi suatu kondisi untuk menentukan apakah instruksi selanjutnya pada blok kode di dalam _Indentasi_ akan dijalankan atau tidak oleh program.
- Jika kondisi tersebut bernilai **TRUE (1)**, blok kode yang di dalam indentasi akan **dieksekusi**. 
- Sebaliknya jika kondisi tersebut bernilai **FALSE (0)**, blok kode yang di dalam indentasi akan **tidak akan dieksekusi**.

Contoh

Sebagai contoh, di dashboard mobil terdapat indikator bahan bakar yang akan **menyala jika bahan bakar yang tersisa kurang dari level tertentu (misal kurang dari 10 liter)** dengan kondisi “Apakah bahan bakar kurang dari 10 liter?”.

Pada kasus ini terdapat kondisi
- **Jika bahan bakar kurang dari 10 liter** maka nyalakan lampu indikator.

```python
gasoline = 3

# Jika bahan bakar kurang dari 10 liter
if gasoline < 10:
    # Apa yang perlu dilakukan ketika kondisi terpenuhi?
    print("Lampu Indikator menyala!")
```

Output

```
Lampu Indikator menyala!
```

## Percabangan If-Else

Sintaks yang digunakan dalam percabangan menggunakan `if-else` adalah sebagai berikut.

```python
if <Ekspresi/Kondisi>:
    // Blok Kode yang akan dieksekusi jika kondisi tersebut benar
else:
    // Blok Kode yang akan dieksekusi jika kondisi tersebut salah
```

Cara kerja percabangan `if-else` yaitu memeriksa kondisi dalam `if`.
- Jika kondisi tersebut bernilai **TRUE (1)**, Program akan **menjalankan blok kode yang di dalam indentasi `if`**.
- Sebaliknya jika kondisi tersebut bernilai **FALSE (0)**, blok kode di bawah **`else`** lah **yang akan dijalankan**.

Sebagai contoh, kita ingin mencari tahu apakah seseorang absen dari kelas atau tidak. **Apabila ia tidak hadir, maka absensinya akan dicoret (bernilai X)**, dan **apabila hadir, maka absensinya akan di centang (bernilai V)**.

Sehingga dari kasus tersebut, didapat dua alternatif kondisi.
- **Apabila ia hadir, maka muncul V**
- **Apabila ia tidak hadir, maka muncul X**

```python
hadir = True
if hadir: # Jika orang tersebut hadir
    print("V\n")
else:
    print("X\n")
```

Output

```
V

```

## Percabangan If-Elif

Sintaks yang digunakan dalam percabangan menggunakan `if-elif` adalah sebagai berikut.

```python
if <Ekspresi/Kondisi>:
    # Blok Kode yang akan dieksekusi jika kondisi tersebut benar
elif <Ekspresi/Kondisi>:
    # Blok Kode yang akan dieksekusi jika kondisi `if` salah dan kondisi `elif` benar
# Boleh menambahkan else apabila perlu
```

Cara kerja percabangan `if-elif` yaitu memeriksa kondisi dalam `if`.
- Jika kondisi tersebut bernilai **TRUE (1)**, Program akan **menjalankan kode di dalam bracket `if`**.
- Apabila kondisi pertama tidak memenuhi, maka ia akan memerika kondisi didalam `elif`, apabila bernilai **TRUE (1)**, maka ia akan **menjalankan blok kode yang di dalam indentasi tersebut**, apabila tidak maka ia akan menjalankan sequence selanjutnya.
- Apabila kita menyediakan statement else diakhir, maka ketika **seluruh kondisi** `if` dan `elif` tidak memenuhi atau **FALSE (0)**, maka secara otomatis ia akan **menjalankan perintah di dalam `else`** tersebut.

## Percabangan Match-Case

Selain penggunaan statement `if` untuk memilih di antara banyak alternatif, dalam Python versi 3.10 dan seterusnya, terdapat statement `match-case` yang berfungsi untuk memilih di antara banyak alternatif berdasarkan sebuah kondisi. Kondisi pada statemen match berisi ekspresi yang dapat menggunakan sebuah variable tunggal yang akan diperiksa kesamaan nilainya di setiap blok case.

Sintaks dasar untuk `match-case` di Python:

```python
match ekspresi:
    case pola1:
        statement
    case pola2:
        statement
    ...
    case _:
        statement_default
```

- **ekspresi**: Ini adalah nilai atau variabel yang akan diperiksa.
- **pola**: Setiap `case` dapat berisi pola yang akan dicocokkan dengan nilai dari **ekspresi**.
- **_**: Sebuah wildcard yang digunakan untuk menangkap semua nilai lain yang tidak cocok dengan pola sebelumnya, mirip dengan `default` dalam `switch-case`.

Setiap blok `case` dapat berisi satu atau beberapa statement yang akan dieksekusi jika pola cocok dengan nilai dari **ekspresi**. Jika tidak ada pola yang cocok, maka blok kode `case _:` (yang berperan seperti `default`) akan dieksekusi.

### Contoh:

Berikut adalah contoh penggunaan `match-case` dalam Python:

```python
plat_nomor = input("Masukkan huruf awal plat nomor anda: ")
match plat_nomor:
    case 'L':
        print("Surabaya")
    case 'B':
        print("Jakarta")
    case 'D':
        print("Bandung")
    case 'N':
        print("Malang/Lumajang")
    case _:
        print("Karakter plat nomor tidak diketahui")
```

Dalam contoh di atas, **ekspresi** yang digunakan adalah **plat_nomor**, di mana **case-case** nya adalah huruf plat nomor tersebut: `'L'`, `'B'`, `'D'`, `'N'`, dan wildcard `_` untuk menangkap semua karakter lainnya.

### Penjelasan:

- **match plat_nomor:** adalah pernyataan utama yang melakukan pencocokan berdasarkan nilai yang diberikan dalam **plat_nomor**.
- **case 'L':** adalah salah satu kemungkinan nilai yang dapat dicocokkan dengan **plat_nomor**. Jika cocok, maka statement yang terkait akan dieksekusi.
- **case _:** bertindak sebagai penangkap, jika semua `case` tidak ada yang memenuhi.


## Operator Kondisional (` ? : `)

Operator kondisional mempunyai bentuk sintaks sebagai berikut:

```
(ekspresi/kondisi) ? (ekspresi jika TRUE) : (ekspresi jika FALSE);
```

Operator kondisional adalah satu-satunya operator ternary dalam bahasa C. Operator kondisional bertingkah seperti layaknya percabangan `if - else`. Ekspresi/kondisi yang akan dievaluasi diletakkan sebelum tanda tanya (`?`). Apabila menghasilkan **TRUE**, maka program akan mengeksekusi bagian di **kiri** tanda titik dua. Jika **FALSE**, akan mengeksekusi bagian di **kanan** tanda titik dua.

Contoh:

```c
#include <stdio.h>

int main()
{
    int mark;
    
    scanf("%d", &mark);
    printf(mark >= 75 ? "Lulus\n" : "Tidak Lulus\n");
    return 0;
}
```

Program di atas ekuivalen dengan:

```c
#include <stdio.h>

int main()
{
    int mark;
    
    scanf("%d", &mark);
    if (mark >= 75) {
        printf("Lulus\n");
    } else {
        printf("Tidak Lulus\n");
    }
    return 0;
}
```

# Soal Latihan

## Soal 1

Buatlah program yang dapat menentukan apakah suatu input bilangan dari 0 sampai 999 merupakan bilangan Armstrong.

**Sample Input 1**
```
153
```
**Sample Output 1**
```
Merupakan Bilangan Armstrong
```

**Sample Input 2**
```
25
```
**Sample Output 2**
```
Bukan Merupakan Bilangan Armstrong
```

Catatan:
153 merupakan bilangan armstrong karena 153 = 1^3 + 5^3 + 3^3

## Soal 2

Buatlah program yang hanya menerima inputan 0 sampai 999 dan mengeluarkan hasil berupa kalimat terbilang dari angka yang dimasukan.

**Sample Input 1**
```
1
```
**Sample Output 1**
```
Satu
```

**Sample Input 2**
```
11
```
**Sample Output 2**
```
Sebelas
```

**Sample Input 3**
```
979
```
**Sample Output 3**
```
Sembilan ratus tujuh puluh sembilan
```

## Soal 3

A, B, C, D, E, F, G merupakan input sinyal untuk sebuah digit dari 0 sampai 9 seperti berikut.

![seven-segment](https://www.realdigital.org/img/83efb712b75cf12d4a31f4ed93b7b16c.svg)

Buatlah program yang menerima input I1, I2, I3, I4 dan keluarkan output berupa nilai dari ketujuh input sinyal (1 menyala, 0 mati).
(Input I1, I2, I3, I4 bertindak sebagai notasi biner. Contoh 1 0 0 0 bernilai 8)

**Sample Input 1**
```
0 0 0 0
```
**Sample Output 1**
```
1 1 1 1 1 1 0
```

**Sample Input 2**
```
1 0 1 1
```
**Sample Output 2**
```
0 0 0 0 0 0 0
```