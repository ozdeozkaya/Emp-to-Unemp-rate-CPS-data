# CPS


## Overwiev

The goal is to help to extract raw CPS files and link different records from different months. 
For extraction, the code here is mainly based on Brian Dew's code: https://www.bd-econ.com/cps.html

You can download public raw CPS files from this link: https://www.census.gov/data/datasets/time-series/demo/cps/cps-basic.2018.html. Each file is in .dat format. 

Alternatively, you can download the CPS data from https://cps.ipums.org/cps/ for different programs -- which should be easier than reading raw data as we do here. 

For linking individuals, I give an example code where I link people across different folders to estimate the rate from employment to unemployment. 

## Notes on CPS

Households in the data are in the survey for 4 consecutive months (an example; June 2010, July 2010, August 2010 and September 2010), out for 8 (October 2010, November 2010, December 2010, January 2011, February 2011, March 2011, April 2011 and May 2011), and then they return for another 4 months (June 2011, July 2011, August 2011 and September 2011) before leaving the sample permanently. Therefore, if the survey month in the sample (variable HRMIS) is 4 or 8 then this person will not be in the sample of next month. For example, if we use Dec 2011 basic CPS file , then households with HRMIS=4 or HRMIS=8 will not be in the Jan 2012 basic CPS file.

