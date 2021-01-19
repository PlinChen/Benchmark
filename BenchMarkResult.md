[TOC] 
# BenchMark Result On WebGL
---
## Macbook Pro 
### Deveice Info
> OS Version ： macOS 10.15.7 (19H2)
> Processor ： Quad-Core Intel Core i7
> Graphics Card : AMD Radeon Pro 455 (2G) + Intel HD Graphics 530 (1.5G)
> Memory ： 16GB
> Browser ：MS Edge （ 86.0.622.56 ）
> Unity Editor ：2019.4


### Profile Result
|       | new EMCC & Split | new EMCC & No Split |   old EMCC|no resolve symbol|
|:------:|:------:|:-----:|:------:|:-----:|
|**Mandlebrot Script**|2260|29460|    33228||
| **Instantiate & Destroy**  |42708|45106|      43476||
| **CrytoHash Script**  |166167|210386|      198494||
| **Animation & Skinning**  |529|547|      566||
| **Asteroid Field**  |15676|17200|     15407 ||
| **Particles**  |116310|116110|      116650||
| **Physical Meshes**  |716|765|      761||
| **physical Cubes**  |757|795|      823||
| **Physical Spheres**  |1346|1723|     1714||
| **2D Physical Spheres**  |1752|2156|     2304| |  
| **2D Physical Boxes**  |1186|1379|      1351||
| **AI Agent**  |2110|2155|        2080||
| **TOTAL_POINTS**  |    |    |   ||
|**OVERALL_SCORE**   |88362|97180|       93454||

### LoadTime (ms)  (Test Twice)
| | new EMCC & Split | new EMCC & No Split  |old EMCC|
| :-------: | :-------: | :-------: | :-------: |
|Data|1115 / 263|93 / 182|950 / 238|
| Code  |1512 / 267|168 / 186|1086 / 239|
| Framework  |234 / 264|92 / 178|91 / 237|
|Time to Screen |12526 / 4200|2873 / 2863|4010 / 2845|
| Time to Interactive|465977 / 4245|2902 / 2946|4142 / 2922|
| Engine Initialization  |127 / 241|159 / 293|185 / 237|

---
## Windows  Desktop
### Deveice Info
> OS Version ： Win10 1909 
> Processor ： Intel(R) Core(TM) i7-9700K CPU @ 3.60GHz
> Graphics Card : NVIDIA GeForce RTX 2070
> Memory ： 16GB
> Browser ：MS Edge （ 86.0.622.58 ）
> Unity Editor ：2019.4

### Profile Result
|       | new EMCC & Split | new EMCC & No Split |   old EMCC|no resolve symbol|
|:------:|:------:|:-----:|:------:|:------:|
|**Mandlebrot Script**|3831|48451|49485||
| **Instantiate & Destroy**  |63691|67111|62087||
| **CrytoHash Script**  |175847|206258|202597||
| **Animation & Skinning**  |567|588|590691| |
| **Asteroid Field**  |18930|21643|20399||
| **Particles**  |162060|156140|165270||
| **Physical Meshes**  |958|1034|997||
| **physical Cubes**  |993|1134|1042||
| **Physical Spheres**  |2022|2414|2335||
| **2D Physical Spheres**  |2322|2741|2612||
| **2D Physical Boxes**  |1548|1661|1666||
| **AI Agent**  |2855|2820|2805||
| **TOTAL_POINTS**  |    |    |   ||
|**OVERALL_SCORE**   |112149|123442|119583||


### Load Time (ms)
| | new EMCC & Split | new EMCC & No Split  |old EMCC|
| :-------: | :-------: | :-------: | :-------: |
|Data|140|144|138|
| Code  |195|183|184|
| Framework  |63|55|57|
|Time to Screen |5383|2733|2817|
| Time to Interactive|5411|2746|2847|
| Engine Initialization  |113|144|178|

# Math Test On WebGL
## Time Cost (ms)
#### Mac Pro
| | new EMCC & Split | new EMCC & No Split  |old EMCC|
| :-------: | :-------: | :-------: | :-------: |
| UnityEngine.Mathf  |1289 / 1269|378 / 383|477 / 479|
|System.Math   |1553 /1663|661 / 655|772 / 757|
#### Win
| | new EMCC & Split | new EMCC & No Split  |old EMCC|
| :-------: | :-------: | :-------: | :-------: |
| UnityEngine.Mathf  |883 / 872|260 / 257|322 / 320|
|System.Math   |1069 / 1069|424 / 421|471 / 470|


# SinCos Test On WebGL
## Accuratable  & Time Cost Test

>System.Math.Sin 18.9  =  0.0504223068223244 
System.Math.Cos 18.9  =  0.998727986478158 

>Mathf.Sin 18.9  =  0.05042231 
Mathf.Cos 18.9  =  0.998728 

>DIY.Sin 18.9  =  0.05042131 
DIY.Cos 18.9  =  0.998728 

#### Mac Pro
| | new EMCC & Split | new EMCC & No Split  |old EMCC|
| :-------: | :-------: | :-------: | :-------: |
| UnityEngine.Mathf  |1260|389|473|
|System.Math   |1556|594|655|
| DIYTalor  | 304|323|   401|

#### Win
| | new EMCC & Split | new EMCC & No Split  |old EMCC|
| :-------: | :-------: | :-------: | :-------: |
| UnityEngine.Mathf  |821|247|310|
|System.Math   |961|373|431|
|DIYTalor   |203|  218  |271|