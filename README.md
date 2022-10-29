# Digital Elevation Models (DEMs) dataset


## Format

## Pre-processing

In a first folder named "unprocessed_DEMs", the DEMs are provided without pre-processing, with the raw data from GEBCO. 

On the other hand, in the folder named "processed_DEMs", the instances have been pre-processed to locate the isolated maritime cells (elevation less than or equal to 0) in the middle of terrestrial cells (e.g. lakes or ponds) and to assign them an arbitrary elevation (9999 in this case) to facilitate the use of these instances in practical cases. This pre-processing was done by transforming the set of maritime cells of the grid into a graph and by subsequently carrying out a computation of the connected components (see He et al. [2] for more details). More precisely, each maritime cell is considered as a vertex and is connected by an edge with its 4 neighboring cells (west, east, south and north) if these are also maritime cells. Some might also have considered diagonal cells (northwest, northeast, southwest and southeast) as an alternative implementation choice. Finally, the largest major component is then retained as the maritime area of interest while the smaller ones are artificially "filled in".

In both cases, the files are named "*width_height_m.asc*" where $m \in \mathbb{N}$ is the number of effective maritime cells.

## Visualisations

The different unprocessed DEMs of the dataset are illustrated below with $i \in \mathbb{N}$ the number of isolated maritime cells, if any.

### $15 \times 15$

---

#### $m = 105$

![15_15_105](https://github.com/owein-thuillier/geographical_instances/blob/main/visualisations/15_15_105.PNG)

#### $m = 125$

![15_15_125](https://github.com/owein-thuillier/geographical_instances/blob/main/visualisations/15_15_125.PNG)

#### $m = 146$

![15_15_146](https://github.com/owein-thuillier/geographical_instances/blob/main/visualisations/15_15_146.PNG)

### $20 \times 20$

---

#### $m = 187$

![20_20_187](https://github.com/owein-thuillier/geographical_instances/blob/main/visualisations/20_20_187.PNG)

#### $m = 234$

![20_20_234](https://github.com/owein-thuillier/geographical_instances/blob/main/visualisations/20_20_234.PNG)

#### $m = 291$

![20_20_291](https://github.com/owein-thuillier/geographical_instances/blob/main/visualisations/20_20_291.PNG)

### $25 \times 25$

---

#### $m = 336$

![25_25_336](https://github.com/owein-thuillier/geographical_instances/blob/main/visualisations/25_25_336.PNG)

#### $m = 419$

![25_25_419](https://github.com/owein-thuillier/geographical_instances/blob/main/visualisations/25_25_419.PNG)

#### $m = 542$

![25_25_542](https://github.com/owein-thuillier/geographical_instances/blob/main/visualisations/25_25_542.PNG)

### $50 \times 50$

---

#### $m = 937$

![50_50_937](https://github.com/owein-thuillier/geographical_instances/blob/main/visualisations/50_50_937.PNG)

#### $m = 1455$

![50_50_1455](https://github.com/owein-thuillier/geographical_instances/blob/main/visualisations/50_50_1455.PNG)

#### $m = 2304$

![50_50_2304](https://github.com/owein-thuillier/geographical_instances/blob/main/visualisations/50_50_2304.PNG)

### $75 \times 75$

---

#### $m = 3090$; $i = 7$

![75_75_3083](https://github.com/owein-thuillier/geographical_instances/blob/main/visualisations/75_75_3083.PNG)

#### $m = 4169$; $i = 1$

![75_75_4169](https://github.com/owein-thuillier/geographical_instances/blob/main/visualisations/75_75_4169.PNG)

#### $m = 5343$

![75_75_5343](https://github.com/owein-thuillier/geographical_instances/blob/main/visualisations/75_75_5343.PNG)

### $100 \times 100$

---

#### $m = 6361$; $i = 1$

![100_100_6361](https://github.com/owein-thuillier/geographical_instances/blob/main/visualisations/100_100_6361.PNG)

#### $m = 7527$; $i = 3$

![100_100_7527](https://github.com/owein-thuillier/geographical_instances/blob/main/visualisations/100_100_7527.PNG)

#### $m = 8947$

![100_100_8947](https://github.com/owein-thuillier/geographical_instances/blob/main/visualisations/100_100_8947.PNG)

### $125 \times 125$

---

#### $m = 10506$; $i = 16$

![125_125_10506](https://github.com/owein-thuillier/geographical_instances/blob/main/visualisations/125_125_10506.PNG)

#### $m = 12224$

![125_125_12224](https://github.com/owein-thuillier/geographical_instances/blob/main/visualisations/125_125_12224.PNG)

#### $m = 14239$

![125_125_14239](https://github.com/owein-thuillier/geographical_instances/blob/main/visualisations/125_125_14239.PNG)

### $150 \times 150$

---

#### $m = 15525$

![150_150_15525](https://github.com/owein-thuillier/geographical_instances/blob/main/visualisations/150_150_15525.PNG)

#### $m = 17036$; $i = 10$

![150_150_17036](https://github.com/owein-thuillier/geographical_instances/blob/main/visualisations/150_150_17036.PNG)

#### $m = 18948$

![150_150_18948](https://github.com/owein-thuillier/geographical_instances/blob/main/visualisations/150_150_18948.PNG)

### $175 \times 175$

---

#### $m = 20684$; $i = 9$

![175_175_20684](https://github.com/owein-thuillier/geographical_instances/blob/main/visualisations/175_175_20684.PNG)

#### $m = 24196$; $i = 17$

![175_175_24196](https://github.com/owein-thuillier/geographical_instances/blob/main/visualisations/175_175_24196.PNG)

#### $m = 26443$

![175_175_26443](https://github.com/owein-thuillier/geographical_instances/blob/main/visualisations/175_175_26443.PNG)

## References

[1] GEBCO Bathymetric Compilation Group, 2022. The GEBCO 2022 grid - a continuous terrain model of the global oceans and land. doi:10.5285/e0f0bb80-ab44-2739-e053-6c86abc0289c.

[2] He, L., Ren, X., Gao, Q., Zhao, X., Yao, B., Chao, Y., 2017. The connected-component labeling problem: A review of state-of-the-art algorithms. Pattern Recognition 70, 25–43. doi:10.1016/j.patcog.2017.04.018.
