Intructions
Fine particulate matter (PM2.5) is an ambient air pollutant for which there is strong evidence that
it is harmful to human health. In the United States, the Environmental Protection Agency (EPA) is
tasked with setting national ambient air quality standards for fine PM and for tracking the
emissions of this pollutant into the atmosphere. Approximatly every 3 years, the EPA releases its
database on emissions of PM2.5. This database is known as the National Emissions Inventory
(NEI). You can read more information about the NEI at the EPA National Emissions Inventory
web site.
For each year and for each type of PM source, the NEI records how many tons of PM2.5 were
emitted from that source over the course of the entire year. The data that you will use for this
assignment are for 1999, 2002, 2005, and 2008.
## Warning: package 'ggplot2' was built under R version 3.2.5
## Warning: package 'dplyr' was built under R version 3.2.5
##
## Attaching package: 'dplyr'
## The following objects are masked from 'package:stats':
##
## filter, lag
## The following objects are masked from 'package:base':
##
## intersect, setdiff, setequal, union

Download file

The following code downloads the file, then unzips it, then reads it into R.

url1 <- "https://d396qusza40orc.cloudfront.net/exdata%2Fdata%2FNEI_data.zip"
destfile1 <- "destfile.zip"
if (! file.exists ( destfile1 )) {
download.file ( url1 ,
destfile = destfile1 ,
method = "curl" )
unzip ( destfile1 , exdir = "." )
}
NEI <- readRDS ( "summarySCC_PM25.rds" )
SCC <- readRDS ( "Source_Classification_Code.rds" )
