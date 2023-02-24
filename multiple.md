# Apa yang dimaksud dengan multiple impor/ekspor javascript?
Dalam JavaScript, istilah "impor" dan "ekspor" digunakan untuk menentukan bagaimana modul diatur dan dibagikan di berbagai bagian aplikasi.<br>
Pernyataan "Impor" digunakan untuk memuat modul ke dalam file, sedangkan pernyataan "ekspor" digunakan untuk mengekspos bagian modul untuk digunakan di file lain. Beberapa impor/ekspor mengacu pada kemampuan untuk mengimpor dan mengekspor beberapa item dalam satu pernyataan.<br>
## contoh "import" untuk memuat banyak item dari modul seperti ini:<br>
import { item1, item2, item3 } from './myModule';<br>
Dalam hal ini, item "item1", "item2", dan "item3" sedang diimpor dari file "myModule".<br>
## contoh "ekspor" untuk mengekspor beberapa item dari modul seperti ini:
export { item1, item2, item3 };<br>
Dalam hal ini, item "item1", "item2", dan "item3" diekspor dari modul.<br><br>
Beberapa pernyataan impor/ekspor dapat membuat kode lebih ringkas dan lebih mudah dibaca dengan mengurangi jumlah baris kode yang diperlukan untuk mengimpor atau mengekspor beberapa item<br><br>
# Kapan bisa menggunakan banyak impor/ekspor javascript?<br>
Beberapa pernyataan impor/ekspor dapat digunakan setiap kali ada banyak item dalam modul yang perlu diimpor atau diekspor. Ini sering terjadi ketika modul berisi kumpulan fungsi, kelas, atau konstanta terkait yang digunakan di berbagai bagian aplikasi.<br>
Misalnya, modul bernama "utils" yang berisi beberapa fungsi pembantu, serta beberapa konstanta dan kelas:<br>
// utils.js

export const PI = 3.14159;

export function square(x) {<br>
  return x * x;<br>
}<br>

export function cube(x) {<br>
  return x * x * x;<br>
}<br>

export class Point {<br>
  constructor(x, y) {<br>
    this.x = x;<br>
    this.y = y;<br>
  }<br>

  distance() {<br>
    return Math.sqrt(this.x * this.x + this.y * this.y);<br>
  }<br>
}

Untuk menggunakan item ini di modul lain, Anda dapat menggunakan beberapa pernyataan import seperti ini:<br>
// main.js

import { PI, square, cube, Point } from './utils';

console.log(PI);<br>
console.log(square(3));<br>
console.log(cube(3));<br>

const p = new Point(3, 4);<br>
console.log(p.distance());<br>
Dalam contoh ini, menggunakan pernyataan impor tunggal untuk mengimpor beberapa item dari modul "utils". Kami kemudian dapat menggunakan item ini dalam kode kami sesuai kebutuhan.<br>
### Secara keseluruhan, menggunakan beberapa pernyataan impor/ekspor dapat membantu membuat kode Anda lebih modular, lebih mudah dibaca, dan lebih mudah dipelihara, terutama dalam aplikasi besar yang memiliki banyak modul dan file berbeda.



