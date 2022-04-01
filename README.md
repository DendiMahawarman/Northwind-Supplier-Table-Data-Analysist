# Northwind-Supplier-Table-Data-Analysist
Northwind Database - Supplier Table Data Analysist

Permasalahan dari project ini yaitu untuk menemukan solusi pada sebuah perusahaan penjualan produk makanan khas berbagai negara agar dapat meningkatkan jumlah pemesanan produk dan jumlah pendapatan perusahaan. Database yang digunakan yaitu Northwind Database dengan tabel supplier untuk menemukan feature dari perusahaan - perusahaan penjualan produk makanan khas berbagai negara di dunia agar dapat diterapkan didalam perusahaan. Dari database tersebut, perusahaan ingin mendapatkan gambaran kondisi pasar saat ini, sehingga nantinya mereka dapat melakukan penerapan strategi bisnis yang tepat sasaran untuk memperoleh keuntungan bagi perusahaan

Database Information
Sumber Database : https://www.aspsnippets.com/Articles/Download-and-Install-Microsoft-Northwind-Sample-database-in-MySql.aspx

Database "Northwind Database.sql" terdiri dari 13 tabel, yaitu:

1. categories : menyimpan informasi tentang kategori dari jenis produk makanan
2. customercustomerdemo : null
3. customerdemographics : null
4. customers : menyimpan informasi tentang data lengkap pelanggan / customer
5. employees : menyimpan informasi tentang data pegawai yang berhubungan dengan penjualan kepada customer
6. employeeterritories : menyimpan informasi tentang data pembagian wilayah untuk masing - masing pegawai
7. orderdetails : menyimpan informasi tentang data penjualan untuk masing-masing order ID, seperti harga dan jumlah yang dibeli
8. orders : menyimpan informasi tentang data penjualan dan pengiriman produk, seperti tanggal pemesanan, tanggal pengiriman, serta informasi terkait pengiriman produk
9. products : menyimpan informasi tentang data produk, supplier yang menyediakan, harga produk hingga stock yang tersedia
10. region : menyimpan informasi tentang data region sesuai dengan region ID nya
11. shippers : menyimpan informasi tentang data ekspedisi pengiriman sesuai dengan shipper ID nya
12. suppliers : menyimpan informasi tentang data lengkap supplier / penyedia barang
13. territories : menyimpan informasi tentang data wilayah sesuai dengan territory ID nya

Tabel yang digunakan dalam project ini yaitu tabel Suppliers, Orders, OrderDetails, Products dan Shippers.

Feature yang digunakan dari 5 tabel tersebut yaitu:
1. SupplierID dari tabel suppliers
2. CompanyName dari tabel suppliers
3. City dari tabel suppliers
4. Country dari tabel suppliers
5. ProductID dari tabel products
6. ProductName dari tabel products
7. UnitPrice dari tabel products
8. UnitsInStock dari tabel products
9. UnitsOnOrder dari tabel products
10. ReorderLevel dari tabel products
11. Discontinued dari tabel products
12. OrderID dari tabel orderdetails
13. UnitPrice dari tabel orderdetails --> Dirubah menjadi BuyPrice untuk membedakan dengan UnitPrice dari tabel products
14. Quantity dari tabel orderdetails --> Dirubah menjadi BuyQuantity untuk membedakan dengan UnitInStock dari tabel products
15. OrderDate dari tabel orders
16. ShippedDate dari tabel orders
17. ShipVia dari tabel orders
18. Freight dari tabel orders
19. ShipCity dari tabel orders
20. ShipCountry dari tabel orders
21. CompanyName dari tabel shippers --> Dirubah menjadi ShipperCompanyName untuk membedakan dengan CompanyName dari tabel suppliers

Selain dari tabel, ditambahkan sebuah kolom yang dinamakan "Discount" yang merupakan selisih antara "UnitPrice" dari tabel products dan "UnitPrice" dari tabel orderdetails (BuyPrice).

Pada tahap data anomalies dilakukan cara-cara penanganan sebagai berikut:
1. Handling missing value dengan menghapus baris yang terdapat missing value
2. Handling false datatype dengan merubah datatype dari object ke numerik untuk feature yang seharusnya datatype numerik
3. Data Outlier dibiarkan karena jumlahnya sampai 10,3% signifikan terhadap data
4. Data duplicate tidak ada

Pada tahap data visualiasi dan analisis statistic bagian-bagian yang dianalisis yaitu:
1. Waktu Respon Pemesanan Oleh Supplier
2. Supplier dengan Pendapatan Tertinggi
3. Supplier dengan Pemesanan Tertinggi
4. Hubungan Pendapatan dan Pemesanan pada Supplier
5. Product dari Supplier yang Terlaris
6. Supplier dengan Pemberian Diskon Tertinggi
7. Hubungan Pemesanan dan Pemberian Diskon
8. Presentase Diskon pada Setiap Produk terhadap Harga Produk menggunakan uji normalitas shapiro wilk test dan uji perbandingan kruskal wallis test
9. Hubungan Waktu Respon dan Diskon dengan Jumlah Pendapatan menggunakan uji korelasi spearman
