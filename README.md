# Belajar Git #

## Version Control System ##
Version control adalah sebuah sistem yang mencatat setiap perubahan terhadap sebuah berkas atau kumpulan berkas sehingga pada suatu saat anda dapat kembali kepada salah satu versi dari berkas tersebut.

Ada tiga macam jenis VCS yaitu :
* VCS Local
* VCS Terpusat
* VCS Terdistribusi

## GIT ##
Git adalah salah satu jenis Version Control System. Namun Git berbeda dengan VCS lainnya. Salah satu perbedaan yang mencolok antar Git dengan VCS lain yaitu dalam hal cara git memperlakukan datanya. VCS lain menyimpan informasi sebagai sebuah daftar perubahan berkas. Git memperlakukan datanya sebagai sebuah kumpulan snapshot dari sebuah miniatur sistem berkas.

Git memiliki 3 keadaan utama dimana berkas anda dapat berada: '''committed, modified dan staged'''. Committed berarti data telah tersimpan secara aman pada basisdata lokal. Modified berarti anda telah melakukan perubahan pada berkas namun anda belum melakukan commit pada basisdata. Staged berarti anda telah menandai berkas yang telah diubah pada versi yang sedang berlangsung untuk kemudian dilakukan commit.

Alur kerja dasar Git adalah seperti ini:

* Anda mengubah berkas dalam direktori kerja anda.
* Anda membawa berkas ke stage, menambahkan snapshotnya ke staging area.
* Anda melakukan commit, yang mengambil berkas seperti yang ada di staging area dan menyimpan snapshotnya secara permanen ke direktori Git anda.

Referensi : 
* https://git-scm.com/book/id/v1/Memulai-Git-Tentang-Version-Control
* https://git-scm.com/book/id/v1/Memulai-Git-Dasar-Git


## Kolaborasi Proyek Git ##
Git memungkinkan kita untuk melakukan kolaborasi proyek dengan git, adapun langkahnya sebagai berikut :
* Buka proyek yang ingin dimodifikasi, klik tombol Fork
* Konfigurasi akun git dengan perintah '''git config --global user.name "anjarrh" '''
* Membuat duplikasi proyek git yang akan diubah  dengan perintah '''git clone https://github.com/slamet789/Mengenal-Git.git '''
Hasilnya :
'''
Cloning into 'Mengenal-Git'...
remote: Counting objects: 3, done.
remote: Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
Unpacking objects: 100% (3/3), done.
Checking connectivity... done.
'''
* Direktori Mengenal-Git akan terbentuk, masuk pada direktori tersebut ''' cd Mengenal-Git '''
* Membuat branch baru dan langsung berpindah ke branch tersebut dengan perintah ''' git checkout -b 1-deskripsi-git '''
Branch yang dibuat bernama 1-deskripsi-git.
Hasilnya :
''' Switched to a new branch '1-deskripsi-git' '''
* Buat file .md pada direktori Mengenal-Git, file bernama deskripsi-git.md merupakan file markdown berisi deskripsi singkat tentang git
* Lakukan commit
''' git commit -am "deskripsi singkat tentang git" '''
Hasilnya :
'''
On branch 1-deskripsi-git
Untracked files:
        deskripsi-git.md
		
nothing added to commit but untracked files present
'''
* Tambahkan file .md pada repo dengan perintah ''' git add deskripsi-git.md '''
* Ulangi commit 'git commit -m "deskripsi sederhana git oleh anjar" '''
Hasilnya :
'''
[1-deskripsi-git 89d74aa] deskripsi sederhana git oleh anjar
 1 file changed, 23 insertions(+)
 create mode 100644 deskripsi-git.md
'''
* Remote dengan perintah '''git remote -v'''
Hasilnya :
'''
origin  https://github.com/slamet789/Mengenal-Git.git (fetch)
origin  https://github.com/slamet789/Mengenal-Git.git (push)
'''
* Lakukan push dengan perintah '''git push origin 1-deskripsi-git'''
Pada proses ini akan diminta username dan password github yang digunakan
Hasilnya :
'''
Fatal: HttpRequestException encountered.
Username for 'https://github.com': anjarrh
Password for 'https://anjarrh@github.com':
Counting objects: 3, done.
Delta compression using up to 4 threads.
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 980 bytes | 0 bytes/s, done.
Total 3 (delta 0), reused 0 (delta 0)
To https://github.com/slamet789/Mengenal-Git.git
   05731b3..89d74aa  1-deskripsi-git -> 1-deskripsi-git
'''

Referensi :
* https://github.com/endymuhardin/belajarGit/blob/master/cara-berkontribusi-opensources-github.md
* https://www.petanikode.com/github-workflow/

## Membuat Proyek Git Mandiri ##
Setelah melakukan kolaborasi, agar proses kolaborasi dapat terdokumentasi dengan baik perlu dibuat dokumentasi pribadi pada github. Adapun langkahnya sebagai berikut :
* Membuat file README.md berisi dokumentasi langkah kerja yang sedang dibaca ini
* Membuat repo baru bernama belajar-git dengan perintah '''git init belajar-git'''
Hasilnya :
'''
Initialized empty Git repository in F:/KULIAH/TI_Semester4/Praktikum TCCL/Mengenal-Git/belajar-git/.git/
'''
* Pindah ke direktori baru yang otomatis tercipta yaitu belajar-git '''cd belajar-git'''
* Letakkan file .md yang dibuat tadi pada direktori master proyek yaitu di belajar-git/README.md