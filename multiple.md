# Apa yang dimaksud dengan multiple impor/ekspor javascript?
Dalam JavaScript, istilah "import" dan "export" digunakan untuk menentukan bagaimana modul diatur dan dibagikan di berbagai bagian aplikasi.<br>
Pernyataan "Import" digunakan untuk memuat modul ke dalam file, sedangkan pernyataan "export" digunakan untuk mengekspos bagian modul untuk digunakan di file lain. Multiple import/export mengacu pada kemampuan untuk mengimpor dan mengekspor beberapa item dalam satu pernyataan.<br>
## contoh "import" untuk memuat banyak item dari modul seperti ini:<br>
```
import { item1, item2, item3 } from './myModule';
```
Dalam hal ini, item "item1", "item2", dan "item3" sedang diimpor dari file "myModule".<br>
## contoh "ekspor" untuk mengekspor beberapa item dari modul seperti ini:
```
export { item1, item2, item3 };
```
Dalam hal ini, item "item1", "item2", dan "item3" diekspor dari modul.<br><br>
Multiple import/export dapat membuat kode lebih ringkas dan lebih mudah dibaca dengan mengurangi jumlah baris kode yang diperlukan untuk mengimpor atau mengekspor beberapa item<br><br>

# Kapan bisa menggunakan multiple import/export javascript?<br>
Multiple import/export dapat digunakan setiap kali ada banyak item dalam modul yang perlu diimpor atau diekspor. Ini sering terjadi ketika modul berisi kumpulan fungsi, kelas, atau konstanta terkait yang digunakan di berbagai bagian aplikasi.<br>
Misalnya, modul bernama "utils" yang berisi beberapa fungsi pembantu, serta beberapa konstanta dan kelas:<br>
```
// utils.js

export const PI = 3.14159;

export function square(x) {
  return x * x;
}

export function cube(x) {
  return x * x * x;
}

export class Point {
  constructor(x, y) {
    this.x = x;
    this.y = y;
  }<br>

  distance() {
    return Math.sqrt(this.x * this.x + this.y * this.y);
  }
}
```
Untuk menggunakan item ini di modul lain, Anda dapat menggunakan beberapa pernyataan import seperti ini:<br>
```
// main.js

import { PI, square, cube, Point } from './utils';

console.log(PI);
console.log(cube(3));

const p = new Point(3, 4);
console.log(p.distance());
```
Dalam contoh ini, menggunakan pernyataan import tunggal untuk mengimpor beberapa item dari modul "utils". kemudian dapat menggunakan item ini dalam kode sesuai kebutuhan.<br>
Secara keseluruhan, menggunakan beberapa pernyataan impor/ekspor dapat membantu membuat kode Anda lebih modular, lebih mudah dibaca, dan lebih mudah dipelihara, terutama dalam aplikasi besar yang memiliki banyak modul dan file berbeda.

## Bagaimana menggunakan multiple import/export dalam javaScript

Untuk menggunakan mulitple import/export dalam JavaScript, dapat menggunakan sintaks berikut:

Dalam modul tempat Anda ingin mengekspor beberapa item, dapat menggunakan pernyataan export yang diikuti dengan daftar item yang ingin diekspor yang dipisahkan koma:


```
export const item1 = "value1";
export const item2 = "value2";
export function myFunction() { /* function code */ }
```
Dalam modul tempat Anda ingin mengimpor beberapa item, Anda dapat menggunakan pernyataan importyang diikuti dengan daftar item yang ingin Anda impor yang dipisahkan koma:
```
import { item1, item2, myFunction } from './myModule';
```

Anda juga dapat menggunakan import * assintaks untuk mengimpor semua item yang diekspor dari modul sebagai objek tunggal:
```
import * as myModule from './myModule';

console.log(myModule.item1);
console.log(myModule.item2);
myModule.myFunction();
```

Dalam hal ini, semua item yang diekspor dari myModulemodul akan tersedia sebagai properti objek myModule.

Perhatikan bahwa saat menggunakan multiple import/export, penting untuk memastikan bahwa item yang diexport dan diimport memiliki nama dan tipe data yang benar, karena ketidakcocokan dapat menyebabkan kesalahan dalam kode Anda.




