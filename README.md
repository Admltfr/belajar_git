belajar git motion


git commands



inisialisasi + remote repo
1. Folder
2. Git init
3. Cek bila iya udh add apa belum pakai git status
4. GIT add ( git add . untuk seluruh file project)
5. git commit -m "pesannya apa"
6. Buka github 
7. git remote add origin link repo (origin boleh custom tapi biasanya pakai origin)
8. git remote -v
9. git push -u origin main (sesuai nama branch dan origin) (untuk cek branchnya apa bisa git branch)
10. extra (cara ubah branch = git branch -M main <= untuk ubah master ke main)

undo
1. git log dapatkan hashcode dari log sebelum head
2. git reset --hard <hashcode sebelum head>
3. git push (harus git push -force namun tak disarankan)

show data log
1.git log

pull dari github
1.git pull

commit
1.git commit -m "message"

branching operation
1. git branch <= cek nama branch
2. git checkout -b master <= switch ke branch master sekaligus membuat branchnya
3. git branch -M main <= mengubah nama branch
4. git checkout main <= switch ke branch main
5. git branch -d master <= menghapus branch master (harus berada di branch lain terlebih dahulu pakai checkout kalau mau pindah)

branch baru
1. git checkout -b branchbaru <= buat dulu branch baru
2. git add . 
3. git commit -m "message"
4. git push <= copy saja commandnya di terminal yaitu git push --set-upstream origin master
5. done

rename branch
1. git branch -M branch lama nama branch baru
2. lalu untuk remote,
   git fetch origin,
  git branch -u origin/branchbaru branchbaru,
   git remote set-head origin -a

remote merge branch 
1. klik compare and pull request
2. jika tidak ada maka coba klik contribute lalu ada opsi pull requests
3. coba klik pull request
4. lalu confirm merge jika berhasil
5. setelah di merge maka branch yang "dummy" bisa dihapus karena yang telah dimerge masuk ke branch main
6. setelah itu lakukan git checkout main 
7. git pull
8. branch yang di merge akan dipull ke local (perubahan pada branch "dummy" akan ada di branch main sekarang, makanya branch dummy bisa dihapus)
