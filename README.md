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
**bisa!**<br>
**list semua statictable di Jateng**
![image](https://github.com/syaerulid/stadata_bps_tutor/assets/119069839/2de32781-640b-4b12-bd7e-8c2bc719693d)
<br>
**list semua statictable di Semarang**
![image](https://github.com/syaerulid/stadata_bps_tutor/assets/119069839/f486ce54-24f8-455b-946b-7c12770cb139)
<br>
**Filter data Statictable Jateng dalam 3 Tahun Terakhir**
![image](https://github.com/syaerulid/stadata_bps_tutor/assets/119069839/166f1880-b443-4a5c-9e59-eb5253728be1)
<br><br>
**5**. Misalnya kita tertarik nih sama data Telur dan Unggas,<br>
nah gimana cara dapetin datanya???<br>

Kita menuju ke website:<br>







