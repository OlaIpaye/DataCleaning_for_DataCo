# DataCleaning_for_DataCo

A data cleaning and data preparation project assigned to me by my Tutor on DataCamp.

## Project Summary

The purpose of this project is to showcase how to prepare and clean raw data in Excel using data provided by a Consumer product business based in the USA and serving customers across America.

The initial files contain information on different customer product sales, inclduing the customer names, city, state, customer id, product cost, order details and more.

**Tools used in this project:**

- Microsoft Excel, for data cleaning and preparation.
- Company Datasets, from Datacamp platform.
- Git, for documenting my process and pushing work to Github.
- Git Bash command line interface, for cloning the remote repository on my local computer and for creating and accessing folders and images for this project.

## Datasets (Before) and (After) Cleaning

**Steps I took for cleaning the 3 initial datasets:**

- Imported each raw data into Excel, including txt and csv files.
- Imported initial files into one worksheet for easier access.
- Removed initial formatting such as table design and converted to normal cell ranges.
- Added filters, formatted headings, and text alignments to all files.

**Working with RAW DATA(B):**

The first thing I did with the DataCo raw data (including txt and csv files) I was given was to open them inidividually in Excel then I imported each sepeted files in the main "Orders" file so they can all be in one worksheet.
![worksheet in excel](<Images/DataCo Initial file.png>)

Then I removed the formating from each of them by removing the initial table designs and converted the tables to normal cell ranges. After, I renamed each file in the worksheet.
![importing worksheet into excel](<Images/Importing txt file into main worksheet.png>)

**Working with RAW DATA(A):**

Once all the initial 3 files I was given to clean are in one worksheet, I decide to: format the headings by making it bold with a yellow background color so it stands out from the rest of the cells in the worksheet. Then I added filters to each column headings, and adjusted the column widths so that all cell content is visible.
![alt text](<Images/Formatting Imported data - bold headings, yellow cell headings, added filters, column widths for headings.png>)

![formatting worksheet in excel before](<Images/Orders workbook after formatting.png>)

![formatting worksheet in excel after](<Images/Product workbook after formatting.png>)

## Removing Duplicates from Data (Before / After):

Before doing anything else, I identified the 2 files I will be using for lookup sheets and decided to further clean them up by removing any duplicated data to avoid consusion and inaccuracies later on.

Before:
![removing duplicate values in excel before](<Images/Removing duplicates from Products file.png>)

After:
![removing duplicate values in excel after](<Images/Removing duplicates from Products file-outcome.png>)

**Steps I took for removing duplicated data:**

- I selected the Product id and Customer Id columns from both worksheets, then applied conditional formatting (Highlight cell rules/Duplicate values).
- Then I selected all columns at once, and removed the duplicates (Data tab/Remove duplicates/selected My Data has headers)

Before:
![removing duplicate values in excel before](<Images/Removing duplicates from Customers file.png>)

After:
![removing duplicate values in excel after](<Images/Removing duplicates from Customers file-outcome.png>)

**Removing Unnecessary columns from the Customers dataset:**

I took a look at all the comuns in the Customers worksheet and found there were 2 columns (Customer Fname and Customer Lname). I decided to merge these 2 columns into 1 using the flash fill feature in Excel.

I typed the first 3 names manually and correctly in the new column: Full Name, making sure I pressed enter after manually typing each name of the customer. Then I used the **flash fill feature** in the Data tab to automatically input the corresponding names of the rest of the customers because it will be too time consuming to do it all myself since there are over 1000 rows of data in the worksheet.

After:
![usinf fill series in excel](<Images/Used flash fill to remove unnecessary columns in Customers file.png>)

**Populating values into new Dates worksheet without having the data:**

Created a new Dates lookup worksheet. From the Order date column in the Orders worksheet, I know orders were placed from 2015 to 2018. So I started with the first date of 2015 (01/01/2025) and used the **flash series feature** to populate for the rest of each day till the last day of 2018 (31/12/2018). These dates serve has dates orders were placed with DataCo.

Before:
![using flash fill in excel before](<Images/Using fill series feature for dates worksheet.png>)
After:
![using flash fill in excel after](<Images/Using fill series feature for dates worksheet-outcome.png>)

**Using text functions to check length and trim text values:**

In the Customers worksheet, I noticed the Customer State column had values greater than 2 because the initial dataset had spaces within the values in the column.

So I created a new column called Length Check, then used the LEN() fucntion to get the lenght of each values in the Customer State column to determine which values were greater than 2 because of the spaces in them.

Then after, I created another coloumn between the 2 columns as stated above, and used the TRIM() function to remove any unwanted spaces and trim down the values to 2. Then I removed the applied fucntion in the new Cust State column by copying the column and (paste as values). After that, I deleted the initial Customer State column since I no longer need it and then lastly I adjusted the function applied to the Length Check colomn to match the new Customer State comun with the corrected values of 0-2 in each columns.

