# Tutorial Menggunakan STADATA Package BPS
![image](https://github.com/syaerulid/stadata_bps_tutor/assets/119069839/4311c297-6062-42d1-ab5d-8819fe533db7)

Apa itu **STADATA?**
<br><br>
STADATA adalah Python Package yang dibuat oleh tim Badan Pusat Statistik untuk memudahkan (data analyst, researcher, atau pengguna biasa seperti kita) memperoleh data yang disediakan oleh BPS.
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

3. Cek Domain dari Daerah yang ingin kita ambil datanya

Melalui stadata, list_domain adalah suatu method yang me-return  
(domain_id, domain_name, domain_url, dan juga level)
dari data yang ada di BPS. bisa dibilang ini adalah Induknya.

selain itu ada beberapa method lain:
