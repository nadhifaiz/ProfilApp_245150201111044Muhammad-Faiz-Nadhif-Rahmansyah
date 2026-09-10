# Tugas Praktikum 2 - ProfilApp

Aplikasi profil sederhana yang dibangun menggunakan Jetpack Compose dengan arsitektur UI deklaratif.

## Penjelasan Singkat Kode
1. **Layouting (`Column` & `Box`):** Menggunakan `Box` untuk memposisikan kontainer ke tengah layar, serta `Column` dengan `Alignment.CenterHorizontally` agar seluruh elemen (Foto, Teks, Tombol) tersusun rapi secara vertikal di tengah.
2. **Komponen UI Dasar:** 
   - `Image` dengan modifier `.clip(CircleShape)` untuk menampilkan foto profil berbentuk lingkaran.
   - `Text` untuk menampilkan nama lengkap, NIM, dan deskripsi program studi.
   - `Spacer` untuk memberikan jarak vertikal antar elemen.
3. **State Management (`FollowButton`):** Menggunakan `remember { mutableStateOf(false) }` untuk melacak status tombol. Ketika tombol diklik, state `isFollowed` dinegasikan sehingga memicu rekomposisi otomatis untuk mengubah teks antara "Follow" dan "Unfollow".

## Analisis: Keuntungan Jetpack Compose vs XML Layout
- **Deklaratif vs Imperatif:** Pada Compose, kita cukup mendefinisikan tampilan berdasarkan *state*. Kita tidak perlu lagi menulis XML layout, memanggil `findViewById()`, atau memanipulasi view secara manual langkah demi langkah.
- **Produktivitas & Kode Ringkas:** Mengurangi *boilerplate code* secara drastis karena logika bisnis UI dan tampilan ditulis dalam bahasa yang sama (Kotlin), tanpa perlu berpindah-pindah file antara XML dan Kotlin.
- **Modularitas & Reusabilitas:** Komponen UI dibuat berupa fungsi composable kecil (seperti `FollowButton()`) yang mudah diuji dan digunakan kembali di bagian lain tanpa konfigurasi kustom view XML yang rumit.
