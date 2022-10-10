# OmegaTeam_JC_DS_LS_02_FinalProject
# DC Residential Properties
Team members:   
1. Faykel Nicandro Hattu
2. Muhammad Rafi Amiruddin  
3. Tamara Coglitore  

### Outline

* Business Problem
* Data Understanding
* Exploratory Data Analysis & Data Preprocessing
* Data Analysis
* Modeling
* Conclusion and Recommendation

## Business Problem

**Context**<br>  
   
Washington, D.C. adalah Ibu Kota dari Amerika Serikat dengan jumlah penduduk 689.545 dan memiliki jumlah tempat tinggal sebanyak 350.364 unit berdasarkan sensus tahun 2020 [(opendataDC)](https://opendata.dc.gov/). Sebagai kota pusat pemerintahan di Amerika Serikat, tidak dapat dipungkiri bila biaya hidup disana cukup tinggi dimana salah satunya adalah harga properti. Pada tahun 2017, rata-rata harga rumah pribadi (*single-family home*) di kota tersebut berada di kisaran $647.000, sedangkan harga rata-rata rumah di Amerika Serikat pada tahun yang sama berada di kisaran $399.700 [(FRED)](https://fred.stlouisfed.org/series/ASPUS). Meskipun hal ini menunjukkan tingginya harga rumah di Washington, D.C, wilayah tersebut secara konsisten menjadi salah satu pasar properti yang paling banyak diminati di Amerika Serikat [(Atlaslane)](https://www.atlaslane.com/post/investment-property-washington-dc-best-areas#:~:text=Washington%2C%20DC%20is%20consistently%20ranked,month%20when%20rent%20is%20collected.). Oleh karena itu, banyak perusahaan *real estate* seperti [The One Street](https://www.onestreet.one/), [GreenLine](https://www.greenlinere.com/), [Fulcrum Property](https://www.fulcrumproperty.com/), dan perusahaan lainnya yang ingin memanfaatkan peluang ini sehingga membuat persaingan bisnis di bidang *residential real estate* menjadi sangat kompetitif. Untuk dapat bersaing, Residential Real Estate Company perlu memberikan layanan yang optimal antara lain dengan memberikan penawaran harga terbaik dan sesuai dengan segmentasi pasar. 

Harga properti di Amerika cukup berdampak pada stabilitas ekonomi negara [(TheBalanceMoney)](https://www.thebalancemoney.com/how-does-real-estate-affect-the-u-s-economy-3306018), yang menyebabkan pemerintah juga turut menentukan dan mengatur kebijakan yang berdampak pada harga properti [(Fannie and Freddie)](https://www.chicagobooth.edu/review/should-government-intervene-housing-market). Sehingga untuk memberikan penawaran harga, kita perlu mengikuti kebijakan dan kualifikasi dari pemerintah. 
   
Selain mengikuti kebijakan pemerintah, survey terhadap properti residential juga perlu dilakukan untuk memperkirakan harga yang tepat. Namun, seperti yang dikutip dilaman Department of Consumer and Regulatory Affairs Washington, D.C., proses survey secara konvensional memakan biaya yang cukup besar [(Angi)](https://www.angi.com/articles/how-much-does-land-survey-cost.htm) serta memakan waktu yang cukup lama. Selain itu, metode konvensional seperti survey berpotensi terjadinya *overpriced* dan *underpriced*.
   
Perusahaan juga perlu mengetahui segmentasi properti residential untuk diberikan ke target market tertentu sebagai penunjang Department Marketing perusahaan. Strategi marketing dengan cara menawarkan rumah secara acak tanpa memberikan batasan tertentu dapat memberikan hasil yang kurang efektif. 
<br>

**Problem Statement**<br>
  
Survey yang dilakukan untuk memperkirakan harga properti residential cukup memakan waktu dan biaya. Selain itu, subjektifitas dalam penentuan harga jual oleh surveyor dapat menyebabkan terjadinya *overpriced* dan *underpriced*. *Overpriced* maupun *underpriced* dapat merugikan perusahaan. Kasus *overpriced* dapat menyebabkan properti tersebut sulit terjual karena harga yang kurang bersaing, sedangkan pada kasus *underpriced* dapat menyebabkan *profit loss* [(CPG)](https://www.durangohomesforsale.com/blog/what-to-know-about-overpricing-or-underpricing-your-home/). Disamping itu, budget marketing akan menjadi kurang efisien jika perusahaan tidak mampu menentukan segmentasi properti dengan tepat. 
<br>

**Goals**<br>  
  
Dengan adanya permasalahan di atas, maka tujuan analisa yang dilakukan adalah sebagai berikut :
1. Memberikan prediksi harga properti residential dengan meminimalisir error sehingga tidak *overpriced* dan *underpriced*, serta mengurangi biaya dan waktu pengerjaan survey properti
2. Melakukan segmentasi properti untuk meningkatkan produktivitas Department Marketing

Dengan menggunakan pemodelan machine learning, permasalahan di atas bisa diselesaikan dengan cara yang lebih efisien dibandingkan dengan cara konvensional sehingga kinerja perusahaan meningkat.
<br>

**Analytic Approach**<br>
   
Pendekatan analitik yang dilakukan adalah dengan menganalisa data untuk dapat menemukan pola dari fitur-fitur yang ada. Akan dilakukan pembuatan, evaluasi, dan implementasi model machine learning regresi dan clustering sebagai *tool* yang dapat digunakan untuk memprediksi harga dan segmentasi properti residential.
<br>

**Metric**<br>
    
Evaluation metrics digunakan untuk mengukur performa atau kualitas model machine learning. Dengan menggunakan 2 model yang berbeda, maka metrik yang akan digunakan juga berbeda. 

Pada model machine learning regresi terdapat berbagai macam metrik yang digunakan, seperti MAE, MAPE, dan R-squared. MAE merupakan rata-rata nilai absolut dari error dan MAPE merupakan rata-rata persentase error. MAE dan MAPE merupakan metrik yang tidak sensitif terhadap outlier. Semakin rendah nilai MAE dan MAPE maka semakin akurat model dalam prediksi harga properti residential. Selain itu R-squared merupakan koefisien determinasi yang mengindikasi besarnya kombinasi variabel independen mempengaruhi variabel dependen. Nilai R-squared berkisar diantara 0 dan 1, dimana semakin tinggi nilai R-square maka semakin baik model regresi. R-squared hanya bisa digunakan pada model linear.

Pada model machine learning clustering, metrik yang dapat digunakan adalah Silhouette Score. Metrik digunakan untuk menentukan jumlah clustering yang optimal. Jumlah cluster yang ideal dengan metrik silhouette dilihat dari nilai koefisien dengan rentang -1 sampai 1. Nilai 1 menunjukkan nilai terbaik dimana data sangat compact pada clusternya, nilai 0 menunjukkan cluster saling tumpang tindih, dan nilai terburuk adalah -1. Silhouette score digunakan karena memiliki pendekatan yang lebih akurat dan *reliable* pada penentuan jumlah cluster.
