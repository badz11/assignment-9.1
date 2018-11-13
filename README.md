# assignment-9.1

Acagild session 10.1 assignment

Import dataset from the following link: AirQuality Data Set

Perform the following written operations:

Read the file in Zip format and get it into R.

Create Univariate for all the columns.

Check for missing values in all columns.

Impute the missing values using appropriate methods.

Create bi-variate analysis for all relationships.

Test relevant hypothesis for valid relations.

Create cross tabulations with derived variables.

Check for trends and patterns in time series.

Find out the most polluted time of the day and the name of the chemical compound.

Ans 1 ->

unzip("x.zip")

for (i in files.temp)

unzip(i)

airqual <- read.table("C:/Desktop/airquality.txt")

airquality <- read.csv("~/CUNY/Bridge Classes/R Programming/Week4/airquality.csv", row.names=1) head(airquality)

ggplot(airquality, aes(x = Ozone)) + geom_histogram(binwidth = 5, fill="green", color="black")

3.We can use two colsums or apply. Please see below

colSums(is.na(airquality))

        or 
        
apply(is.na(airquality),2,sum)

md.pattern(airquality)

t.test(airquality)

We need to use Z value to find check whether H0 is accepted or rejected

table(airquality)

ts(inputData,frequency = 1, start = c(2018, 2)

