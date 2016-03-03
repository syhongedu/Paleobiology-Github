## Problem Set 1

> 18.6/20

1) Miocene -> 602
   Early Jurassic -> 169
   Late Cretaceous -> 375
   Pennsylvanian -> 133
   I used apply(PresencePBDB,1,sum)

2) 29, I used I used apply(PresencePBDB,1,sum) and counted them

3) Pridoli, Early Devonian, Cisuralian, Late Jurassic, Eocene, Late Cretaceous, Early Cretaceous, Middle Jurassic, Paleocene, Oligocene, Miocene, Early Jurassic, Pleistocene, Middle Jurassic, Late Triassic, Pliocene, Early Triassic. I used which(PresencePBDB[,"Mytilus"]==1)

4) Holocene, Lopingian, Guadalupian, Mississippian, Late Devonian, Middle Devonian, Compare occurrence in PBDB data and geologic timescale. Since Mytilus' timespan in PBDB data is Pridoli to Pleistocene, you can deduce out that missing epochs between Pridoli and Pleistocene are answer for this question. I also added Holocene because Mytilus still exists now.

## Problem Set 2
1) 0.8276423

> You didn't show how you got this. -1 points

2) 1 - 0.8276423 = 0.1723577

3) 0.1720779

4) 

````R
vegdist(NewMatrix,method="jaccard",binary=FALSE,diag=FALSE,upper=FALSE,na.rm=FALSE)

          Pleistocene   Pliocene    Miocene  Oligocene     Eocene
Pliocene   0.12692967                                            
Miocene    0.17207792 0.08496732                                 
Oligocene  0.26910299 0.18968386 0.16065574                      
Eocene     0.21870048 0.13397129 0.08585056 0.19063005           
Paleocene  0.44444444 0.37914692 0.33333333 0.41042345 0.33385827
````

Paleocene and Pleistocen are the most dissmiliar

## Problem Set 3
1) ````RandomEpochs <- PresencePBDB[c("Pliocene","Oligocene","Paleocene","Early Cretaceous","Late Jurassic","Middle Jurassic"),]````

2) ````vegdist(RandomEpochs, method="jaccard", binary=FALSE, diag=FALSE, upper=FALSE, na.rm=FALSE)````

3) Middle Jurassic - Late Jurassic - Early Cretaceous - Paleocene - Oligocene - Pliocene

4) Global Climate and geographic distance. Global climate and geographical distance would be different as the time goes further apart. This might create gradient between epochs.

> How can time-periods be more geographically distant from each other? -0.5 Points

5) Because K/Pg extinction wipe out most of Mesozoic taxa and replace with Paleocene taxa.

## Problem Set 4
1) ````Ordovician <- downloadPBDB(Taxa=c("Animalia"),StartInterval="Ordovician",StopInterval="Ordovician")````

2) ````Ordovician <- cleanGenus(Ordovician)````

3)

````R
CommunityMatrix <- presenceMatrix(Ordovician,SampleDefinition="geoplate")
CulledMatrix<-cullMatrix(CommunityMatrix,minOccurrences=2,minDiversity=25)
````

4) I used: 

````R
CulledMatrixDCA <- decorana(CulledMatrix,ira=0)
plot(CulledMatrixDCA,display="sites")
tapply(Ordovician[,"paleolat"],Ordovician[,"geoplate"],mean)
tapply(Ordovician[,"paleolon"],Ordovician[,"geoplate"],mean)
````

After I compared the plot and average of latitude or longitude, I found out that axis 1 or 2 and average lat/long are not related at all.
