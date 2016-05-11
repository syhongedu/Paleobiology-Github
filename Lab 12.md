[Problem Set 1]

> 20/20

1. TriassicSynapsids<-downloadPBDB("Synapsida","Anisian","Rhaetian")
   TriassicDiapsids<-downloadPBDB("Diapsida","Anisian","Rhaetian")
   JurassicDiapsids<-downloadPBDB("Diapsida","Jurassic","Neogene")
   JurassicSynapsids<-downloadPBDB("Synapsida","Jurassic","Neogene")

2. TriassicSynapsids<-cleanRank(TriassicSynapsids,"genus")
   nrow(TriassicSynapsids)
   [1] 357
   TriassicDiapsids<-cleanRank(TriassicDiapsids,"genus")
   nrow(TriassicDiapsids)
   [1] 2081

3. TJDsurvivors <- intersect(TriassicDiapsids[,"genus"],JurassicDiapsids[,"genus"]) 
   length(TJDsurvivors)
   [1] 36

   TJDvictims <- setdiff(TriassicDiapsids[,"genus"],JurassicDiapsids[,"genus"])
   length(TJDvictims)
   [1] 353

   TJSsurvivors <- intersect(TriassicSynapsids[,"genus"],JurassicSynapsids[,"genus"])
   length(TJSsurvivors)
   [1] 9

   TJSvictims <- setdiff(TriassicSynapsids[,"genus"],JurassicSynapsids[,"genus"])
   length(TJSvictims)
   [1] 107

4. TJoddsRation <- (length(TJDsurvivors)/(length(TJDsurvivors)+length(TJDvictims)))/(length(TJSsurvivors)/(length(TJSsurvivors)+length(TJSvictims)))
   [1] 1.192802
   log(TJoddsRation)
   [1] 0.1763052

5. TJStandardError <- sqrt(1/length(TJDsurvivors)+1/length(TJDvictims)+1/length(TJSsurvivors)+1/length(TJSvictims))
  TJStandardError
  [1] 0.3886741

  UpperLimit <- log(TJoddsRation) + (TJStandardError*1.96)
  UpperLimit
  [1] 0.9381064

  LowerLimit <- log(TJoddsRation) - (TJStandardError*1.96)
  LowerLimit
  [1] -0.585496
  => According to the data, lower limit of the data shows negative value. This means my result is not   statistically significant.

[Problem Set 2]
1.  TriassicSyanpsidsDiapsids<-downloadPBDB(c("Diapsida","Synapsida"),"Anisian","Rhaetian")
    JurassicSyanpsidsDiapsids<-downloadPBDB(c("Diapsida","Synapsida"),"Jurassic","Neogene")

2. MeanLatitudes <- tapply(TriassicSyanpsidsDiapsids[,"paleolat"],TriassicSyanpsidsDiapsids[,"genus"],mean)

3.  TJBSurvivors <- subset(TriassicSyanpsidsDiapsids,TriassicSyanpsidsDiapsids[,"genus"]%in%unique(JurassicSyanpsidsDiapsids[,"genus"])==TRUE)
    TJBSurvivors <- unique(TriassicSyanpsidsDiapsids[,"genus"])

    TJBVictims <- subset(TriassicSyanpsidsDiapsids,TriassicSyanpsidsDiapsids[,"genus"]%in%unique(JurassicSyanpsidsDiapsids[,"genus"])!=TRUE)
    TJBVictims <- unique(TJBVictims[,"genus"])

4.  TriassicDiapsids <- subset(TriassicSyanpsidsDiapsids,TriassicSyanpsidsDiapsids[,"genus"]%in%unique(TriassicDiapsids["genus"])==TRUE)
TriassicDiapsids <- unique(TriassicDiapsids[,"genus"])

    TriassicSynapsids <- subset(TriassicSyanpsidsDiapsids,TriassicSyanpsidsDiapsids[,"genus"]%in%unique(TriassicSynapsids["genus"])==TRUE)
TriassicSynapsids <- unique(TriassicSynapsids[,"genus"])

5. TJB <- array(0,dim=length(TJBVictims),dimnames=list(TJBVictims))
   FinalMatrix <- merge(MeanLatitudes,TJB,all=TRUE,by="row.names")
   FinalMatrix <- transform(FinalMatrix,row.names=Row.names,Row.names=NULL)
   colnames(FinalMatrix) <- c("MeanLatitudes","Survivor/Victim")
   FinalMatrix[is.na(FinalMatrix[,"Survivor/Victim"]),]<-1
   Regression <- glm(FinalMatrix[,"Survivor/Victim"]~FinalMatrix[,"MeanLatitudes"],family="binomial")
   summary(Regression)
 According to the data, for every one degree increase in the latitude of the genus, its odds of having survived T/J increases by 0.000774. This value is somewhat low, in my opinion. Therefore, I don't think mean latitude of a Triassic genus is a good predictor of it survival.
 
[Extra Credit]
Idontknow <- array(0,dim=length(TJBVictims),dimnames=list(TJBVictims))
Iamsorry <- array(0,dim=length(TriassicDiapsids),dimnames=list(TriassicDiapsids))
IsitFinalMatrix <- merge(MeanLatitudes,Idontknow,all=TRUE,by="row.names")
IsitFinalMatrix<-transform(IsitFinalMatrix,row.names=Row.names,Row.names=NULL)

Maybe <- merge(IsitFinalMatrix,Iamsorry,all=TRUE,by="row.names")
Maybe <- transform(Maybe,row.names=Row.names,Row.names=NULL)
colnames(Maybe) <- c("MeanLatitudes","Survivor/Victim","Diapsid/Synapsid")

Maybe[is.na(Maybe[,"Survivor/Victim"]),]<-1







