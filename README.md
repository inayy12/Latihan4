### Latihan4
## Nama: Inayatus Sholekhawati
## NIM: 3122110200
## Kelas: TI.22.A.2
### TUGAS PERTEMUAN 10

## Tabel pegawai 
Buatlah tabel pegawai dengan kodingan berikut
```
CREATE TABLE pegawai (
  idpegawai VARCHAR(10) PRIMARY KEY,
  nama_depan VARCHAR(15),
  nama_belakang VARCHAR(15),
  email VARCHAR(25),
  telepon VARCHAR(30),
  tgl_kontrak DATE,
  id_job VARCHAR(10),
  gaji INT,
  tunjangan INT
);


INSERT INTO pegawai (idpegawai, nama_depan, nama_belakang, email, telepon, tgl_kontrak, id_job, gaji, tunjangan)
VALUES
('E001', 'Ferry', 'gustiawan', 'ferry@yahoo.com', '07117059004', '2005-09-01', 'L0001', 2000000, 500000),
('E002', 'aris', 'ganiardi', 'aris@yahoo.com', '081312345678', '2006-09-01', 'L0002', 2000000, 200000),
('E003', 'faiz', 'ahnad', 'faiz@gmail.com', '081367384342', '2006-10-01', 'L0003', 1500000, NULL),
('E004', 'emna', 'bunton', 'enna@gmail.com', '081363484342', '2006-10-01', 'L0004', 1500000, 9),
('E005', 'mike', 'scoff', 'mike@plasa.com', '08163454555', '2007-09-01', 'L0005', 1250000, 9),
('E006', 'lincolin', 'burrows', 'linc@yahoo.com', '08527388432', '2008-09-01', 'L0006', 1750000, NULL);

```

<img width="850" alt="ss1" src="https://github.com/inayy12/Latihan4/assets/115867315/9380f25d-2353-434b-bcbf-9d42899a0755">

<img width="668" alt="ss2" src="https://github.com/inayy12/Latihan4/assets/115867315/9204f81c-73f8-40d6-bbfa-93a9d8d591c7">

1. Tampilkan pegawai yang gaji bukan 2.000.000 dan 1.250.000

```
SELECT * FROM pegawai WHERE gaji NOT IN (2000000, 1250000);
```
<img width="660" alt="ss3" src="https://github.com/inayy12/Latihan4/assets/115867315/a180030e-5826-4a48-b15c-969121fcbbc6">

2. Tampilkan pegawai yang tunjuangannya NULL!

```
SELECT * FROM pegawai WHERE tunjangan IS NULL;
```

<img width="660" alt="ss3" src="https://github.com/inayy12/Latihan4/assets/115867315/100e78ec-bc2b-4621-8112-6f2a2c7e3b7d">

3. Tampilkan pegawai yang tunjangannya tidak NULL!

```
SELECT * FROM pegawai WHERE tunjangan IS NOT NULL;
```

<img width="657" alt="ss4" src="https://github.com/inayy12/Latihan4/assets/115867315/9680a4e1-cdca-49a2-a5a1-f2922ad91e5a">

4. Tampilkan/hitung jumlah baris/record tabel pegawai!

```
SELECT COUNT(*) FROM pegawai;
```

<img width="671" alt="ss5" src="https://github.com/inayy12/Latihan4/assets/115867315/5c803c37-3971-4333-9b2f-e555e08d71c9">

5. Tampilkan/hitung jumlah total gaji di tabel pegawai!

```
