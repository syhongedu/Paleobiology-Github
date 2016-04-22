## Problem Set 1

> 20/20

1) West

2) 

   + `col= function` -> enables coloring in the map
   + `lty= function` -> decides line type for the map
   + `add= function` -> decides whether you are going to add additional plot on the map or not. 
   + `rgb() function` -> gives RGB color specification to the plot. (1,0,0) for red, (0,1,0) for blue, (0,0,1) for green
   + `plot() function` -> plot the map with the codes in it    

3) `AlbianMap <- downloadPaleogeography(Age=110)`
4) `plot(AlbianMap,col=rgb(0,1,0,0.33),lty=0,add=TRUE)`
5) North and eastward movement since the Albian
6) <strike>South</strike> and westward movement since the Albian

## Problem Set 2
1) 

   ````R
   PEMap <- downloadPaleogeography(Age=56)
   plot(PEMap,col=rgb(0,0,1,0.5),lty=0.01)
   ````

2) DataPBDB <- downloadPBDB(Taxa=c("Anthozoa"),StartInterval="Paleocene",StopInterval="Eocene")

3) 2847 occurrences

4) 
   + `occurrence_no` -> unique number of the occurrence
   + `record_type` -> Type of the record
   + `reid_no` -> Unique identifier for the reidentification
   + `flags` -> A record which identification is superseded by a more recent identification
   + `collection_no` -> The identifier of the collection with which this occurrence is associated
   + `identified_name` -> The taxonomic name by which this occurrence was identified
   + `identified_rank` -> The taxonomic rank of the identified name
   + `identified_no` -> The unique identifier of the identified taxonomic name
   + `difference` -> Show reason why identified name is different from accepted name 
   + `accepted_name` -> Accepted taxonomic name of the identified name
   + `accepted_rank` -> The taxonomic rank of the accepted name
   + `accepted_no` -> The unique identifer of the accpeted taxonomic name in this database
   + `early_interval` -> The specific geologic time associated with the occurence
   + `late_interval` -> The interval ends the specific geologic time of the occurence 
   + `max_ma` -> The early bound of the geologic time range of the occurence
   + `min_ma` ->  The late bound of the geologic time range of the occurence
   + reference_no` -> The identifier of the reference from which this data was entered
   + `paleomodel` -> The primary model specified by the parameter pgm
   + `paleolng` -> The paleolongitude of the collection
   + `paleolat` -> The paleolatitude of the collection
   + `geolplate` -> The identifier of the geological plate on which the collection lies
   + `phylum` -> The name of the phylum which this identification is classified
   + `class` -> The name of the class which this identification is classified
   + `order` -> The name of the order which this identification is classified
   + `family` -> The name of the family which this identification is classified
   + `genus` -> The name of the genus which this identification is classified

5. `points(DataPBDB[c("paleolng","paleolat")])`

6. Most Anthozoa occurred in the Europe (Mostly Western Europe). Anthozoa are primarily marine organisms. Therefore, during Paleocene/Eocene boundary, Western Europe was submerged under the ocean.

## Problem Set 3

1) `DataPBDB <- downloadPBDB(Taxa=c("Perissodactyla"),StartInterval="Paleogene",StopInterval="Paleogene")`

2) They are odd-toed ungulates. Perissodactyla includes Tapir, horses, and rhinoceros.

3) `DataPBDB[which(DataPBDB[,"collection_no"]==112723),]`

4) "geoplate" id is 501, this geoplate id is correspond to the modern Pakistan. 

5) `nrow(DataPBDB[which(DataPBDB[,"geoplate"]==501),])`
   84 occurrences

6) Region X has moved south and (slightly) westward direction from Albian to the present day.

7) 
+ Scenario 1: Species of Perissodactyla migrated from region-X to China during the Paleogene? 

Maybe plausible howerver not most part of the Paleogene. According to the Paleobiology Navigator tool, there are no Perissodactyla fossil records reported from Region X, but China, during 44 Ma. For now, this means that Perissodactyla is unlikely to migrate from region-X to China during Paleogene. However,one thing you need to remind is that Paleogene is long period. Even though region-X was separated from China for a long time, it was attached to the China later part of the Paleogene. Therefore, yes, there might be possibility that species of Perissodactyla migrated from region-X to China during Paleogene but not until the later part of the Paleogene.
   
   + Scenario 2: Species of Perissodactyla migrated from China to region-X during the Paleogene?
   
   More plausible scenario for me according to the data. Since most of Perissodactyla fossils discovered during Paleogene are located is China rather than region-X, it is likely that Perissodactyla migrated to the region-X first from China when Eurasia and India continents are collided. 
   
   + Scenario 3: The species of Perissodactyla in China and region-X are unrelated and probably both came from a third region?
   
   In a wider sense, it could be a case but this case is not likely for this Scenario. According to the Paleobiology Navigator, during Paleogene, there are already Perissodactyls at China. In wider sense, this Chinese Perissodactyls are derived from somewhere else in the globe but, just in case of Paleogene, it is already happened and I feel like I can't call it a third region anymore. 
