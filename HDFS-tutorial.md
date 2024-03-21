### Step-by-step tutorial on how to insert data into HDFS

1. **Startting HDFS** \
Pertama-tama, Anda harus memformat sistem file HDFS yang telah dikonfigurasi, buka namenode (server HDFS), dan jalankan perintah berikut.

```bash
hadoop namenode -format 
```

2. **Start Hadoop Cluster** \
Setelah memformat HDFS, mulai sistem berkas terdistribusi. Perintah berikut ini akan memulai namenode serta node data sebagai cluster.

```bash
start-all.sh
```

Setelah menjalankan perintah di atas, menggunakan browser klik link berikut <http://localhost:9870/explorer.html#/>.

<img title="a title" alt="Alt text" src="img/initiate.png">

3. **Check HDFS Status** \
Anda dapat memeriksa status HDFS untuk memastikan bahwa HDFS berjalan dengan baik. Buka jendela terminal baru dan ketik:
```bash
hdfs dfsadmin -report
```
Perintah ini akan memberikan laporan terperinci tentang status HDFS Anda.

<img title="a title" alt="Alt text" src="img/2.png">

4. **Create User Directory ** \
Anda harus membuat direktori input.
```bash
hadoop fs -mkdir /user
```
Pastikan direktori user telah terbentuk.

<img title="a title" alt="Alt text" src="img/3.png">

5. **Add a Directory Inside The User Directory** \
Buat direktori dengan nama Anda
```bash
hadoop fs -mkdir /user/sevi
```
Pada kolom Name yang terletak di sebelah kiri klik user sehingga menampilkan direktori dari nama Anda.

<img title="a title" alt="Alt text" src="img/4.png">

5. **Create New File on Your Local** \
Buat file baru yang diberi nama data.csv di komputer Anda.
```bash
cd Documents/hadoop \
touch data.csv \
code data.csv
```

6. **Put the new file into the /user/sevi folder** 
Buka direktori file melalui terminal kemudian upload data.csv ke direktori nama Anda di hadoop.
```bash
hadoop fs -put data.csv /user/sevi
```

Pada kolom Name yang terletak di sebelah kiri klik nama Anda sehingga menampilkan data.csv.

<img title="a title" alt="Alt text" src="img/5.png">