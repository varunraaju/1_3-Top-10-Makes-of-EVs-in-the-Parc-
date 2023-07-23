# 1_3-Top-10-Makes-of-EVs-in-the-Parc-
Pie Chart of Top 10 Makes of EVs in the Parc 
Procedure for Collecting Electric Vehicle Statistics Data in the United Kingdom:
      1.	Access the official website of the UK Government's statistics, https://www.gov.uk/government/collections/vehicles-statistics.
      2.	Navigate to the section dedicated to vehicle statistics and proceed to open the page dedicated to vehicle statistics.
      3.	Locate and access the most recent report on vehicle licensing statistics.
      4.	Within the designated page for Vehicle Licensing Statistics for the specified year, proceed to the documents section and initiate the download of the latest tables in zip file format.
      5.	From the downloaded files, identify and extract the relevant data from the "VEH0171.ods" file, focusing solely on the required information related to electric vehicles.

Procedure for Cleaning the "VEH0171.ods" File:
      1.	Open the "VEH0171.ods" file and navigate to the sheet named "VEH0171b_GenModels."
      2.	Copy all columns containing Electric Vehicle (EV) data, along with their respective column headers, to a new workbook.
      3.	Remove the columns labelled "Geography" and "Units" since their values are identical throughout.
      4.	Rename the column headers as follows:
            a.	Change "BodyType [note 2]" to "BODYTYPE"
            b.	Change "Make [note 6]" to "MAKE"
            c.	Change "Generic model [note 6]" to "MODEL"
      5.	Eliminate all rows that contain the model data "MISSING" by using the RIGHT and IF functions along with the Filter.
      6.	Convert the quarterly data into yearly data by calculating the sum of each quarter and label the header as "YEAR" in YYYY format.
      7.	Calculate the overall row total for each model and name the corresponding header as "TOTAL."
      8.	Delete all the quarterly data, as it is no longer necessary.
      9.	Verify and convert all text data into uppercase for consistency.
      10.	Save the cleaned file as "SOURCE_DATA" in Excel workbook format.

1_3 Procedure to arrive at the data to create Pie chart of “Top 10 Makes of EVs in the Parc”.
      1.	Open the SOURCE_CODE excel file and insert a pivot table.
      2.	Add “MAKE” in rows and “TOTAL” in values.
      3.	Calculate the sum of TOTAL and sort the value in descending order.
      4.	Now copy top 10 rows into a new workbook. 
      5.	Rename the headers as “MAKE” and “TOTAL”.
      6.	Save the file as CSV format with name as “1_3.CSV”.
