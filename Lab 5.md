> An important principle is coding is self-commenting code. This means using object/variable names that are descriptive of what is happening.

> 17/20

## Problem Set 1

1)

````R
BR <-BivalveAbundance[c("Miocene"),]
aa <- which(BR > 0)
NROW(aa)
Generic Richness: 634
````

2) 

````R
BP <- BrachiopodAbundance[c("Pliocene"),]
BB <- which(BB > 0)
max(BB)/sum(BB) = 0.08304598
````

> This is not the correct number, but the code looks correct so I will let it pass.

3) 

````R
Roxanne <- BrachiopodAbundance[c("Late Ordovician"),]
Emery <- which(Roxanne > 0)
1-sum((array(Emery)/sum(Emery))^2)
0.9942574
````

> -1 points

4) 

````R
Live <- BivalveAbundance[c("Late Cretaceous"),]
Forever <- which(Live > 0)
-sum((array(Forever)/sum(Forever))*(log(array(Forever)/sum(Forever))))
6.038689
````

> -1 points

5) 

````R
MySaving <- BivalveAbundance[c("Paleocene"),]
Grace <- which(MySaving > 0)
-sum((array(Grace)/sum(Grace))*(log(array(Grace)/sum(Grace))))
5.469574
````

6) 9.42% difference, There was K/Pg extinction between Late Cretaceous and Paleocene. This extinction wiped away Mesozoic taxa and gave new away to the Cenozoic taxa. The 9% difference of Shannon's Entropy Value reflect this phenonmenon and reflected in Index. 

> 1 points. I would have given you partial credit if you showed you work.

7)


````R
# For No.4: exp(-sum((array(Forever)/sum(Forever))*(log(array(Forever)/sum(Forever)))))
             419.3428
# For No.5: exp(-sum((array(Grace)/sum(Grace))*(log(array(Grace)/sum(Grace)))))
             237.359
````   
   
After re-calculate the percent change with exponentiation of the Shannon's Entropies, I got 43.4% difference between Late Cretaceous and    Paleocene. This is much better 9.42% that I got only from the Shannon's Entropies value and actually, almost accurately, reflect the change       between the Late Cretaceous and Paleocene. I think the percent value is closer to the real value because you increase the number exponentially    to make them bigger to bring out more accurate results. Also, Hill's Number states Shannon's Entropy as e^(Shannon's Entropy) not just Shannon's    Entropy. 

## Problem Set 2

1) Gorgosaurus <- BivalveAbundance[c("Miocene"),]
   specnumber(Gorgosaurus,MARGIN=1)
   634  
   
2) Albertosaurus <- BrachiopodAbundance[c("Late Ordovician"),]
   diversity(Albertosaurus,index="simpson",MARGIN=1,base=exp(1))
   0.9784588
   
3) Tyrannosaurus <- BivalveAbundance[c("Late Cretaceous"),]
   diversity(Tyrannosaurus,index="shannon",MARGIN=1,base=exp(1))
   5.086512

4) Titanoboa <- BivalveAbundance[c("Paleocene"),]
   diversity(Titanoboa,index="shannon",MARGIN=1,base=exp(1))
   4.511063

> You didn't notice that you got different results here than above?

## Problem Set 3

1) 

````R
Vector1 <- c(42,48,87,56,66,81,51,111,88,70,99,104,160,191,156,101,151,242,217,202,270,393,573,403,512,355,634,534,498) <- Bivalve
Vector2 <- c(141,282,331,271,257,234,138,497,353,274,314,284,564,549,406,63,111,193,130,185,111,125,96,29,57,30,45,23,19) <- Brachiopo

cor(Vector2,Vector1)
-0.582002D
# Uncorrelated
````

> No, they are quite reasonably correlated. Please go back and reivew the section on correlation. -1 Points

2) 

