**VARIABEL SCOPE**

**BLOK**
Variabel dengan cakupan (scope) blok adalah variabel yang hanya dapat diakses di dalam blok kode tertentu di mana variabel tersebut dideklarasikan. Cakupan blok ini biasanya terkait dengan penggunaan kata kunci `let` dan `const` dalam JavaScript, yang mengenalkan cakupan blok yang lebih ketat dibandingkan dengan kata kunci `var`.

Berikut adalah contoh penggunaan variabel dengan cakupan blok menggunakan `let`:

```javascript
function contohScope() {
  if (true) {
    let angka = 5; // Variabel angka hanya dapat diakses di dalam blok if ini
    console.log(angka); // Output: 5
  }

  // Diluar blok if, variabel angka tidak dapat diakses
  console.log(angka); // Ini akan menyebabkan error
}

contohScope();
```

Dalam contoh di atas, variabel `angka` dideklarasikan dengan kata kunci `let` di dalam blok `if`. Oleh karena itu, variabel `angka` hanya dapat diakses di dalam blok `if`. Di luar blok tersebut, variabel `angka` tidak dapat diakses.

Ini sangat berguna dalam mengisolasi variabel agar hanya dapat digunakan dalam konteks tertentu dan untuk mencegah polusi nama (namespace pollution) di dalam kode Anda.

Contoh penggunaan variabel dengan cakupan blok menggunakan `const`:

```javascript
function contohScope() {
  if (true) {
    const pesan = "Halo, dunia!"; // Variabel pesan hanya dapat diakses di dalam blok if ini
    console.log(pesan); // Output: "Halo, dunia!"
  }

  // Diluar blok if, variabel pesan tidak dapat diakses
  console.log(pesan); // Ini akan menyebabkan error
}

contohScope();
```

Prinsipnya sama dengan penggunaan `let`, tetapi dengan `const`, Anda juga menunjukkan bahwa nilai variabel tersebut tidak akan berubah setelah dideklarasikan. Hal ini menjadikan `const` pilihan yang baik ketika Anda ingin membuat variabel yang hanya dapat dibaca di dalam blok tertentu dan memiliki nilai tetap.

Variabel dengan cakupan blok sangat berguna dalam membuat kode yang lebih aman dan memahami, karena Anda dapat membatasi akses ke variabel hanya pada bagian yang memerlukannya.

**FUNCTION SCOPE**
Variabel dengan cakupan (scope) fungsi adalah variabel yang hanya dapat diakses di dalam fungsi di mana variabel tersebut dideklarasikan. Berikut adalah contoh penggunaan variabel dengan cakupan fungsi:

```javascript
function contohScope() {
  let pesan = "Halo, dunia!"; // Variabel pesan hanya dapat diakses di dalam fungsi ini
  console.log(pesan); // Output: "Halo, dunia!"
}

contohScope();

// Di luar fungsi, variabel pesan tidak dapat diakses
console.log(pesan); // Ini akan menyebabkan error
```

Dalam contoh di atas, variabel `pesan` dideklarasikan dengan kata kunci `let` di dalam fungsi `contohScope`. Oleh karena itu, variabel `pesan` hanya dapat diakses di dalam fungsi tersebut. Di luar fungsi `contohScope`, variabel `pesan` tidak dapat diakses.

Variabel dengan cakupan fungsi sangat berguna dalam mengisolasi variabel dan data yang hanya diperlukan dalam konteks tertentu, seperti di dalam fungsi. Ini membantu mencegah polusi namespace dan konflik nama variabel dalam kode Anda.

**GLOBAL SCOPE**
Variabel dengan cakupan (scope) global adalah variabel yang dapat diakses dari mana saja dalam kode JavaScript, baik itu di dalam fungsi, di luar fungsi, atau di berbagai berkas JavaScript yang dijalankan dalam satu halaman web. Variabel global dideklarasikan di luar semua fungsi dan blok kode, sehingga mereka memiliki cakupan yang luas di seluruh program Anda.

Berikut adalah contoh penggunaan variabel dengan cakupan global:

```javascript
// Variabel global
var nama = "John";

function contohScope() {
  // Variabel lokal
  var pesan = "Halo, dunia!";
  console.log(pesan); // Output: "Halo, dunia!"

  // Mengakses variabel global dari dalam fungsi
  console.log(nama); // Output: "John"
}

contohScope();

// Mengakses variabel global di luar fungsi
console.log(nama); // Output: "John"
```

Dalam contoh di atas, variabel `nama` dideklarasikan di luar fungsi `contohScope`, sehingga menjadi variabel global. Variabel global `nama` dapat diakses dari dalam fungsi `contohScope` dan di luar fungsi tersebut.

Variabel dengan cakupan global memiliki beberapa pertimbangan:

1. **Pencemaran Nama (Namespace Pollution):** Karena variabel global dapat diakses dari mana saja, Anda harus berhati-hati agar tidak mengganti nilainya atau mengaksesnya secara tidak sengaja dari berbagai bagian kode Anda. Ini dapat mengarah pada kesulitan dalam pemeliharaan dan pemahaman kode.

2. **Potensi Konflik Nama (Name Conflicts):** Jika Anda menggunakan variabel global dengan nama yang sama dalam berkas JavaScript yang berbeda, Anda dapat mengalami konflik nama yang sulit diidentifikasi dan diperbaiki.

3. **Kinerja:** Variabel global dapat mempengaruhi kinerja aplikasi jika terlalu banyak digunakan. Ini karena variabel global tetap ada selama aplikasi berjalan, bahkan jika tidak digunakan lagi, sehingga memakan memori.

Karena beberapa masalah yang mungkin timbul akibat penggunaan variabel global, disarankan untuk menghindarinya sebisa mungkin. Sebaiknya gunakan pendekatan yang lebih aman dengan menggunakan cakupan lokal (variabel dalam fungsi) atau memanfaatkan mekanisme modularisasi seperti modul CommonJS atau ES6 Modules untuk mengurangi penggunaan variabel global dalam kode Anda.
