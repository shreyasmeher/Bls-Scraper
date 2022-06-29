## BLS Table Scraper 
### Shreyas Meher

The script is a .ipynb file named as Final.ipynb. Load the jupyter notebook with Jupyter Lab or Jupyter notebook. 

The first few cells in the script ask the user to input the working url of the BLS content/table that they want to scrape using the script. Here, they are expected to input a url from https://www.bls.gov/bls/newsrels.htm#OPLC, after which the url is stored by the script.

The url is then scraped using BeautifulSoup, looking for the relevant tags of the various tables in the page. This script is unique in the sense that it allows for selective scraping of multiple tables in the webpage, which is not a base function of the packages used (Pandas or BeautifulSoup). Tables are first unwrapped from within the various <tbody> tags and then merged using a loop function. 

The user is then asked which of the tables in the page (in the case that there are multiple of them - eg. https://www.bls.gov/regions/southwest/news-release/2022/occupationalemploymentandwages_houston_20220624.htm) they want to scrape. 

To clean the data up even more, the footnote markers are then removed from the dataframe using another function. As the data scraped is going to be quantitative in nature, $ signs and markers are removed from the dataframe created as well. This is to ensure that the data is readable by statistical software and requires very little cleaning after it is run through the script. You might have to change a few tags in the script for this to work, and so I have #'d out the commands to do the same. 

Finally, the user is then prompted once again to define a .csv filename for the data to be stored to in their local computing environment. The .csv file is then stored onto the working directory. 
