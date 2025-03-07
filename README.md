# DataProject1
Group member: Carol Wu (computing ID: pmx5pm)
This ETL pipeline looks at the latest New York Times Best Seller Lists for both hardcover fiction and EBook fiction. 
Both datasets can be found on New York Times Books API (https://developer.nytimes.com/docs/books-product/1/overview). 
The dataset for NYT Best Seller List for Ebook fiction (latest to the date March 7th 2025) is stored in the repo in both JSON and CSV format.
The pipeline can take dataset directly from API calls or from local files (both JSON and CSV format are supported).
The local file has to contain the following columns: ["rank", "rank_last_week", "weeks_on_list", "title", "author", "publisher", "isbn", "description"]
The pipeline supports data conversion between CSV, JSON, and SQlite3 Database tables. Users have the option to output any datasets as either JSON files or CSV files. 
The pipeline merges lists for hardcover and ebook to perform downstream analysis. Analysis results is describe below: 

Rank Change Trends:

E-Book Fiction has a larger average rank drop (-6.53) compared to Hardcover Fiction (-2.33).
- This suggests that E-Book Fiction bestsellers fluctuate more in rankings.
The biggest rank drop in E-Book Fiction was -15, while in Hardcover Fiction, it was -13.
- This indicates that E-Books tend to be more volatile than Hardcovers.

Weeks on the Bestseller List:

E-Book Fiction books stay on the list for a much shorter period, with an average of 2.67 weeks and a maximum of 12 weeks.
- This suggests that E-Books have a shorter lifecycle on the bestseller list.
Hardcover Fiction books remain much longer, with an average of 26.73 weeks and a maximum of 86 weeks.
- This indicates that Hardcover Fiction books tend to have long-term popularity compared to E-Books.
