#Data Analysis: Airbnb Listing in Bangkok
## A. Latar Belakang & Tujuan Analisis

Analisis bisnis ini disusun untuk memberikan rekomendasi kepada Chief Business Officer (CBO) air bnb mengenai langkah-langkah bisnis yang perlu dilakukan oleh perusahaan untuk menjaga sustainability dan pertumbuhan bisnis ke depan. Salah satu tolak ukur yang mencerminkan pertumbuhan bisnis perusahaan adalah peningkatan revenue. Analisis ini akan berfokus pada bagaimana perusahaan dapat meingkatkan revenue ke depannya.

Sebagai pemilik platform dan juga pihak perantara, airbnb memiliki akses penuh terhadap seluruh database transaksi sewa-menyewa yang dilakukan melalui platform airbnb. Dengan memanfaatkan database tersebut, airbnb dapat memperoleh analisis komprehensif untuk menentukan langkah-langkah bisnis sebagai upaya untuk meningkatkan revenue ke depan.

## B. Airbnb Business Model

![image](https://github.com/user-attachments/assets/2ad769ae-545b-4888-83cc-28d63e9ce47b)

Air bnb merupakan marketplace yang menghubungkan pemilik tempat tinggal (hosts) dengan penyewa (travelers/visitors) melalui online platform yang dapat memfasilitasi proses transaksasi sewa-menyewa. Dari sudut pandang host, airbnb memungkinkan pemilik tempat tinggal untuk mendaftarkan tempat tinggal miliknya (disebut list) untuk memperoleh uang sewa. Sedangkan dari sudut visitor, air bnb menawarkan akses yang mudah untuk mencari, membandingkan, memilih dan menyewa tempat tinggal di berbagai belahan dunia.

Pada proses transaksi sewa-menyewa, Airbnb memperoleh penghasilan dari 2 sumber, yaitu:
1. Komisi dari host untuk setiap transaksi sebesar 3%-5%
2. Service fee dari visitor sebesar 6%-20% dari booking fee

Berdasarkan informasi di lapangan, banyak host airbnb yang bukan pemilik tempat tinggal dan bertindak hanya sebagai agen untuk si pemilik rumah. Dengan demikian, melalui analisis data terkini, airbnb dapat memberikan informasi kepada host mengenai tempat tinggal seperti apa yang paling diminati pelanggan. Dengan demikian, host (yang sebagian bertindak sebagai agen)  memiliki acuan dalam mencari bisnis baru.

## C. Business Problems and Workflow
Berdasarkan business model dari airbnb, peningkatan revenue dapat diperoleh dengan cara meningkatkan volume transaksi sewa-menyewa. Lalu, bagaimana cara untuk dapat meningkatkan volume transaksi?

Peningkatan volume transaksi dapat terjadi apabila supply dan demand memiliki keselarasan. Oleh karena itu, analisis akan difokuskan pada analisis supply vs demand. Berikut adalah proses analisis yang akan dilakukan:

1. Mengetahui bagaimana kondisi listing dari bisnis airbnb baik dari sudut pandang:
    - supply (ketersediaan listing)
    - current demand (jumlah review 12 bulan terakhir)
    - overall demand (jumlah review keseluruhan tahun)
    
    Note:
    - Overal demand dapat menggambarkan sustainability ke depan
    - Current demand dapat menggambarkan peluang pertumbuhan ke depan
    
1. Kondisi listing pada poin 1 dapat ditinjau dari beberapa aspek, yaitu:
    - Letak geografis (neighbourhood)
    - Room type
    - Range Harga
1. Analisis akan dilakukan dengan membandingkan supply dan demand untuk masing-masing aspek pada poin 2. Setelah itu, apabila terdapat gap di antara keduanya, maka akan ditinjau lebih lanjut apakah gap tersebut dapat menimbulkan konsekuensi / peluang bisnis yang dapat berdampak pada sustainability dan pertumbuhan revenue ke depannya.

## D. Data
**Data Source**

https://drive.google.com/drive/folders/1A_KBMRFTS5Mthpp46nulso679ML4ZwTF

**Kolom dan Deskripsi Kolom**
| Nama Kolom | Keterangan | Tipe Data |
| --- | --- | --- |
| name | Name of the listing | Kategorikal |
| id | Airbnb's unique identifier for the listing | Kategorikal |
| host_id | Airbnb's unique identifier for the host/user | Kategorikal |
| host_name | Name of the host. Usually, just the first name(s) | Kategorikal |
| neighborhood | The neighborhood is geocoded using the latitude and longitude against neighborhoods as defined by open or public digital shapefiles | Kategorikal |
| latitude | Uses the World Geodetic System (WGS84) projection for latitude and longitude | Float |
| longitude | Uses the World Geodetic System (WGS84) projection for latitude and longitude | Float |
| room_type | 1. Entire home/apt 2. Private room 3. Shared room or 4. Hotel | Kategorikal |
| price | Daily price in local currency. Note, the $ sign may be used despite the locale | Float|
| minimum_nights | The minimum number of night stays for the listing (calendar rules may differ) | Integer |
| number_of_reviews | The number of reviews the listing has | Integer |
| last_review | The date of the last/newest review | Datetime |
| reviews_per_month | Number of Reviews per Month | Float |
| calculated_host_listings_count | The number of listings the host has in the current scrape in the city/region geography | Integer |
| availability_365 |avaliability_x. The calendar determines the availability of the listing x days in the future. Note a listing may be available because it has been booked by a guest or blocked by the host | Integer |
| number_of_reviews_ltm | The number of reviews the listing has (in the last 12 months) |  Integer |



**Room Types Description**

*Entire place*: Entire places are best if you're seeking a home away from home. With an entire place, you'll have the whole space to yourself. This usually includes a bedroom, a bathroom, a kitchen, and a separate, dedicated entrance. Hosts should note in the description if they'll be on the property or not (ex: "Host occupies the first floor of the home") and provide further details on the listing.

*Private rooms* : Private rooms are great for when you prefer a little privacy, and still value a local connection. When you book a private room, you'll have your private room for sleeping and may share some spaces with others. You might need to walk through indoor spaces that another host or guest may occupy to get to your room.

*Shared rooms* : Shared rooms are for when you don't mind sharing a space with others. When you book a shared room, you'll be sleeping in a space that is shared with others and share the entire space with other people. Shared rooms are popular among flexible travelers looking for new friends and budget-friendly stays.

# E. Tahapan Analisis
![image](https://github.com/user-attachments/assets/eecfa1b3-102a-405a-aa78-ea281a831534)

# G. Summary and Business Recommendation

1. Walaupun listing tersebar di 50 disctrict, ketersediaan suatu room type terkonsentrasi di neighbourhood tertentu. 
2. Terdapat perbedaan demand antar room type, dimana shared room paling tidak diminati. Apabila memungkinkan, host dapat mengubah shared room menjadi private room. Selain itu, demand juga terkonsentrasi di neighbourhood tertentu saja untuk setiap room type.
3. Terdapat 2 listing yang paling diminati, yaitu:
    - Entire home/apt: Beautiful One Bedroom Apartment Near Skytrain yang dikelola oleh Suchada dan terletak di Phaya Thai
    - Private room: FREE PICK UP⭐BKK AIRPORT/BREAKFAST/PRIVATE DELUXE yang dikelola oleh Pailin dan terletak di Lat Krabang
4. Terdapat 2 listing dengan tipe private room di Bang Phlat yang jauh di atas harga pasar, yaitu id 22633450 dan id 629653142142561774 yang keduanya milik host Jeab dengan host_id 117057915.
5. Semakin tinggi harga, maka tingkat penetrasi pasar (peluang listing memperoleh penyewa) semakin rendah. Jika ingin mengejar volume transaksi, maka sebaiknya memperbanyak listing dengan Demand-Based Price Category Normal hingga High. Walaupun secara penetrasi pasar harga mempengaruhi, namun dari sisi jumlah review tidak terlalu mempengaruhi (korelasi lemah). Hal ini mengindikasikan bahwa penyewa cenderung mencoba tempat tinggal yang memiliki harga normal hingga high, namun tidak menentukan keputusannya untuk menginap di tempat yang sama.
6. List Peluang Bisnis

|Peluang Bisnis Berkembang|
|---|
|Hotel room di Lat Krabang|
|Entire home/apt di Khlong Tei, Vadhana dan Ratchathewi|
|Private room di Phra Nakhon|

7. List Bisnis yang Sustain

|Bisnis yang Sustain|
|---|
|Entire home/apt di Sathon|
|Hotel room di Phra Nakhon|
|Private room di Huai Khwang|

8. Shared room yang belum memperoleh penyewa di neighbourhood berikut dapat disarankan untuk mengubah menjadi private room:
- Bang Khen
- Bang Khun thain
- Bang Sue
- Chom Thong
- Lat Phrao
- Min Buri
- Phasi Charoen
- Saphan Sung
- Wang Thong Lang
- Yan na wa



