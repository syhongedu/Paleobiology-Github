> 19/20

## Problem Set 1
1) `TriassicUnits <- read.csv("https://macrostrat.org/api/units?interval_name=Triassic&format=csv")`

2) 
````R
   nrow(TriassicUnits)
   [1] 838
````

3) 
   `TriassicUnits[1:10,]`
   
   These rocks are mostly igneous rocks and these rocks do not preserve fossils at all (since fossils    are going to be melt from the high heat of magma)

4) Column b_age is the starting age and t_age is the ending age of each unit

5) Every rocks are not only constrained by the Triassic. Some units are started from Triassic but it goes through other periods. Also, other units do not start from Triassic but have Triassic within their range.

##Problem Set 2

1) `TriassicUnits <- read.csv("https://macrostrat.org/api/units?lith_class=sedimentary&interval_unit=Triassic&format=csv")`

2) `TriassicUnitsRestricted <- TriassicUnits[which(TriassicUnits[,"b_age"]<=252.17&TriassicUnits[,"t_age"]>=201.3),]`

3) 
````R
Cretaceous <- read.csv("https://macrostrat.org/api/units?lith_class=sedimentary&interval_unit=Cretaceous&format=csv")
 -> CretaceousUnitsRestricted <- Cretaceous[which(Cretaceous[,"b_age"]<=145&Cretaceous[,"t_age"]>=66),]

   + Jurassic <- read.csv("https://macrostrat.org/api/units?lith_class=sedimentary&interval_unit=Jurassic&format=csv")
 -> JurassicUnitsRestricted <- Jurassic[which(Jurassic[,"b_age"]<=201.3&Jurassic[,"t_age"]>=145),]

   + Permian <- read.csv("https://macrostrat.org/api/units?lith_class=sedimentary&interval_unit=Permian&format=csv")
 ->  PermianUnitsRestricted <- Permian[which(Permian[,"b_age"]<=298.9&Permian[,"t_age"]>=252.17),]

   + Carboniferous <- read.csv("https://macrostrat.org/api/units?lith_class=sedimentary&interval_unit=Carboniferous&format=csv")
 ->  CarboniferousUnitsRestricted <- Carboniferous[which(Carboniferous[,"b_age"]<=358.9&Carboniferous[,"t_age"]>=298.9),]

   + Devonian <- read.csv("https://macrostrat.org/api/units?lith_class=sedimentary&interval_unit=Devonian&format=csv")
 ->  DevonianRestricted <- Devonian[which(Devonian[,"b_age"]<=419.2&Devonian[,"t_age"]>=358.9),]

   + Silurian <- read.csv("https://macrostrat.org/api/units?lith_class=sedimentary&interval_unit=Silurian&format=csv")
 ->  SilurianUnitsRestricted <- Silurian[which(Silurian[,"b_age"]<=443.8&Silurian[,"t_age"]>=419.2),]

   + Ordovician <- read.csv("https://macrostrat.org/api/units?lith_class=sedimentary&interval_unit=Ordovician&format=csv")
 ->  OrdovianUnitsRestricted <- Ordovician[which(Ordovician[,"b_age"]<=485.4&Ordovican[,"t_age"]>=443.8),]

4. UnitFreqs <- c(nrow(CretaceousUnitsRestricted),nrow(JurassicUnitsRestricted),nrow(TriassicUnitsRestricted),nrow(PermianUnitsRestricted),nrow(CarboniferousUnitsRestricted),nrow(DevonianRestricted),nrow(SilurianUnitsRestricted),nrow(OrdovianUnitsRestricted))
[1] 4588  998  604  903 3020 2059 1205 2161
````

5. 
````R
TriUnitFreqs <- c(nrow(CretaceousUnitsRestricted),nrow(JurassicUnitsRestricted),nrow(PermianUnitsRestricted),nrow(CarboniferousUnitsRestricted),nrow(DevonianRestricted),nrow(SilurianUnitsRestricted),nrow(OrdovianUnitsRestricted))
   mean(TriUnitFreqs)
   [1] 2133.429
   sd(TriUnitFreqs)
   [1] 1321.764
   (838-2133.429)/1321.764
   [1] -0.9800759
   Triassic Unit is  -0.9800759 sd below the mean
````

> No you did it backwards. -1 Points.

6) No I don't think Triassic Units are statistically lower in numbers of units than other periods. It's value is still below the mean, 0.9800759 doesn't seem to show significant difference than other units.

7) 
````R
   TriJurUnitFreqs <- c(nrow(CretaceousUnitsRestricted),nrow(PermianUnitsRestricted),nrow(CarboniferousUnitsRestricted),nrow(DevonianRestricted),nrow(SilurianUnitsRestricted),nrow(OrdovianUnitsRestricted))
   mean(TriJurUnitFreqs)
   [1] 2322.667
   sd(TriJurUnitFreqs)
   [1] 1340.022
  
   (838-2322.667)/1340.022
   [1] -1.107942
````

   Even though Triassic and Jurassic are considered as potential outliers, still it is not    statistically significant (Even though value is little bit increase though)   

## Problem Set 3
1)  
````R
URL2<-"https://macrostrat.org/api/columns?format=geojson_bare&project_id=1"   
    GotURL2<-getURL(URL2)
    NAMAP<-readOGR(GotURL2,"OGRGeoJSON",verbose=FALSE)
    plot(NAMAP,col=NA)
````

2)
````R
URL3 <- "https://macrostrat.org/api/columns?format=geojson_bare&interval_name=Olenekian&project_id=1"
   GotURL3<-getURL(URL3)
   OleMap <- readOGR(GotURL4,"OGRGeoJSON",verbose=FALSE)
   plot(OleMap,col="#B051A5",add=TRUE)
````

3) 
````R
DataPBDB <- downloadPBDB(Taxa=c("Animalia"),StartInterval="Induan",StopInterval="Anisian")
   points(DataPBDB[c("lng","lat")])
````

4)
````R
URL4 <- "https://macrostrat.org/api/columns?format=geojson_bare&interval_name=Lopingian&project_id=1"
   GotURL4 <- getURL(URL4)
   LopMap <- readOGR(GotURL4,"OGRGeoJSON",verbose=FALSE)
   plot(LopMap,col="#FBA794",add=TRUE)
````

5) 
````R
DataPBDB <- downloadPBDB(Taxa=c("Animalia"),StartInterval="Lopingian",StopInterval="Lopingian")
   points(DataPBDB[c("lng","lat")])
````

6. No. According the result I got, Early Triassic record does not show substantial drop in sedimentary rock unit numbers. Thus, with the result I got, the hypothesis is rejected. The lower diversity during Early Triassic does not mean an artefact of poor sampling or available sedimentary rock accoring to the data I get. However, the time span I used for Early Triassic is way longer than Lopingian that this data can be somewhat misdirected. 
