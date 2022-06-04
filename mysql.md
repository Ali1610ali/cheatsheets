CREATE DATABASE MuhammadAliMahdi105
CREATE TABLE `tabel karyawan` (
 `IDKARYAWAN` varchar(6) DEFAULT NULL,
 `NAMA` varchar(255) DEFAULT NULL,
 `ALAMAT` varchar(255) DEFAULT NULL
 ) ;
 
INSERT INTO `tabel karyawan` (IDKARYAWAN, NAMA, ALAMAT) 
values
('K1A023', 'Rita Rosita', 'Bandung'),
('K1A011', 'Nagib askar', 'Bogor'),
('K2B032', 'Ibrahim', 'Bekasi'),
('K2B453', 'Yusi Afriani', 'Tangerang'),
('K2B235', 'Aisyah', 'Tangerang');

CREATE TABLE `tabel gaji` (
 `IDKARYAWAN` varchar(6) DEFAULT NULL,
 `GOLONGAN` varchar(2) DEFAULT NULL,
 `GAJI POKOK` float DEFAULT NULL,
 `TUNJANGAN` float DEFAULT NULL
);

INSERT INTO `tabel gaji` (IDKARYAWAN, GOLONGAN, `GAJI POKOK`, TUNJANGAN) 
values
('K1A023', '1A', 3000000.0, 1500000.0),
('K1A011', '1A', 2500000.0, 1000000.0),
('K2B032', '2B', 2000000.0, 550000.0),
('K2B453', '2B', 2000000.0, 550000.0),
('K2B235', '2B', 2000000.0, 550000.0);
CREATE TABLE `tabel status` (
 `GOLONGAN` varchar(2) DEFAULT NULL,
 `STATUS` varchar(12) DEFAULT NULL
);

INSERT INTO `tabel status` (GOLONGAN, STATUS) 
values
('1A ', 'Tetap '),
('2B ', 'Honor ');
ALTER table `tabel karyawan` change IDKARYAWAN ID_KARYAWAN varchar(6);
alter table `tabel karyawan` add TELP varchar(14);
UPDATE `tabel karyawan` 
SET TELP=081234567890
WHERE ID_KARYAWAN='K1A023';
UPDATE `tabel karyawan` 
SET TELP=081234567891
WHERE ID_KARYAWAN='K1A011';
UPDATE `tabel karyawan` 
SET TELP=081234567892
WHERE ID_KARYAWAN='K2B032';
UPDATE `tabel karyawan` 
SET TELP=081234567893
WHERE ID_KARYAWAN='K2B453';
UPDATE `tabel karyawan` 
SET TELP=081234567894
WHERE ID_KARYAWAN='K2B235';
