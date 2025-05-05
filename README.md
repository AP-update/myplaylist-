# My Simple Music Playlist <i class="fa-solid fa-music"></i>

Sebuah halaman web sederhana yang menampilkan daftar musik dengan pemutar audio. Dibuat menggunakan HTML, CSS Tailwind, dan Font Awesome.

[Lihat Demo](URL_DEMO_KAMU_DI_SINI)

## Fitur

* **Daftar Musik:** Menampilkan daftar lagu dengan judul.
* **Pemutar Audio:** Setiap lagu dilengkapi dengan pemutar audio bawaan browser.
* **Pengelompokan:** Lagu dikelompokkan berdasarkan huruf pertama pada judul.
* **Desain Responsif:** Tata letak yang baik di berbagai ukuran layar.
* **Ikon Sosial Media:** Tautan ke platform sosial media kamu.
* **Mudah Diedit:** Struktur kode yang sederhana memudahkan penambahan, penghapusan, dan pengeditan konten.

## Cara Menggunakan

1.  **Unduh atau Klon Repository:**
    ```bash
    git clone [URL_REPOSITORY_KAMU]
    ```
2.  **Buka `index.html`:** Buka file `index.html` di browser web kamu.

## Cara Mengedit Musik

Untuk menambahkan, menghapus, atau mengganti informasi musik, kamu perlu memodifikasi bagian `<script>` di dalam file `index.html`. Cari blok kode berikut:

```javascript
  <script>
    const songs = [
            { title: "judul lagu", url: "https://files.catbox.moe/.mp3" },

            { title: "judul lagu", url: "https://files.catbox.moe/.mp3" },

      { title: "judul lagu", url: "https://files.catbox.moe/.mp3" },

            { title: "judul lagu", url: "[https://files.catbox.moe/.mp3" },

        { title: "judul lagu", url: "https://files.catbox.moe/.mp3" },
    ];
    // ... kode JavaScript lainnya ...
  </script>
```

### Menambah Musik Menggunakan Catbox.moe

Catbox.moe adalah layanan *file hosting* anonim yang bisa kamu gunakan untuk mengunggah file audio MP3 kamu dan mendapatkan *direct link* yang bisa digunakan di playlist ini. Berikut caranya:

1.  **Buka Situs Catbox.moe:** Kunjungi [https://catbox.moe/](https://catbox.moe/) di browser kamu.
2.  **Unggah File Audio:** Klik tombol "Choose File" atau seret dan lepas file MP3 yang ingin kamu tambahkan ke playlist.
3.  **Dapatkan Direct Link:** Setelah proses unggah selesai, Catbox.moe akan memberikan *direct link* ke file audio kamu. Biasanya link akan terlihat seperti `https://files.catbox.moe/kodeunik.mp3`.
4.  **Tambahkan ke `index.html`:** Salin *direct link* dari Catbox.moe dan tambahkan objek baru ke dalam array `songs` di file `index.html` dengan format berikut:

    ```javascript
        const songs = [
          // ... daftar lagu sebelumnya ...
          { title: "Nama Artis - Judul Lagu Baru", url: "[https://files.catbox.moe/kodeunik.mp3](https://files.catbox.moe/kodeunik.mp3)" }
        ];
    ```

    Ganti `"Nama Artis - Judul Lagu Baru"` dengan judul lagu yang sesuai dan `"https://files.catbox.moe/kodeunik.mp3"` dengan *direct link* yang kamu dapatkan dari Catbox.moe. Jangan lupa tambahkan koma di akhir objek sebelumnya jika ini bukan lagu pertama yang kamu tambahkan.

### Menghapus Musik

Untuk menghapus lagu, cukup hapus objek (kurung kurawal `{}`) yang sesuai dengan lagu yang ingin kamu hilangkan dari array `songs`. Pastikan kamu juga menghapus tanda koma jika lagu yang dihapus bukan yang terakhir dalam daftar.

### Mengganti Judul Musik

Untuk mengganti judul lagu, ubah nilai dari properti `title` pada objek lagu yang sesuai. Contoh:

```javascript
    const songs = [
      { title: "Judul Lagu Yang Diperbarui", url: "[https://files.catbox.moe/lqht9d.mp3](https://files.catbox.moe/lqht9d.mp3)" },
      // ... lagu lainnya ...
    ];
```

### Mengganti URL Musik

Untuk mengganti link file audio, ubah nilai dari properti `url` pada objek lagu yang sesuai. Pastikan URL yang kamu masukkan adalah URL langsung ke file MP3 (misalnya dari Catbox.moe atau layanan serupa). Contoh:

```javascript
    const songs = [
      { title: "judul laguu", url: "https://link/audio/baru.mp3" },
      // ... lagu lainnya ...
    ];
```

## Cara Mengganti Link Sosial Media

Untuk mengganti link ikon sosial media, cari bagian kode HTML berikut:

```html
    <div class="flex justify-center space-x-6 text-2xl text-gray-300 social-icons">
      <a href="[https://whatsapp.com/channel/0029VaalShkGZNCsXgFPO80A](https://whatsapp.com/channel/0029VaalShkGZNCsXgFPO80A)" class="text-green-500 hover:text-green-400 transition"><i class="fab fa-whatsapp"></i></a>
      <a href="#link FB mu" class="text-blue-600 hover:text-blue-500 transition"><i class="fab fa-facebook"></i></a>
      <a href="#link igmu" class="text-pink-500 hover:text-pink-400 transition"><i class="fab fa-instagram"></i></a>
      <a href="#link spotify mu" class="text-[#1ed760] hover:text-[#19b854] transition"><i class="fab fa-spotify"></i></a>
    </div>
```

Ganti nilai atribut `href` (`#link FB mu`, `#link igmu`, `#link spotify mu`) dengan URL profil sosial media kamu yang sebenarnya. Contoh:

```html
    <div class="flex justify-center space-x-6 text-2xl text-gray-300 social-icons">
      <a href="[https://whatsapp.com/channel/LINK_WHATSAPP_KAMU]" class="text-green-500 hover:text-green-400 transition"><i class="fab fa-whatsapp"></i></a>
      <a href="[https://facebook.com/PROFIL_FB_KAMU" class="text-blue-600 hover:text-blue-500 transition"><i class="fab fa-facebook"></i></a>
      <a href="[https://instagram.com/PROFIL_IG_KAMU]" class="text-pink-500 hover:text-pink-400 transition"><i class="fab fa-instagram"></i></a>
      <a href="[https://open.spotify.com/user/PROFIL_SPOTIFY_KAMU]" class="text-[#1ed760] hover:text-[#19b854] transition"><i class="fab fa-spotify"></i></a>
    </div>
```

## Kustomisasi Lebih Lanjut

Kamu dapat menyesuaikan tampilan halaman ini lebih lanjut dengan memodifikasi kode CSS di dalam tag `<style>` atau dengan menambahkan kelas-kelas Tailwind CSS lainnya pada elemen-elemen HTML.

-----

Dibuat dengan \<3 oleh A\&Z
```

