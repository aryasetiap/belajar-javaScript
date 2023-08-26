==============================

**VARIABEL VAR**
Variabel `var` adalah salah satu cara untuk mendefinisikan variabel dalam JavaScript. Namun, penting untuk dicatat bahwa `var` memiliki cakupan (scope) yang berbeda dibandingkan dengan `let` dan `const`, yang merupakan cara yang lebih modern untuk mendefinisikan variabel.

Berikut adalah cara menggunakan `var` untuk mendefinisikan variabel:

```javascript
// Mendefinisikan variabel dengan var
var namaVariabel = nilaiVariabel;

// Contoh penggunaan
var angka = 10;
var pesan = "Halo, dunia!";
```

Hal-hal yang perlu diperhatikan tentang `var`:

1. **Function Scope:** Variabel yang didefinisikan dengan `var` memiliki cakupan (scope) fungsi. Artinya, variabel tersebut hanya dapat diakses di dalam fungsi di mana variabel tersebut dideklarasikan.

2. **Hoisting:** Variabel `var` mengalami hoisting, yang berarti deklarasinya akan "dinaikkan" ke atas fungsi atau lingkup tertentu. Ini berarti Anda dapat menggunakan variabel sebelum deklarasi sebenarnya dalam kode Anda. Namun, nilainya akan `undefined` jika Anda mencoba mengaksesnya sebelum deklarasi.

3. **Re-deklarasi:** Anda dapat mengganti nilai variabel `var` atau mendeklarasikannya kembali dalam cakupan yang sama tanpa memicu error.

```javascript
var angka = 5;
var angka = 7; // Ini valid, dan angka sekarang bernilai 7.
```

Karena beberapa masalah cakupan (scope) dan hoisting yang dapat membingungkan, banyak pengembang JavaScript lebih suka menggunakan `let` dan `const` sebagai pengganti `var`. `let` dan `const` memiliki cakupan blok (block scope) dan tidak mengalami hoisting, yang membuat kode lebih mudah dipahami dan meminimalkan kesalahan.

Contoh dengan `let`:

```javascript
// Mendefinisikan variabel dengan let
let namaVariabel = nilaiVariabel;

// Contoh penggunaan
let angka = 10;
```

Contoh dengan `const`:

```javascript
// Mendefinisikan variabel dengan const
const namaVariabel = nilaiVariabel;

// Contoh penggunaan
const pesan = "Halo, dunia!";
```

Secara umum, disarankan untuk lebih memilih `let` dan `const` daripada `var` saat mengembangkan kode JavaScript modern.

==============================

**VARIABEL LET**
Variabel `let` adalah salah satu cara untuk mendefinisikan variabel dalam JavaScript. `let` diperkenalkan dalam ECMAScript 6 (ES6) dan memberikan beberapa perubahan dan perbaikan dibandingkan dengan `var`. Berikut adalah cara menggunakan `let` untuk mendefinisikan variabel:

```javascript
// Mendefinisikan variabel dengan let
let namaVariabel = nilaiVariabel;

// Contoh penggunaan
let angka = 10;
let pesan = "Halo, dunia!";
```

Hal-hal yang perlu diperhatikan tentang `let`:

1. **Block Scope:** Variabel yang didefinisikan dengan `let` memiliki cakupan (scope) blok. Artinya, variabel tersebut hanya dapat diakses di dalam blok kode (misalnya, dalam if statement, loop, atau fungsi) di mana variabel tersebut dideklarasikan.

2. **Tidak Ada Hoisting:** Variabel `let` tidak mengalami hoisting, yang berarti Anda tidak dapat mengaksesnya sebelum deklarasi dalam kode. Ini mengurangi potensi kesalahan yang dapat terjadi.

3. **Tidak Dapat Dire-deklarasikan:** Anda tidak dapat mendeklarasikan ulang (re-declare) variabel yang telah dideklarasikan menggunakan `let` dalam cakupan yang sama. Ini menghindari konflik nama variabel.

