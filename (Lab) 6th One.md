> 19/20

## Problem Set 1

1) 

````R
nrow(MacroPBDB)
[1] 9013
nrow(DataPBDB)
[1] 34166
-> 25153 occurrences are lost
````

2) Because Macrostrat database data are limited to certain continents: North America + Greenland + New Zealand + (some)sea cores

## Problem Set 2

1) 

````R
sort((specnumber(OrderMatrix,MARGIN=1)),decreasing=FALSE)
   CandidateUnits <- sort((specnumber(OrderMatrix,MARGIN=1)),decreasing=FALSE)[147:157]
    Harkless Fm       Forteau Fm     Parker Slate   Snowy Range Fm 
              14               14               16               16 
     Weymouth Fm      Langston Fm    Wheeler Shale Marjum Limestone 
              16               17               18               19 
      Stephen Fm       Kinzers Fm       Chancellor 
              23               24               27 
````           

2) 

````R
apply(GenusMatrix,2,sum)
sort(apply(GenusMatrix,2,sum))
GenusFrequencies <- sort(apply(GenusMatrix,2,sum))
````

3) table() code.

> -1 Points

4) Hollow Curve distribution

5) RareGenera <- GenusFrequencies[which(GenusFrequencies<= median(GenusFrequencies))]

## Problem Set 3

1) CandidateMatrix <- GenusMatrix[CandidateUnits,]

2) Weymouth Formation, Chancellor, Forteau Formation, Harkless Formation/I picked these formation because they have high percentage of genera in specific stratigraphic unit. Therefore, higher the number, higher the number of species in it. Since Lagerstatten is famous for showing its exquisite preservation and sample diversity, higher number would definitely show that these formations are Lagerstatten

3) Chancellor Basin, it is famous for including Burgess Shale Fossil Site, it is significant to Paleobiology because of its exquisite Lagerstatten and representing the Cambrian Explosion (assumed event which rapid diversification of animal taxon likely to happen based on fossil record). It also contains rare Cambrian Fauna which most of faunas only existed during Cambrian (exceptions like Trilobites).
