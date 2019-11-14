# Assignment-05
if (!require("data.table")) install.packages("data.table")
library("data.table")
  header <- read.table("yellow_tripdata_2017-06.csv", header = TRUE,
                       sep=",", nrow = 1)
  DF <- fread("yellow_tripdata_2017-06.csv", skip=1, sep=",",
              header=FALSE, data.table=FALSE,
              showProgress=FALSE)
  setnames(DF, colnames(header))
  rm(header)