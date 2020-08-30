# Gender-Recognition-by-Voice

This database was created to identify a voice as male or female, based upon acoustic properties of the voice and speech. The dataset consists of 3,168 recorded voice samples, collected from male and female speakers. The voice samples are pre-processed by acoustic analysis in R using the seewave and tuneR packages, with an analyzed frequency range of 0hz-280hz.


*The following acoustic properties of each voice are measured and included within the CSV:

-meanfreq: mean frequency (in kHz)

-sd: standard deviation of frequency

-median: median frequency (in kHz)

-Q25: first quantile (in kHz)

-Q75: third quantile (in kHz)

-IQR: interquantile range (in kHz)

-skew: skewness (see note in specprop description)

-kurt: kurtosis (see note in specprop description)

-sp.ent: spectral entropy

-sfm: spectral flatness

-mode: mode frequency

-centroid: frequency centroid (see specprop)

-peakf: peak frequency (frequency with highest energy)

-meanfun: average of fundamental frequency measured across acoustic signal

-minfun: minimum fundamental frequency measured across acoustic signal

-maxfun: maximum fundamental frequency measured across acoustic signal

-meandom: average of dominant frequency measured across acoustic signal

-mindom: minimum of dominant frequency measured across acoustic signal

-maxdom: maximum of dominant frequency measured across acoustic signal

-dfrange: range of dominant frequency measured across acoustic signal

-modindx: modulation index. Calculated as the accumulated absolute difference between adjacent measurements of fundamental frequencies divided by the frequency range

-label: male or female



The best model achieves 99% accuracy on the test set. According to a CART model, it appears that looking at the mean fundamental frequency might be enough to accurately classify a voice. However, some male voices use a higher frequency, even though their resonance differs from female voices, and may be incorrectly classified as female. To the human ear, there is apparently more than simple frequency, that determines a voice's gender.


*Step-by-Step Process::

1 ) Importing Various Modules and Loading the Dataset

2 ) Exploratory Data Analysis (EDA)

3 ) OutlierTreatment

4 ) Feature Engineering

5 ) Preparing the Data

6 ) Modelling

7 ) Parameter Tuning with GridSearchCV

