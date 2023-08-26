Dalam JavaScript, ada beberapa aturan yang harus diikuti ketika Anda menamai variabel:

1. **Nama Variabel harus dimulai dengan huruf (a-z, A-Z), garis bawah (\_), atau tanda dollar ($).** Misalnya, `nama`, `_variabel`, atau `$variabel` adalah nama variabel yang valid.

2. **Karakter berikutnya dapat berupa huruf (a-z, A-Z), angka (0-9), garis bawah (\_), atau tanda dollar ($).** Misalnya, `namaVariabel1`, `_nilai`, atau `$jumlah_total` adalah nama variabel yang valid.

3. **Variabel bersifat case-sensitive.** Artinya, `namaVariabel` dan `namavariabel` dianggap sebagai dua variabel yang berbeda.

4. **Hindari menggunakan kata kunci (reserved words) sebagai nama variabel.** JavaScript memiliki sejumlah kata kunci yang memiliki makna khusus dalam bahasa. Anda tidak boleh menggunakan kata kunci ini sebagai nama variabel. Beberapa contoh kata kunci JavaScript adalah `if`, `else`, `for`, `while`, `function`, dan lain-lain.

5. **Gunakan gaya penamaan yang konsisten.** Ini membantu dalam pembacaan dan pemahaman kode. Ada beberapa konvensi penamaan yang umum digunakan:

   - **Camel Case:** Di mana kata pertama tidak diawali huruf besar, dan kata-kata berikutnya diawali huruf besar. Contoh: `namaVariabel`, `jumlahTotal`.
   - **Snake Case:** Di mana kata-kata dipisahkan dengan garis bawah. Contoh: `nama_variabel`, `jumlah_total`.
   - **Kebab Case:** Di mana kata-kata dipisahkan dengan tanda hubung (dash). Contoh: `nama-variabel`, `jumlah-total`.

6. **Nama variabel sebaiknya deskriptif.** Gunakan nama yang menjelaskan tujuan atau isian dari variabel tersebut. Ini akan membuat kode lebih mudah dimengerti oleh Anda dan orang lain yang membaca kode Anda.

Contoh penggunaan variabel dengan nama yang baik:

```javascript
let jumlahPengguna = 10; // Deskriptif dan menggunakan camel case
let total_belanja = 100.50; // Deskriptif dan menggunakan snake case
let nama-pelanggan = "John Doe"; // Deskriptif dan menggunakan kebab case
```

Mematuhi aturan-aturan ini akan membantu Anda menulis kode JavaScript yang lebih mudah dipahami, dikelola, dan dipelihara.