Before:
![text fucntions in excel](<Images/Checking text length for values greater than 2.png>)

After:
![using len function in excel](<Images/Checking text length for values greater than 2-OUTCOME1.png>)

![text fucntions in excel](<Images/Checking text length for values greater than 2-OUTCOME.png>)

**Replacing unclear values in the DataCo dataset:**

In the Customer Country column in the Customers worksheet, the values: EE.UU. is unclear and doesn't say what country the customers are from so I replaced it with USA, because the cities belong in the United States. This is clearer and easier for all to understand.

After:
![Replaced column values in excel](<Images/Replaced values in the Customer Country column.png>)

**Joining values and Removing unneeded columns in the DataCo dataset:**

In the DataCo dataset, I saw that the Customers address were seperated into 3 columns. I didn't think it made sense since the Customer City, Customer Street and Zip code columns were not important for analysis later on. So I decided to join the values into one column called Customer Address using the cancat fucntion.

After:
![using cancat function in excel](<Images/using cancat function to join values from multiple columns.png>)

**Protecting cleaned Customers worksheet:**

After cleaning the Customers worksheet and I was satisfied with the outcome I decided to password protect it to avoid losing any data.

After:
![protecting worksheet in excel](<Images/Customers worksheet cleaned, protected and ready for analysis.png>)

**Specifying customer delivery day of the week using date functions:**

Since DataCo delivers all accross the US and Puerto Rico, and working with different time zones. I wanted to spicity the value for the day of the week for each date in the Dates worksheet using the Weekday() fucntion, with 1 = Sunday and 7 = Saturday.

Also, I added the date the worksheet was last edited, using the Today() fucntion.

After:
![alt text](<Images/DataCo delivery weekday specified in Dates worksheet.png>)

**Specifying customer order delivery date using date functions:**

Since the Order date and Date for shipment date values were provided for me. I decided to add an extra column to provide information for the DataCo team so they can keep track of the date orders will get to their customers.

I used the Workday() function in combination with the two affordmentioned columns to get the values for the new Scheduled Delivery date column.

Before:
![using date functions in excel](<Images/Scheduled delivery date for Orders.png>)

After:
![using date functions in excel](<Images/Scheduled delivery date for Orders-outcome.png>)

**Finding average product price and using logical functions:**

In the Products worksheet, I calculated the average product price from all products sold and then used the NOT() logical function to figure out which product is not greater than or equal to the average price to determine which products are more expensive.

Then I created an absolute reference in the formula so it doesn't change and locks in for formula for all columns.

After:
![using logical functions in excel](<Images/using logical functions in excel.png>)

**Determining which orders were same day delivery using logical functions:**

In the Orders worksheet, I wanted to determine which orders are same-day deliveries without a risk of being late.

I decided to use the if and function together to identify which orders will be delayed based on the Late_delivery_risk column being 0 = no delay, and 1 = delayed in combination with the values in the Shipping mode column. Since there is already "Same Day" in the column, it made my job easier.

After:
![using if fucntion in excel](<Images/Checking for orders with same day delivery in Orders worksheet.png>)

![using if and function in excel](<Images/Checking for orders with same day delivery in Orders worksheet-outcome.png>)

**Identifying Orders paid for by cash and over 200 using logical functions:**

Out of all the columns in the Orders worksheet, there was not a column for the Total sales per order. So I created the Total Order Sales column.

Then I wanted to find out which orders were paid for in cash, debit and bank transfer. I did this using the if and logical functions.

Before:
![nested if function in excel](<Images/using nested if to check if cash payment is over 200.png>)

After:
![using logical functions in excel](<Images/using nested if to check if cash payment is over 200-outcome.png>)

**Adding comments and notes in the worksheets:**

After cleaning all the worksheets in the workbook, I decided to add some notes and comments regarding the steps I took to aggregate some of the columns in the datasets.

Adding a comment to the Products worksheet:
![adding a comment in excel](<Images/Adding comments to Products worksheet.png>)

Adding a note to the Orders worksheet:
![adding a note in excel](<Images/Adding notes to Orders worksheet.png>)

**Adding comments and notes in the worksheets:**

When I was done cleaning the data, I decided to carry out some more analysis into the products sold by DataCo. I used the vlookup function to bring in some product information into the Orders worksheet, from the Products worksheet.

Since the Product Category Id and Product Id columns were already in the Orders worksheet, for better analysis and visualisation, I needed them to correspond what products and category they were referencing in the Orders worksheet.

After:
![Using vlookup function for consumer product business](<Images/Using vlookup function1.png>)

![Using vlookup function for consumer product business](<Images/Using vlookup function2.png>)

![Using vlookup function for consumer product business](<Images/Using vlookup function2-Paste as values to remove functions.png>)

![Using vlookup function for consumer product business](<Images/Using vlookup function3-deleted 2 columns.png>)

nmn
