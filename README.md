#TASK 1
İBB_WİFİ_LOCATİON
#Kütüphanelerin Tanıtılması

import pandas as pd
import numpy as np

#Gerekli Veri Manipülasyonalarının yapılması

df = pd.read_csv("Desktop/ibb_proje/ibb_wifi_location.csv")

print(df.shape)

(3927, 6)


print(df.columns)

Index(['LOCATION_GROUP', 'LOCATION_TYPE', 'LOCATION_CODE', 'LOCATION',
       'LONGITUDE', 'LATITUDE'],
      dtype='object')
      
      
 print(df.dtypes) 
 
 LOCATION_GROUP     object
LOCATION_TYPE      object
LOCATION_CODE      object
LOCATION           object
LONGITUDE         float64
LATITUDE          float64
dtype: object
 
 df.head()
 
 LOCATION_GROUP	LOCATION_TYPE	LOCATION_CODE	LOCATION	LONGITUDE	LATITUDE
0	Hizmet Binasi	Bina	METRO-T4 Habipler	ARNAVUTKÖY	28.843808	41.122220
1	Hizmet Binasi	Bina	059-Arnavutkoy Mezarliklar	ARNAVUTKÖY	28.751046	41.179543
2	Hizmet Binasi	Bina	001-Atasehir Darulaceze Tip Merkezi	ATAŞEHİR	29.147271	40.977937
3	Hizmet Binasi	Bina	001-Cobancesme Kurumsal Atik	BAHÇELİEVLER	28.825496	40.997055
4	Hizmet Binasi	Bina	061-Bahcelievler Yol Bakim	BAHÇELİEVLER	28.825249	40.997040


df.describe()


	LONGITUDE	LATITUDE
count	3927.000000	3927.000000
mean	6.941840	9.842478
std	12.365292	17.522992
min	0.000000	0.000000
25%	0.000000	0.000000
50%	0.000000	0.000000
75%	0.000000	0.000000
max	41.093551	41.477258



df.info()

<class 'pandas.core.frame.DataFrame'>
RangeIndex: 3927 entries, 0 to 3926
Data columns (total 6 columns):
 #   Column          Non-Null Count  Dtype  
---  ------          --------------  -----  
 0   LOCATION_GROUP  3927 non-null   object 
 1   LOCATION_TYPE   3927 non-null   object 
 2   LOCATION_CODE   3927 non-null   object 
 3   LOCATION        3927 non-null   object 
 4   LONGITUDE       3927 non-null   float64
 5   LATITUDE        3927 non-null   float64
dtypes: float64(2), object(4)
memory usage: 184.2+ KB


df.groupby("LOCATION").mean()


 LONGITUDE	LATITUDE
LOCATION		
ADALAR	29.131422	40.873475
ARNAVUTKÖY	28.707349	41.224597
ATAŞEHİR	26.884001	40.896995
AVCILAR	28.683097	40.936909
BAHÇELİEVLER	28.824813	40.982216
BAKIRKÖY	28.826252	40.978428
BAYRAMPAŞA	28.898470	41.048294
BAĞCILAR	28.850837	41.037127
BAŞAKŞEHİR	28.757981	41.089375
BEYKOZ	29.723793	41.122387
BEYLİKDÜZÜ	28.627380	41.006140
BEYOĞLU	28.939611	41.038301
BEŞİKTAŞ	29.016501	41.059068
Belnet Otobus	0.000000	0.000000
BÜYÜKÇEKMECE	28.540992	41.023042
ESENLER	28.880801	41.042792
ESENYURT	28.760342	41.015133
EYÜPSULTAN	28.925212	41.074791
FATİH	28.931040	41.014081
GAZİOSMANPAŞA	28.904319	41.072815
GÜNGÖREN	28.878128	41.018851
IETT Metrobus	0.000000	0.000000
IETT Otobus	0.000000	0.000000
KADIKÖY	28.850591	40.904254
KARTAL	29.188596	40.869015
KAĞITHANE	28.945436	41.074215
KÜÇÜKÇEKMECE	28.765819	41.012745
MALTEPE	29.144158	40.930194
PENDİK	29.263207	40.858790
SANCAKTEPE	29.219555	41.000165
SARIYER	29.031834	41.141653
SULTANBEYLİ	29.259355	40.934725
SULTANGAZİ	28.872026	41.100987
Sehir Hatlari Vapuru	0.000000	0.000000
SİLİVRİ	28.221410	41.128121
TUZLA	29.316717	40.853723
ZEYTİNBURNU	28.904080	41.007116
ÇATALCA	28.435832	41.258919
ÇEKMEKÖY	29.236925	41.048874
ÜMRANİYE	29.123383	41.026196
ÜSKÜDAR	29.035678	41.024274
İSTANBUL	0.000000	0.000000
ŞİLE	29.636053	41.112340
ŞİŞLİ	28.945931	41.059142
      
      
      
       code_show = !code_show
} 
$( document ).ready(code_toggle);
</script>
The raw code for this IPython notebook is by default hidden for easier reading.
To toggle on/off the raw code, click <a href="javascript:code_toggle()">here</a>.''')
      