```R
Vector3 <- array(YourOrder) <- Bivalve
Vector4 <- array(WhyMe) <- Brachiopod
cor(Vector4,Vector3)
   -0.2355608
Uncorrelated
````
> They are weakly negatively correlated. -0.5 points.

3) The greatest drop in brachiopod richness occurred between Lopinginan and Early Triassic

## Problem Set 4

1) 

````R
SampleAbundances<-apply(BrachiopodAbundance,1,sum)
SampleAbundances[which(SampleAbundances==min(SampleAbundances))]
StandardizedRichness<-apply(BrachiopodAbundance,1,subsampleIndividuals,Quota=63)
StandardizedRichness[1:29]
 Mississippian     Pennsylvanian  Early Ordovician Middle Ordovician 
         42.92             34.42             38.15             45.78 
 Late Ordovician        Llandovery           Wenlock            Ludlow 
         42.06             41.57             43.84             43.89 
       Pridoli    Early Devonian   Middle Devonian     Late Devonian 
         40.99             49.62             40.71             39.09 
    Cisuralian     Late Jurassic            Eocene   Late Cretaceous 
         50.89             34.40             26.75             28.64 
Early Cretaceous   Middle Jurassic         Paleocene         Lopingian 
         36.26             37.61             16.78             43.54 
Early Jurassic       Guadalupian   Middle Triassic     Late Triassic 
         30.22             51.06             32.93             36.96 
       Miocene    Early Triassic          Pliocene       Pleistocene 
         24.43             23.59             18.73             19.00 
     Oligocene 
         25.04 
````

2)

````R
(Standardized Richness)
TempStandardizedRichness<-StandardizedRichness[c("Early Ordovician","Middle Ordovician","Late Ordovician","Llandovery","Wenlock","Ludlow","Pridoli","Early Devonian","Middle Devonian","Late Devonian","Mississippian","Pennsylvanian","Cisuralian","Guadalupian","Lopingian","Early Triassic","Middle Triassic","Late Triassic","Early Jurassic","Middle Jurassic","Late Jurassic","Early Cretaceous","Late Cretaceous","Paleocene","Eocene","Oligocene","Miocene","Pliocene","Pleistocene")]
TempStandardizedRichness
 Early Ordovician Middle Ordovician   Late Ordovician        Llandovery 
            38.17             46.37             41.46             41.84 
          Wenlock            Ludlow           Pridoli    Early Devonian 
            43.68             43.84             41.03             49.85 
  Middle Devonian     Late Devonian     Mississippian     Pennsylvanian 
            41.51             38.68             42.41             34.20 
       Cisuralian       Guadalupian         Lopingian    Early Triassic 
            50.85             50.80             43.29             23.90 
  Middle Triassic     Late Triassic    Early Jurassic   Middle Jurassic 
            32.96             37.64             31.04             37.74 
    Late Jurassic  Early Cretaceous   Late Cretaceous         Paleocene 
            34.45             36.40             28.64             17.19 
           Eocene         Oligocene           Miocene          Pliocene 
            27.33             25.31             24.45             18.96 
      Pleistocene 
            19.00 

(Unstandaridzed Richness)
Outorder <- array(c(314,284,141,282,331,271,257,234,138,497,353,274,564,111,57,96,125,175,29,406,130,549,111,193,45,63,23,19,30),dimnames=list(c("Mississippian","Pennsylvanian","Early Ordovician","Middle Ordovician","Late Ordovician","Llandovery","Wenlock","Ludlow","Pridoli","Early Devonian","Middle Devonian","Late Devonian","Cisuralian","Late Jurassic","Eocene","Late Cretaceous","Early Cretaceous","Middle Jurassic","Paleocene","Lopingian","Early Jurassic","Guadalupian","Middle Triassic","Late Triassic","Miocene","Early Triassic","Pliocene","Pleistocene","Oligocene")))
Inorder <- Outorder[c("Early Ordovician","Middle Ordovician","Late Ordovician","Llandovery","Wenlock","Ludlow","Pridoli","Early Devonian","Middle Devonian","Late Devonian","Mississippian","Pennsylvanian","Cisuralian","Guadalupian","Lopingian","Early Triassic","Middle Triassic","Late Triassic","Early Jurassic","Middle Jurassic","Late Jurassic","Early Cretaceous","Late Cretaceous","Paleocene","Eocene","Oligocene","Miocene","Pliocene","Pleistocene")]
> Inorder
 Early Ordovician Middle Ordovician   Late Ordovician        Llandovery 
              141               282               331               271 
          Wenlock            Ludlow           Pridoli    Early Devonian 
              257               234               138               497 
  Middle Devonian     Late Devonian     Mississippian     Pennsylvanian 
              353               274               314               284 
       Cisuralian       Guadalupian         Lopingian    Early Triassic 
              564               549               406                63 
  Middle Triassic     Late Triassic    Early Jurassic   Middle Jurassic 
              111               193               130               175 
    Late Jurassic  Early Cretaceous   Late Cretaceous         Paleocene 
              111               125                96                29 
           Eocene         Oligocene           Miocene          Pliocene 
               57                30                45                23 
      Pleistocene 
               19 
````

Unstandardized Richness shows higher value than standardized richness. I think unstandardized one shows much higher value because of the inaccuracy due to the species-area effect. Therefore, sampling standardization would correct this inaccuracy and reduce the number into more correct value.

3) Unstandardized graph shows much better pattern than standardized graph when standardized graph shows more erratic pattern. Standardizing does standardize the mattter and I think this pattern is visible because standardizing "trim out" the inaccurate measurements from the unstandardized matters.

`````R
TempStandardizedRichness <-StandardizedRichness[c("Early Ordovician","Middle Ordovician","Late Ordovician","Llandovery","Wenlock","Ludlow","Pridoli","Early Devonian","Middle Devonian","Late Devonian","Mississippian","Pennsylvanian","Cisuralian","Guadalupian","Lopingian","Early Triassic","Middle Triassic","Late Triassic","Early Jurassic","Middle Jurassic","Late Jurassic","Early Cretaceous","Late Cretaceous","Paleocene","Eocene","Oligocene","Miocene","Pliocene","Pleistocene"

Inorder <- Outorder[c("Early Ordovician","Middle Ordovician","Late Ordovician","Llandovery","Wenlock","Ludlow","Pridoli","Early Devonian","Middle Devonian","Late Devonian","Mississippian","Pennsylvanian","Cisuralian","Guadalupian","Lopingian","Early Triassic","Middle Triassic","Late Triassic","Early Jurassic","Middle Jurassic","Late Jurassic","Early Cretaceous","Late Cretaceous","Paleocene","Eocene","Oligocene","Miocene","Pliocene","Pleistocene"

Forever<-Paradise[c("Early Ordovician","Middle Ordovician","Late Ordovician","Llandovery","Wenlock","Ludlow","Pridoli","Early Devonian","Middle Devonian","Late Devonian","Mississippian","Pennsylvanian","Cisuralian","Guadalupian","Lopingian","Early Triassic","Middle Triassic","Late Triassic","Early Jurassic","Middle Jurassic","Late Jurassic","Early Cretaceous","Late Cretaceous","Paleocene","Eocene","Oligocene","Miocene","Pliocene","Pleistocene")]

Yeahhh <-apply(BivalveAbundance,1,subsampleIndividuals,Quota=124)

plot(TempStandardizedRichness,Yeahhh)
plot(Inorder,Forever)
````

4) No. Because no pattern in standardized richness in Brachiopod and Bivavle is visible in the graph. In Unstandardized one, there was a clear relationship between two but in standardized one, there's none. So, it is hard to clearly say that Bivalve actually outcompeted Brachiopod over time with this richness graph.
