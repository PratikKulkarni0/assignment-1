
Assignment-1-Q7 

import numpy as np
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns
%matplotlib inline


cars=pd.read_csv("Database/Q7.csv")
cars


Unnamed: 0	Points	Score	Weigh
0	Mazda RX4	3.90	2.620	16.46
1	Mazda RX4 Wag	3.90	2.875	17.02
2	Datsun 710	3.85	2.320	18.61
3	Hornet 4 Drive	3.08	3.215	19.44
4	Hornet Sportabout	3.15	3.440	17.02
5	Valiant	2.76	3.460	20.22
6	Duster 360	3.21	3.570	15.84
7	Merc 240D	3.69	3.190	20.00
8	Merc 230	3.92	3.150	22.90
9	Merc 280	3.92	3.440	18.30
10	Merc 280C	3.92	3.440	18.90
11	Merc 450SE	3.07	4.070	17.40
12	Merc 450SL	3.07	3.730	17.60
13	Merc 450SLC	3.07	3.780	18.00
14	Cadillac Fleetwood	2.93	5.250	17.98
15	Lincoln Continental	3.00	5.424	17.82
16	Chrysler Imperial	3.23	5.345	17.42
17	Fiat 128	4.08	2.200	19.47
18	Honda Civic	4.93	1.615	18.52
19	Toyota Corolla	4.22	1.835	19.90
20	Toyota Corona	3.70	2.465	20.01
21	Dodge Challenger	2.76	3.520	16.87
22	AMC Javelin	3.15	3.435	17.30
23	Camaro Z28	3.73	3.840	15.41
24	Pontiac Firebird	3.08	3.845	17.05
25	Fiat X1-9	4.08	1.935	18.90
26	Porsche 914-2	4.43	2.140	16.70
27	Lotus Europa	3.77	1.513	16.90
28	Ford Pantera L	4.22	3.170	14.50
29	Ferrari Dino	3.62	2.770	15.50
30	Maserati Bora	3.54	3.570	14.60
31	Volvo 142E	4.11	2.780	18.60


# mean
cars.mean()
Points     3.596563
Score      3.217250
Weigh     17.848750
dtype: float64


# Median
cars.median()
Points     3.695
Score      3.325
Weigh     17.710
dtype: float64


# Mode
cars.Points.mode() 
0    3.07
1    3.92
dtype: float64
cars.Score.mode()
0    3.44
dtype: float64
cars.Weigh.mode()
0    17.02
1    18.90
dtype: float64


# Variance
cars.var()
Points    0.285881
Score     0.957379
Weigh     3.193166
dtype: float64


# Satndard Deviation
cars.std()
Points    0.534679
Score     0.978457
Weigh     1.786943
dtype: float64


# Range
cars.describe()
Points	Score	Weigh
count	32.000000	32.000000	32.000000
mean	3.596563	3.217250	17.848750
std	0.534679	0.978457	1.786943
min	2.760000	1.513000	14.500000
25%	3.080000	2.581250	16.892500
50%	3.695000	3.325000	17.710000
75%	3.920000	3.610000	18.900000
max	4.930000	5.424000	22.900000


Points_Range=cars.Points.max()-cars.Points.min()
Points_Range
2.17


Score_Range=cars.Score.max()-cars.Score.min()
Score_Range
3.9109999999999996


Weigh_Range=cars.Weigh.max()-cars.Weigh.min()
Weigh_Range
8.399999999999999


f,ax=plt.subplots(figsize=(15,5))
plt.subplot(1,3,1)
plt.boxplot(cars.Points)
plt.title('Points')
plt.subplot(1,3,2)
plt.boxplot(cars.Score)
plt.title('Score')
plt.subplot(1,3,3)
plt.boxplot(cars.Weigh)
plt.title('Weigh')
plt.show()

 
