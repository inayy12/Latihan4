### Latihan4
## Nama: Inayatus Sholekhawati
## NIM: 3122110200
## Kelas: TI.22.A.2
### TUGAS PERTEMUAN 10

## Tabel pegawai 
Buatlah tabel pegawai 
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

<img width="657" alt="ss4" src="https://github.com/inayy12/Latihan4/assets/115867315/01ebbf7c-ac81-45ea-b2f0-cdd8c3c6a58b">


3. Tampilkan pegawai yang tunjangannya tidak NULL!

```
SELECT * FROM pegawai WHERE tunjangan IS NOT NULL;
```

<img width="671" alt="ss5" src="https://github.com/inayy12/Latihan4/assets/115867315/40f70922-81ed-4b3c-94ce-c3a4b8bb5f19">


4. Tampilkan/hitung jumlah baris/record tabel pegawai!

```
SELECT COUNT(*) FROM pegawai;
```

<img width="348" alt="ss6" src="https://github.com/inayy12/Latihan4/assets/115867315/e8c64b99-1317-4499-b5e7-8c9705a47538">

5. Tampilkan/hitung jumlah total gaji di tabel pegawai!

```
SELECT SUM(gaji) FROM pegawaiper;
```

<img width="354" alt="ss7" src="https://github.com/inayy12/Latihan4/assets/115867315/35d83392-4e23-4651-9081-36d23211a9bd">

6. Tampilkan/hitung rata-rata gaji pegawai!

```
SELECT AVG(gaji) FROM pegawaiper;
```

<img width="368" alt="ss8" src="https://github.com/inayy12/Latihan4/assets/115867315/3261381d-b8a7-4b3a-b0bf-4b234950657e">

7. Tampilkan gaji terkecil!

```
SELECT MIN(gaji) FROM pegawaiper;
```

<img width="337" alt="ss9" src="https://github.com/inayy12/Latihan4/assets/115867315/3b8b71fb-1de5-419b-973f-de98f2e4633a">

8. Tampilkan gaji terbesar!

```
SELECT MAX(gaji) FROM pegawaiper;
```

<img width="330" alt="ss10" src="https://github.com/inayy12/Latihan4/assets/115867315/3caae008-00a3-46b6-acb6-9cff2de93a58">

## Tabel Hewan
Buat tabel hewan 
```
 CREATE TABLE hewan (
    -> id VARCHAR(10) PRIMARY KEY,
    -> nama VARCHAR(15),
    -> owner VARCHAR(20),
    -> species VARCHAR(25),
    -> sex CHAR(1)
    -> );
    
    INSERT INTO hewan (id, nama, owner, species, sex)
    -> VALUES
    -> ('p1', 'Puffball', 'Diane', 'Hamster', 'f'),
    -> ('p2', 'Claws', 'Gwen', 'Cat', 'm'),
    -> ('p3', 'Fluffy', 'Haro 1d', 'Cat', 'f'),
    -> ('p4', 'Buffy', 'Haro 1d', 'Dog', 'f'),
    -> ('p5', 'Fang', 'Benny', 'Dog', 'm'),
    -> ('p6', 'Bowser', 'Diane', 'Dog', 'm'),
    -> ('p7', 'Chirpy', 'Gwen', 'Bird', 'f'),
    -> ('p8', 'Whistler', 'Gwen', 'Bird', NULL),
    -> ('p9', 'Slim', 'Benny', 'Snake', 'm');
 ```

<img width="666" alt="ss11" src="https://github.com/inayy12/Latihan4/assets/115867315/b28328d9-f38c-4ddd-b084-51ea78d43092">

<img width="618" alt="ss12" src="https://github.com/inayy12/Latihan4/assets/115867315/75ff353b-8ef4-4501-b1f8-b5da4ede4e35">

1. Tampilkan jumlah hewan yang dimiliki setiap owner.

```
 SELECT owner, COUNT(*) as jumlah_hewan FROM hewan GROUP BY owner;
 ```
 
 <img width="516" alt="ss13" src="https://github.com/inayy12/Latihan4/assets/115867315/36b92aab-d659-4582-850e-fd3836e56745">

2. Tampilkan jumlah hewan berdasarkan spesies.

```
SELECT species, COUNT(*) as jumlah_hewan FROM hewan GROUP BY species;
```

<img width="603" alt="ss14" src="https://github.com/inayy12/Latihan4/assets/115867315/1ad1aa53-c070-4938-98a2-2ef3e18ecc00">

3. Tampilkan jumlah hewan berdasarkan jenis kelamin.

```
SELECT sex, COUNT(*) as jumlah_hewan FROM hewan GROUP BY sex;
```

<img width="489" alt="ss15" src="https://github.com/inayy12/Latihan4/assets/115867315/3c18a30a-2d6c-47da-b8ba-c0a52c1d9bdf">

4. Tampilkan jumlah hewan berdasarkan spesies dan jenis kelamin.

```
SELECT species, sex, COUNT(*) as jumlah_hewan FROM hewan GROUP BY species, sex;
```

<img width="577" alt="ss16" src="https://github.com/inayy12/Latihan4/assets/115867315/1233632e-3bbc-4902-a943-b8a66599402a">

5. Tampilkan jumlah hewan berdasarkan spesis (cat dan dog saja)
dan jenis kelamin.

```
SELECT species, sex, COUNT(*) as jumlah_hewan
    -> FROM hewan
    -> WHERE species IN ('Cat', 'Dog')
    -> GROUP BY species, sex;
```

<img width="445" alt="ss17" src="https://github.com/inayy12/Latihan4/assets/115867315/54726d09-68cb-435d-a713-7f38f3560414">

6. Tampilkan jumlah hewan berdasarkan jenis kelamin yang diketahui
saja.

```
SELECT sex, COUNT(*) as jumlah_hewan
    -> FROM hewan
    -> WHERE sex IS NOT NULL
    -> GROUP BY sex;
```

<img width="356" alt="ss18" src="https://github.com/inayy12/Latihan4/assets/115867315/7c0439f2-55a9-4561-835b-86b0e295f4b6">


## Evaluasi dan Pertanyaan.
