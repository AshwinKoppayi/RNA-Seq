R /path/to/sript/Rscript.R
getwd()
#Download the ftp links to the RNA Seq data from database(EBI,NCBI)
#For ease Copy the links to a seperate text files(ftplinks) if there are many files 
#Create a Rscript to download this files as follows
library(HelpersMG) #for wget function
links<-read.delim(file="ftplinks.txt",sep = ";",header=FALSE,col.names = c("1","2")) #For paired end reads
links<-read.delim(file="ftplinks.txt",sep = ";",header=FALSE,col.names = c("1")) #For single end reads
links[] <- lapply(links, function(x) paste("ftp://", x, sep="")) #Use only when the links dont have complete web address
for (i in 1:nrow(links)){
  wget(links[i,1])
  wget(links[i,2])
                        } #For paired end read
 for (i in 1:nrow(links)){
  wget(links[i,1])
                         } #For single end read 
                        
#Fin
