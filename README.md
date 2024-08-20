# DataCleaning_for_DataCo

A data cleaning and data preparation project assigned to me by my Tutor on DataCamp.

## Project Info

The purpose of this project is to showcase how to prepare and clean raw data in Excel worksheets using data provided by a Car Dealership business based in India.

The initial files contain information on different cars sold by the dealership, inclduing the make of the car, model, fuel type, price sold, order details and customer information.

## Datasets (Before) and (After) Cleaning

**Steps I took for cleaning the 3 initial datasets:**

- Imported each raw data into Excel, including txt and csv files.
- Imported initial files into one worksheet for easier access.
- Removed initial formatting such as table design and converted to normal cell ranges.
- Added filters, formatted headings, and text alignments to all files.

**Working with RAW DATA(B):**

The first thing I did with the DataCo raw data (including txt and csv files) I was given was to open them inidividually in Excel then I imported each sepeted files in the main "Orders" file so they can all be in one worksheet.
![alt text](<Images/DataCo Initial file.png>)

Then I removed the formating from each of them by removing the initial table designs and converted the tables to normal cell ranges. After, I renamed each file in the worksheet.
![alt text](<Images/Importing txt file into main worksheet.png>)

**Working with RAW DATA(A):**

Once all the initial 3 files I was given to clean are in one worksheet, I decide to: format the headings by making it bold with a yellow background color so it stands out from the rest of the cells in the worksheet. Then I added filters to each column headings, and adjusted the column widths so that all cell content is visible.
![alt text](<Images/Formatting Imported data - bold headings, yellow cell headings, added filters, column widths for headings.png>)

![alt text](<Images/Orders workbook after formatting.png>)

![alt text](<Images/Product workbook after formatting.png>)

## Removing Duplicates from Data (Before / After):

Before doing anything else, I identified the 2 files I will be using for lookup sheets and decided to further clean them up by removing any duplicated data to avoid consusion and inaccuracies later on.

Before:
![alt text](<Images/Removing duplicates from Products file.png>)

After:
![alt text](<Images/Removing duplicates from Products file-outcome.png>)

**Steps I took for removing duplicated data:**

- I selected the Product id and Customer Id columns from both worksheets, then applied conditional formatting (Highlight cell rules/Duplicate values).
- Then I selected all columns at once, and removed the duplicates (Data tab/Remove duplicates/selected My Data has headers)

Before:
![alt text](<Images/Removing duplicates from Customers file.png>)

After:
![alt text](<Images/Removing duplicates from Customers file-outcome.png>)

**Removing Unnecessary columns from the Customers dataset:**

I took a look at all the comuns in the Customers worksheet and found there were 2 columns (Customer Fname and Customer Lname). I decided to merge these 2 columns into 1 using the flash fill feature in Excel.

I typed the first 3 names manually and correctly in the new column: Full Name, making sure I pressed enter after manually typing each name of the customer. Then I used the flash fill feature in the Data tab to automatically input the corresponding names of the rest of the customers because it will be too time consuming to do it all myself since there are over 1000 rows of data in the worksheet.

After:
![alt text](<Images/Used flash fill to remove unnecessary columns in Customers file.png>)

vbnvbvbv
