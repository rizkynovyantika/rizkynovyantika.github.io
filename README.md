# rizkynovyantika.github.io

## Penggunaan
1. Buat file postingan
```
hugo new post/<judul-posting>.md
```
2. Tulislah naskah artikel dan sesuaikan meta. Jika ada gambar buat folder di `static/images` namakan folder sesuai dengan judul artikel
3. Commit
```
git add -A;
git commit -m "Pesan Commit"
```
4. Generate HTML
```
hugo
```
5. Keluarkan (cut) folder `public` (kemana aja)
6. Ganti branch
```
git checkout master
```
7. Paste (replace) isi folder `public`
8. Push
```
git add -A;
git commit -m "$(date)";
git push origin master
```