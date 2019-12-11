# CMSC 320 Final Tutorial
Tuan Le, Joseph Johnson, Andrew Thai

In [1]:

# Necessary libraries and imports to complete this tutorial
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
from scipy.stats import f
import seaborn as sns
from sklearn import model_selection
from sklearn import linear_model
from sklearn import preprocessing
from sklearn.preprocessing import LabelEncoder
import statsmodels.formula.api as smf
import warnings
warnings.filterwarnings('ignore')

In [2]:

data = pd.read_csv("top2018.csv")
data.head()

Out[2]:
	id 	name 	artists 	danceability 	energy 	key 	loudness 	mode 	speechiness 	acousticness 	instrumentalness 	liveness 	valence 	tempo 	duration_ms 	time_signature
0 	6DCZcSspjsKoFjzjrWoCd 	God's Plan 	Drake 	0.754 	0.449 	7.0 	-9.211 	1.0 	0.1090 	0.0332 	0.000083 	0.552 	0.357 	77.169 	198973.0 	4.0
1 	3ee8Jmje8o58CHK66QrVC 	SAD! 	XXXTENTACION 	0.740 	0.613 	8.0 	-4.880 	1.0 	0.1450 	0.2580 	0.003720 	0.123 	0.473 	75.023 	166606.0 	4.0
2 	0e7ipj03S05BNilyu5bRz 	rockstar (feat. 21 Savage) 	Post Malone 	0.587 	0.535 	5.0 	-6.090 	0.0 	0.0898 	0.1170 	0.000066 	0.131 	0.140 	159.847 	218147.0 	4.0
3 	3swc6WTsr7rl9DqQKQA55 	Psycho (feat. Ty Dolla $ign) 	Post Malone 	0.739 	0.559 	8.0 	-8.011 	1.0 	0.1170 	0.5800 	0.000000 	0.112 	0.439 	140.124 	221440.0 	4.0
4 	2G7V7zsVDxg1yRsu7Ew9R 	In My Feelings 	Drake 	0.835 	0.626 	1.0 	-5.833 	1.0 	0.1250 	0.0589 	0.000060 	0.396 	0.350 	91.030 	217925.0 	4.0
In [3]:

# Drop ID
data = data.drop(columns='id')
# Move Artists to the leftmost column

# Change duration_ms to something else
data.head()

Out[3]:
	name 	artists 	danceability 	energy 	key 	loudness 	mode 	speechiness 	acousticness 	instrumentalness 	liveness 	valence 	tempo 	duration_ms 	time_signature
0 	God's Plan 	Drake 	0.754 	0.449 	7.0 	-9.211 	1.0 	0.1090 	0.0332 	0.000083 	0.552 	0.357 	77.169 	198973.0 	4.0
1 	SAD! 	XXXTENTACION 	0.740 	0.613 	8.0 	-4.880 	1.0 	0.1450 	0.2580 	0.003720 	0.123 	0.473 	75.023 	166606.0 	4.0
2 	rockstar (feat. 21 Savage) 	Post Malone 	0.587 	0.535 	5.0 	-6.090 	0.0 	0.0898 	0.1170 	0.000066 	0.131 	0.140 	159.847 	218147.0 	4.0
3 	Psycho (feat. Ty Dolla $ign) 	Post Malone 	0.739 	0.559 	8.0 	-8.011 	1.0 	0.1170 	0.5800 	0.000000 	0.112 	0.439 	140.124 	221440.0 	4.0
4 	In My Feelings 	Drake 	0.835 	0.626 	1.0 	-5.833 	1.0 	0.1250 	0.0589 	0.000060 	0.396 	0.350 	91.030 	217925.0 	4.0
In [ ]:


