# extract-tables-in-a-pdf-in-R-using-tabulizer
extracting multiple tables present in a pdf in R using Tabulizer

#For extracting specific tables from a pdf we will be needing its coordinates.The steps to find coordinates is as follows- Use the Tabula app to grab table coordinates.

1.Open Tabula and upload your PDF into the web page that appears.
2.Select your table area(s) as usual and proceed to the "Preview & Export Extracted Data" step. 
3.Under Export Format, select "Script" instead of CSV, and then click "Export" to download the generated code. Save this file. 
4.Open the script you downloaded in a code editor. 
5.The generated script contains measurements already filled in, based on what you selected in the Tabula app. 
You can use this as a starting point to process many of the same type of document, 
for example if you have a monthly report that is generated as separate PDFs for each month, 
and the table you want is located in the exact same place each time.

eg of generated script "java -jar tabula-java.jar -a 234.019,38.991,313.638,555.396 -p 1 "$1" where "234.019,38.991,313.638,555.396" are the coordinates

Install the three packages in specific order:
install.packages("rJava")
library(rJava) # load and attach 'rJava' now
install.packages("devtools")
devtools::install_github("ropensci/tabulizer", args="--no-multiarch")

#Now load the package
library(tabulizer)

#You can view the report on
http://rpubs.com/masterhimanshupoddar/extract-tables-from-pdf-in-R

Author : Himanshu Poddar
