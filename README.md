# NFTData_ResearchPaper

![image](https://github.com/ColdenJohnson/NFTData_ResearchPaper/assets/118926209/f4f27b9f-16e1-487e-9a73-54cf2504317f)


![image](https://github.com/ColdenJohnson/NFTData_ResearchPaper/assets/118926209/42aa818c-090f-4602-8ec8-16942e3d2788)


![image](https://github.com/ColdenJohnson/NFTData_ResearchPaper/assets/118926209/88efc18e-084b-4539-9e2f-0fce918b71af)


![image](https://github.com/ColdenJohnson/NFTData_ResearchPaper/assets/118926209/fc129124-db42-4407-ab1e-6ff98cc00672)


![image](https://github.com/ColdenJohnson/NFTData_ResearchPaper/assets/118926209/f3d9e76a-b465-4b01-9e13-745155e1b9b5)


![image](https://github.com/ColdenJohnson/NFTData_ResearchPaper/assets/118926209/cb236755-2d0f-486d-9367-c26f00add4f2)


![image](https://github.com/ColdenJohnson/NFTData_ResearchPaper/assets/118926209/74ac3f50-a762-4a97-a2ef-8939b52bef2e)


![image](https://github.com/ColdenJohnson/NFTData_ResearchPaper/assets/118926209/083908b8-0db0-4277-8e70-385b76907ec4)

Calls:
Model 1: lm(formula = Price_USD ~ anticipation_ratio + joy_ratio, data = NFT_data)
Model 2: lm(formula = Price_USD ~ anticipation_ratio + joy_ratio + Category, 
    data = NFT_data)
Model 3: lm(formula = Price_USD ~ anger + anticipation + disgust + fear + 
    joy + sadness + surprise + trust + negative + positive + 
    Category, data = NFT_data)

=======================================================================
                               Model 1       Model 2       Model 3     
-----------------------------------------------------------------------
  (Intercept)                  303.707***    443.249***    422.820***  
                               (30.645)      (39.956)      (31.001)    
  anticipation_ratio           894.098***    569.164***                
                              (141.574)     (146.771)                  
  joy_ratio                  -1036.039***   -501.205**                 
                              (163.687)     (180.637)                  
  Category: Collectible/Art                 -102.060      -185.535**   
                                             (71.277)      (61.640)    
  Category: Games/Art                       -330.136***   -340.620***  
                                             (40.405)      (37.896)    
  Category: Metaverse/Art                    455.891**      71.388     
                                            (141.297)     (114.711)    
  Category: Other/Art                       -106.679      -184.413     
                                            (169.793)     (125.580)    
  Category: Utility/Art                      436.631       506.427*    
                                            (232.242)     (216.241)    
  anger                                                     -9.086     
                                                           (36.839)    
  anticipation                                             146.937***  
                                                           (25.066)    
    disgust                                                 -165.915***  
                                                           (31.711)    
  fear                                                      98.501**   
                                                           (30.665)    
  joy                                                     -179.146***  
                                                           (26.358)    
  sadness                                                   30.927     
                                                           (35.346)    
  surprise                                                  49.372     
                                                           (29.794)    
  trust                                                   -107.269***  
                                                           (23.804)    
  negative                                                  -1.500     
                                                           (26.798)    
  positive                                                  90.269***  
                                                           (15.704)    
-----------------------------------------------------------------------
  R-squared                      0.004         0.009         0.014     
  N                          20377         20377         25110         
=======================================================================
  Significance: *** = p < 0.001; ** = p < 0.01; * = p < 0.05  

Notice How Low the R-Squared is on this (despite p-values being significant)



Calls:
Model 1: lm(formula = positive_ratio ~ Category + negative_ratio, data = NFT_data)
Model 2: lm(formula = negative_ratio ~ Category + positive_ratio, data = NFT_data)

=============================================================
                                Model 1         Model 2      
                             --------------  --------------  
                             positive_ratio  negative_ratio  
-------------------------------------------------------------
  (Intercept)                     0.339***        0.227***   
                                 (0.002)         (0.002)     
  Category: Collectible/Art       0.160***        0.561***   
                                 (0.007)         (0.004)     
  Category: Games/Art             0.084***        0.019***   
                                 (0.003)         (0.002)     
  Category: Metaverse/Art         0.138***        0.003      
                                 (0.010)         (0.008)     
  Category: Other/Art            -0.022*         -0.031***   
                                 (0.011)         (0.009)     
  Category: Utility/Art          -0.125***       -0.116***   
                                 (0.016)         (0.013)     
  negative_ratio                 -0.564***                   
                                 (0.007)                     
  positive_ratio                                 -0.398***   
                                                 (0.005)     
-------------------------------------------------------------
  R-squared                       0.351           0.646      
  N                           20431           20431          
=============================================================
  Significance: *** = p < 0.001; ** = p < 0.01;   
                * = p < 0.05  

R-squared here is quite high here -- it seems as though category is actually quite a good predictor of positive/negative sentiment.

![image](https://github.com/ColdenJohnson/NFTData_ResearchPaper/assets/118926209/abbbc2c3-2399-489a-8b77-56e5660b42b9)

