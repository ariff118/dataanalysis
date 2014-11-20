## APPROPRIATE STATISTICS FOR ORDINAL DATA 

#### DISTRIBUTION OVERVIEW 
* Bar graphs [discrete data] 
* Histograms [continuous data] 
* Frequency polygons 
* Cumulative frequency 
* Cumulative percentage 

#### CENTRAL TENDENCY 
* Mode [discrete] 
* Median [more stable than mode] 

#### DISPERSION 
* Inter-percentile ranges 
* Position 
* Ranks 
* Percentile ranks 

The ordinal measurement scale groups objects into classes but each class has a relative but
non-quantified relationship to each other class. An example would be a relative scale of
measurement of the preservation of furniture into poorly preserved, moderately preserved, well
preserved and excellently preserved. 

Multi-state counts on the ordinal data categories can be described by bar graphs when discrete
and by histograms when continuous. However, grouped frequency, cumulative frequency, and
percentage graphs also can be used, because adjacent categories are related. It should be
remembered that the horizontal distances between points in such graphs are arbitrary. The ordinal
scale can be transformed by any increasingly monotonic function. 

#####*CENTRAL TENDENCY*
Multi-state counts on discrete data can use the statistical mode() as a measure of central
tendency, however median() is generally a better predictor because it is more stable than the
mode, as more data is added. Moreover, the mode is dependent upon the size of the class
interval used and the starting point of the individual classes. 

#####*DISPERSION*
Because measurements on an ordinal scale take into account the order of the classes the
essential statistic for measuring dispersion is the Range [measured as MAX-MIN or MAX-MIN+1]

The variability can be measured by the various Quartile and Percentile statistics. The units of
measurement are those of the original observations. Because of the problem associated with not
knowing the distance between classes on the ordinal scale the calculated statistics of quartile
ranges are less preferable than an actual written statement, such as "one fourth of the
measurements had scores below 15 microns and one fourth had scores above 125 microns)". 

*Position*	
With the ordinal scale measurement adjacent observations can be ranked from 1 to n simply by
calling the lowest score 1, the second lowest 2, and so on till n is reached. A more meaningful
measure actually takes into account the size of n and is the percentage rank measured by
[rank/n] * 100. Computationally, this is done by: 

>quantile(idall$clay, na.rm=T) # the R function quantile produces the major percentiles. 
0% 25% 50% 75% 100% 
1 4 13 39 80 
>quantile(idall$clay, c(0.25, 0.75), na.rm=T) # produce the 25th and 75th percentile. NA's are removed. 
25% 75% 
4 39 
>quantile(idall$clay, c(0.07, 0.63), na.rm=T) # produce the 7th and 63rd percentile. 
7% 63% 
1.0 24.2 

#####*ASSOCIATION* 
Spearman's r can be used to test the relationship between a predictor and dependent variable for
a single sample; and, with multiple samples more tests are available depending upon whether or
not the samples are independent. If the samples are independent the Mann-Whitney test for two
samples or the Kruskal-Wallis H for multiple samples, are available. For dependent samples the
Wilcox T is used for two samples and the ANOVA by ranks [Friedman] for multiple samples.
Later, a variety of regression methods are discussed that have been applied to ordinal data-
frames: logistic regression, PROBIT regression, Weighted Lease Squares [WLS], and Diagonal
Least Squares [DWLS].



If your data is a closed array [percentages] it is in SIMPLEX SPACE not EUCLEIDEAN SPACE
therefore it is wise to transform it using something like an isometric log ratio transformation.

_written by:_
_George Hart,_
_Professor emeritus,_
_Geology/Geophysics, LSU_