```javascript
let angka = 5;
let angka = 7; // Ini akan menyebabkan error, karena variabel angka sudah dideklarasikan sebelumnya.
```

4. **Perbedaan dengan `const`:** Meskipun `let` dan `const` berbagi cakupan blok dan tidak mengalami hoisting, perbedaan utama adalah bahwa variabel `let` dapat diubah nilainya setelah deklarasi, sedangkan variabel `const` nilainya tidak dapat diubah setelah dideklarasikan.

```javascript
let angka = 5;
angka = 7; // Ini valid, nilai angka sekarang menjadi 7.

const nilaiTetap = 10;
nilaiTetap = 15; // Ini akan menyebabkan error, karena const tidak dapat diubah.
```

Variabel `let` sangat berguna dalam membuat kode yang lebih aman dan dapat dipahami, terutama dalam skenario di mana Anda ingin memastikan variabel hanya dapat diakses dalam blok tertentu dan tidak dapat diubah secara tidak sengaja.

==============================

**VARIABEL CONST**
Variabel `const` adalah salah satu cara untuk mendefinisikan variabel dalam JavaScript. `const` juga diperkenalkan dalam ECMAScript 6 (ES6), dan seperti `let`, memiliki cakupan blok (block scope). Namun, perbedaan utama antara `const` dan `let` adalah bahwa variabel yang dideklarasikan dengan `const` harus memiliki nilai awal yang diberikan saat deklarasi, dan nilai variabel tersebut tidak dapat diubah setelah deklarasi. Berikut adalah cara menggunakan `const`:

```javascript
// Mendefinisikan variabel dengan const
const namaVariabel = nilaiVariabel;

// Contoh penggunaan
const pi = 3.14;
const pesan = "Halo, dunia!";
```

Hal-hal yang perlu diperhatikan tentang `const`:

1. **Block Scope:** Variabel yang didefinisikan dengan `const` memiliki cakupan (scope) blok yang sama seperti `let`. Artinya, variabel tersebut hanya dapat diakses di dalam blok kode di mana variabel tersebut dideklarasikan.

2. **Tidak Ada Hoisting:** Variabel `const` juga tidak mengalami hoisting, sehingga Anda harus mendeklarasikannya sebelum menggunakannya.

3. **Nilai Tetap (Immutable):** Variabel `const` harus memiliki nilai awal saat deklarasi, dan setelah itu, nilai variabel tersebut tidak dapat diubah. Ini membuatnya cocok untuk menyimpan nilai-nilai yang tidak boleh berubah.

```javascript
const pi = 3.14;
pi = 3.14159; // Ini akan menyebabkan error, karena const tidak dapat diubah.
```

4. **Konstan Identifier:** Penggunaan `const` sering digunakan untuk mendeklarasikan identifier (nama variabel) yang akan digunakan sebagai konstanta dalam kode Anda. Misalnya, jika Anda ingin menyimpan nilai-nilai seperti konstanta matematika atau URL yang tidak boleh berubah.

```javascript
const JUMLAH_HARI_DALAM_SEMINGGU = 7;
const BASE_URL = "https://contoh.com";
```

5. **Tidak Ada Re-deklarasi:** Anda tidak dapat mendeklarasikan ulang (re-declare) variabel dengan nama yang sama dalam cakupan yang sama menggunakan `const`.

```javascript
const angka = 5;
const angka = 7; // Ini akan menyebabkan error, karena const tidak dapat dideklarasikan ulang.
```

Variabel `const` sangat berguna untuk membuat kode yang lebih aman dan menjaga integritas nilai-nilai konstan dalam aplikasi Anda. Hal ini juga membantu dalam memahami dengan jelas bahwa nilai variabel tersebut tidak akan berubah selama eksekusi program.

==============================

**KATA PENTING**

1. "Mutable" adalah istilah yang digunakan dalam pemrograman untuk menggambarkan jenis objek atau variabel yang dapat diubah setelah dibuat.
2. "Immutable" adalah sebuah konsep dalam pemrograman yang merujuk pada sifat objek atau nilai yang tidak dapat diubah setelah pembuatan.
