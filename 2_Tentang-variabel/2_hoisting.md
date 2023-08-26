**HOISTING**

Hoisting adalah perilaku di JavaScript di mana deklarasi variabel dan fungsi dinaikkan (hoisted) ke bagian atas cakupan (scope) saat kode dijalankan. Ini berarti Anda dapat mengakses variabel atau fungsi sebelum mereka sebenarnya dideklarasikan dalam kode Anda. Meskipun deklarasi ini dinaikkan, inisialisasi (penugasan nilai) tetap dijalankan dalam urutan sebenarnya. Ini mungkin menjadi sumber kebingungan bagi pengembang yang baru mengenal JavaScript. Mari kita bahas beberapa contoh untuk lebih memahami konsep hoisting:

1. **Hoisting Variabel:**

   ```javascript
   console.log(nama); // Output: undefined
   var nama = "John";
   ```

   Pada contoh di atas, deklarasi `var nama` dinaikkan ke atas cakupan (scope) oleh JavaScript. Namun, nilai `undefined` yang muncul bukanlah nilai yang sebenarnya. Ini karena inisialisasi (nilai "John") tidak dinaikkan bersamaan dengan deklarasi. Kode di atas setara dengan:

   ```javascript
   var nama; // Deklarasi dinaikkan
   console.log(nama); // Output: undefined
   nama = "John"; // Inisialisasi dilakukan di sini
   ```

2. **Hoisting Fungsi:**

   ```javascript
   greet(); // Output: "Halo, dunia!"
   function greet() {
     console.log("Halo, dunia!");
   }
   ```

   Pada contoh di atas, deklarasi fungsi `greet` dinaikkan ke atas cakupan, sehingga Anda dapat memanggilnya sebelum deklarasi sebenarnya dalam kode. Ini setara dengan:

   ```javascript
   function greet() {
     console.log("Halo, dunia!");
   }
   greet(); // Output: "Halo, dunia!"
   ```

Namun, perlu diingat bahwa hoisting hanya mempengaruhi deklarasi variabel dan fungsi, bukan inisialisasi atau nilai-nilai aktual. Oleh karena itu, sebaiknya selalu mendeklarasikan variabel dan fungsi di bagian atas cakupan atau blok Anda untuk menghindari kebingungan yang disebabkan oleh hoisting. Juga, untuk variabel, lebih disarankan untuk menggunakan `let` atau `const` daripada `var`, karena `let` dan `const` tidak mengalami hoisting dalam cakupan blok.
