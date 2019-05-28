# Concordance
Concordance provides an algorithm for harmonizing Industrial Classification Codes over time.
It is based on the intention and work of Pierce and Schott (2012a,b), 
but implemented as a Java Class relying on a graph algorithm developed 
by Sedgewick and Wayne (2011).

Concordance.java expects a csv-file with lines each containing an 
old product code, the replacing new code and the year of replacement. 
It groups all old and new codes together which are related in at 
least one observation and assigns them a common group code.

Output is a csv-file with four variables:    

productcode (contains all single old and new codes),

groupcode (respective common group codes),

year (the latest year the productcode appears in the concordance file),
    
endyear	
(0, if productcode is still active, or date, if productcode has been replaced)
          
ConcordanceStataWrapper 
wraps the Concordance.java class in order to be called by a Stata Program.

For additional information see https://www.stata.com/java/
