# Tutorial Menggunakan STADATA Package BPS
![image](https://github.com/syaerulid/stadata_bps_tutor/assets/119069839/4311c297-6062-42d1-ab5d-8819fe533db7)

Apa itu **STADATA?**
<br><br>
STADATA adalah Python Package yang dibuat oleh tim Badan Pusat Statistik untuk memudahkan <br>(data analyst, researcher, atau pengguna biasa seperti kita) memperoleh data yang disediakan oleh BPS.
<br><br>
**1.** Daftarkan identitas kita di website API BPS<br>
https://webapi.bps.go.id/developer/<br>
lalu isi semua data diri yang dibutuhkan<br>
seperti ini:<br>
![image](https://github.com/syaerulid/stadata_bps_tutor/assets/119069839/c5c5e579-e378-461e-9bf8-969a39387e94)
![image](https://github.com/syaerulid/stadata_bps_tutor/assets/119069839/7eb48869-0bdb-4dc1-a378-d70711d6f8af)

setelah mendapatkan App ID, simpan App ID, karena ini nantinya akan digunakan sebagai penghubung antara kita (user) untuk melakukan requests ke API BPS
<br><br>
**2.** Install stadata di Python IDE kita
setelah terinstall, import library yang kira2 kita butuhkan
untuk library umum dari stadata ada empat yaitu :<br>
**stadata, requests, html dan pandas**
<br><br>
![image](https://github.com/syaerulid/stadata_bps_tutor/assets/119069839/7b6d16dc-2eab-4f04-b2e2-edcbdf823ab6)

**3.** Cek Domain dari Daerah yang ingin kita ambil datanya

Melalui stadata, list_domain adalah suatu method yang me-return<br>
**(domain_id, domain_name, domain_url, dan juga level)**
dari data yang ada di BPS.<br>
bisa dibilang ini adalah **Induknya.**

selain itu ada beberapa method lain:
<br><br>
3.1 list_statictable(params)<br>
3.2 list_dynamictable(params)<br>
3.3 list_publication(params)<br>
3.4 list_pressrelease(params)<br>
<br>
selain method list ada juga method view, untuk melihat preview data yang ingin kita ketahui<br>
contoh:<br>
3.5 view_statictable(params)<br><br>

**4.** Contoh penggunaan statictable
Disini kita ingin melihat semua statictable yang ada di Jawa Tengah<br>
atau mungkin Semarang?<br>
atau mungkin ingin memfilter data 3 tahun terakhir?<br>
**bisa!**<br><br>
<p align="center"><strong>4.1 List of All Static Tables in Jateng</strong></p>
<p align="center">
  <img src="https://github.com/syaerulid/stadata_bps_tutor/assets/119069839/2de32781-640b-4b12-bd7e-8c2bc719693d" alt="Image">
</p>
<br><br>
<p align="center"><strong>4.2 List of All Static Tables in Semarang</strong></p>
<p align="center">
  <img src="https://github.com/syaerulid/stadata_bps_tutor/assets/119069839/f486ce54-24f8-455b-946b-7c12770cb139" alt="Image">
</p>
<p align="center"><strong>4.3 Filter Data from Static Tables in Jateng for the Last 3 Years</strong></p>
<p align="center">
  <img src="https://github.com/syaerulid/stadata_bps_tutor/assets/119069839/166f1880-b443-4a5c-9e59-eb5253728be1" alt="Image">
</p>

**5**. Misalnya kita tertarik nih sama data Telur dan Unggas,<br>
nah gimana cara dapetin datanya???<br>
<p align="center">
  <img src="https://github.com/syaerulid/stadata_bps_tutor/assets/119069839/401a5cdd-100c-4d3c-a4be-144709879d8a" alt="Image">
</p>
Kita menuju ke website:<br>
https://webapi.bps.go.id/documentation/#statictable_1
<br><br>
<p align="center"><img src="https://github.com/syaerulid/stadata_bps_tutor/assets/119069839/1012a325-1b1a-4a15-a450-5b76f38835b1" alt="Image"></p>
<details>
  <summary>5.1 Domain (Area Domain)</summary>
  <p>Domain adalah nomer domain dari daerah yang ingin Anda telusuri.</p>
</details>
<details>
  <summary>5.2 Model (Metode yang Digunakan)</summary>
  <p>Model merujuk pada metode yang Anda gunakan.</p>
</details>
<details>
  <summary>5.3 Lang (Bahasa)</summary>
  <p>Lang merujuk pada bahasa, baik Indonesia (ind) atau Inggris (eng).</p>
</details>

<details>
  <summary>5.4 ID (Table ID)</summary>
  <p>ID adalah tabel ID yang sedang Anda gunakan.</p>
</details>

<details>
  <summary>5.5 Key (Kunci API)</summary>
  <p>Key adalah kunci API Anda.</p>
</details>
<br>
setelah itu kita akan diberikan link dari data yang kita butuhkan.<br>
excel : "link"<br>
copy link tersebut.
<p align="center">Lihat gambar dibawah agar lebih jelas</p>
<p align="center">
  <img src="https://github.com/syaerulid/stadata_bps_tutor/assets/119069839/586b3cf0-ed8a-4d3a-abd1-6d33c35fee20" alt="Image">
</p>

**6.** masukan link tersebut kedalam sebuah variable (bebas, terserah kita)<br>
check status response dari link tersebut<br>
<p align="center">
  <img src="https://github.com/syaerulid/stadata_bps_tutor/assets/119069839/ee71499e-f3e8-4006-acf7-b4700dbdeb2e" alt="Image">
</p>
pastikan <strong>response status code adalah 200</strong><br>
bukan seperti dibawah ini<br>
404 : not found<br>
403 : forbidden<br>
500 : Internal Server Error<br>
setelah itu download file tersebut kedalam local<br><br>

**7.** Load file yang ada di local tadi dalam bentuk dataframe menggunakan pandas
![image](https://github.com/syaerulid/stadata_bps_tutor/assets/119069839/6e9ea07c-a6ac-4a07-b4d6-bac403dda12e)
terlihat bahwa file masih acak2an dan kotor, serta nama kolom tidak jelas, setelah ini lakukan data cleaning sederhana

**8**. Data Cleaning (Opsional)
<p align="center"><strong>8.1 Data Cleaning Mengganti Nama Kolom</strong></p>
<p align="center">
  <img src="https://github.com/syaerulid/stadata_bps_tutor/assets/119069839/a583ac37-3de4-4709-af59-5b7cb6c9bde1" alt="Image">
</p>
<p align="center"><strong>8.2 Drop Kolom yang tidak dibutuhkan</strong></p>
<p align="center">
  <img src="https://github.com/syaerulid/stadata_bps_tutor/assets/119069839/0189eba0-8959-46d3-a8e7-4cc026971a67" alt="Image">
</p>
<p align="center"><strong>8.3 Bedakan Data menjadi data kabupaten dan data kota</strong></p>
<p align="center">
  <img src="https://github.com/syaerulid/stadata_bps_tutor/assets/119069839/9c54e1fe-6268-4882-961f-82087c11b834" alt="Image">
</p>
<p align="center"><strong>8.4 Ganti Nama Kolom Kabupaten menjadi Kota, untuk data kota</strong></p>
<p align="center">
  <img src="https://github.com/syaerulid/stadata_bps_tutor/assets/119069839/6cc0ddaa-160f-48ca-97bc-abc68de969a8" alt="Image">
</p>
<p align="center"><strong>8.5 Data sudah bersih</strong></p>
<p align="center">
  <img src="https://github.com/syaerulid/stadata_bps_tutor/assets/119069839/0ef61aa1-7777-4858-bd10-a17b881c54e3" alt="Image">
</p>
<br>

**9**. Buat analisa kita
<br>
sebagai contoh, ini visualisasi yang terbentuk dari data BPS yang sudah di cleaning<br>
<p align="center"><strong>Data Produksi Ayam Kampung</strong></p>
<p align="center">
  <img src="https://github.com/syaerulid/stadata_bps_tutor/assets/119069839/96879e9e-613b-44e7-b59c-78ff03f9f919" alt="Image">
</p>

**10**. Untuk proses pengambilan data yang lebih otomatis, silahkan ke data_automation pada repo ini.

Semoga bermanfaat buat teman-teman <strong>data analyst, scientist, researcher atau bahkan sekedar pengguna yang  penasaran xd</strong><br>
<br><br>
<p align="center"><strong>Special Thanks to BPS Indonesia dan Tim yang menyusun STADATA</strong></p>
<br><br>
Official Links to <strong>STADATA</strong>:
<br>
https://github.com/bps-statistics/stadata







