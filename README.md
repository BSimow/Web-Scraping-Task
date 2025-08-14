# Web Scraping Task

This python notebook works as a basic template to webscraping for a specific website. The website used in it is a mock website with mock data. 

## Approach
I started by importing the necessary files that can be found in the requirements.txt file. I called a get request on the website to get the HTML data. I used Beautiful soup to parse the HTML to be used as a python object.

The text data was fetched by looking for all items with p tags, li tags and h1 tags (and its variants). Then getting its text data through iterating through the list of "Texts". To export it I used Pandas. I changed the listss I created in lists. Made a new list for the header and set it as the new header. Removed the indexing after concatenating the multiple serieses together (p, li, h). Exporting it to CSV was the last step.

The table data was the easiest as it required me to fetch the table, then the rows, then the items in the rows. Created a list of lists each item was an item in the original table. Created a dataframe easily due to the structure of List of Lists making it easier for pandas to parse the data. Finally exported it to CSV.

The products, featured products and links all had the same approach. First iterating through the div of products, then defining a dictionary to store each item on its own. Finally, exporting it to as CSV.

## Challenges

Exporting the text data was undoubtly the hardest part. As I first created the list of texts in a horizontal way which pained me to a transpose it and make it fit in a dataframe, and then concatenating the rest of the lists (header and lists) was also as hard due to the horizontal structure of the lists.
