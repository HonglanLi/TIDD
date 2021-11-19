# TIDD
TIDD

TIDD is a universal post-processing tool which supports confident peptideidentifications regardless of the search engine adopted. TIDD can work for any(including newly developed) search engines because it calculates universalfeatures that assess peptide-spectrum match quality while it allows additional featuresprovided by search engines (or users) as well.

Here, we support two types of TIDD version -- a simple GUI based TIDD and command version of TIDD

1. GUI 

It is based on R and java programming. 

So it required:

- install java jre(1.8) and R(4.03 or above)
- for R, the following packages are need to install.

   > install.packages("shiny")
   > install.packages("shinythemes")
   > install.packages("shinyFiles")
   > install.packages("shinythemes")
   > install.packages("ROCR")
   > install.packages("readr")
   > install.packages("e1071")
   > install.packages("rJava")
   
- run shinyApp 
 
  > PSM results:put psm result files to data/PSM/
  > mgf files: make a new dir. under data/MGF/ 
               put mgf files to new dir.


test version of GUI link: https://honglan-li.shinyapps.io/project/


2. commmand  

- Extract TIDD features 
 
   1. java -jar TIDD.java <options> < attributes> 

   You can run "java -jar TIDD.java -h" to check the options and their corresponding values

   (If you need to calculate XCorr, run "java -jar XCorr.jar" additionally)

   2. java -jar xcorr_v2.jar spectrumFile resultFile binWidth binOffset titleCol peptideCol precursorMZCol chargeCol mgffilenameCol header
   
   *detail: check usage (run java -jar *.jar)
