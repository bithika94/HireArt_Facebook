# HireArt_Facebook
Problem Statement:
The marketing ops team sent over this spreadsheet containing four years of data from a CRM system (please make a copy of the spreadsheet in order to manipulate the data): https://docs.google.com/spreadsheets/d/16hLtx8bBDe2GS1MOa3v9hY6Yhm4C30koLoCpiIJ5WDg/edit?usp=sharing.

The team wants to find the month they're likely to contact the most clients, so they can schedule a product upgrade announcement. Which month does the team tend to contact the greatest percentage of its clients?

(In addition to providing an answer, please either include a public link to a spreadsheet showing your work, or describe your process for answering the question.)

Solution Approach:

1. Opened the spreadsheet url and saw data. As data is very small only 21KB, downloaded and saved copy of it on my local machine.

2. Read the excel file with read_excel into dataframe and displayed first 5rows of it.

3. Data Cleaning Checked data types, null values if any before proceeding further, as most of the times efforts required in cleaning and pre processing. But seems that this data is very clean. No null values :-) As reading excel file into dataframe has datetime data type its better to avoid further conversions and prefer to read it as csv instead :-)

4. Data Exploration

Data of contact has 704 unique values
Client Name has 35 unique values
There are 4 Account Managers
Maximum appearing top Account Manager is "Milan Crona"
Maximum appearing top Client Name is "Eichmann and Sons"
Maximum appearing top Date of Contact is "2013-10-11"
So it seems october month might have maximum number of client contacted, but lets explore it more and see
Splitted tha "Date of Contact" column into three columns "Year", "Month" and "Day"

5. After splitting Date of Contact column, we can see that this has 5 Years of data and maximum appearing top year is 2014.

6. Then found out count of clients contacted per Month.

7. Then got to know that month October [10] has maximum number of clients contacted which is 213.

8. Again took count per year per month and found that maximum number of clients are contacted in 2013, 10 which is 60.

9. While calculating total number of clients contacted, it is a possibily that one client has contacted multiple times.

10. So in order to avoid the repetative count , I calculated unique number of clients contacted per month which came to be 35 clients for the Month of October which is highest. It can be concluded that October is the best month to contact the greatest percentage of its clients.

