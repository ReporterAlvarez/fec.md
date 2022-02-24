# fec.md
Felicia Alvarez's Markdown Assignment
## :shower: Open Refine Data Cleaning :shower:
### 1. Trim leading and trailing white space on all columns
### 2. Create text facet for all columns and search for spelling errors and inconsistencies
### 3. Changes for "Recipient" column
* "1995 Repub Senate/House Dinner Cmte" changed to "1995 Republican Senate/House Dinner Committee"
* "1996 Republican Senate/House Dinner" changed to "1996 Republican Senate/House Committee"
* All instances of "Cmte" changed to "Committee"
### 4. Changes for "City" column
* "ATHERTONO" changed to "ATHERTON"
* "BETHELEHEM" changed to "BETHLEHEM"
* "DALLAS/FORT WORTH" changed to "FORT WORTH"
  * Donation was made by American Airlines, which is headquartered in Fort Worth, Texas
* "NEW YORKROOK" changed to "NEW YORK"
  * Donation was made by Trace International Holdings, which is headquartered in New York City
* "RES TRIANGLE PARK" changed to "DURHAM"
  *  Donation was made by Glaxo Wellcome Inc in North Carolina. Glaxo Wellcome Inc's buildings in Research Triangle Park have a Durham address
*  "RESEARCH TRIANGLE" changed to "DURHAM"
  *  Donation was made by Glaxo Wellcome Inc in North Carolina. Glaxo Wellcome Inc's buildings in Research Triangle Park have a Durham address
### 5. Changes for "Zip" column
* "1748" changed to "01748" according to the donor's address in Hopkinton MA
* "1930" changed to "01930" to match donor's address in Gloucester, MA
* "2109" changed to "02109" to match donor's address in Boston, MA
* "2110" changed to "02110" to match donors' addresses in Boston, MA
* "2194" changed to "02194" to match donors' addresses in Boston, MA
* "6339" changed to "0339" to match donor's address in Mashantucket, CT
* "6820" added a zero at the beginning to match donor address in CT
* "6830" added a zero at the beginning to match donor address in CT
* "6836" added a zero at the beginning to match donor address in CT
* "6856" added a zero at the beginning to match donor address in CT
* "6881" added a zero at the beginning to match donor address in CT
* "6905" added a zero at the beginning to match donor address in CT
* "6912" added a zero at the beginning to match donor address in CT
* "7073" added a zero at the beginning to match donor address in NJ
* "7087" added a zero at the beginning to match donor address in NJ
* "7090" added a zero at the beginning to match donor address in NJ
* "7753" added a zero at the beginning to match donor address in NJ
* "7940" added a zero at the beginning to match donor address in NJ
* "7945" added a zero at the beginning to match donor address in NJ
* "7977" added a zero at the beginning to match donor address in NJ
* "8608" added a zero at the beginning to match donor address in NJ
* "960" changed to "00960" to match address in Puerto Rico
* blank ZIP code for "Johnson, Robert Wood" changed to "unknown"
* blank ZIP code for "American Airlines" changed to 76155 to match company headquarters in Fort Worth
### 6. Export Open Refine file as a .xlsx
### 7. Import file into Google Sheets
### 8. Freeze top row, bold top row, add filters to top row
### 9. Sort "Donor" Column A-Z, and search for duplicates with the same Donor, Amount, Date, Recipient
* Duplicates: _(note that row numbers are marked as the one before it is being deleted)_
  *  Row 66 "Cafaro, John J
  *  Row 68 "California Republican Party"
  *  Row 140 "Friess, Foster"
  *  Row 205 "Lauder, Ronald S"
  *  Row 245 "Murdoch, Anna M"
  *  Row 252 "New York Republican State Committee"
  *  Row 284 "Philip Morris"
  *  Row 298 "Republican Assembly Campaign Committee"
  *  Row 327 "Scripps, Edward Wyllis"
  *  Row 328 "Senate Republican Campaign Committee"
  *  Row 329 "Senate Republican Campaign Committee"
  *  Row 330 "Senate Republican Campaign Committee"
## :mag: Answering the Six Questions :mag:
### Question 1
#### _Which industries contributed the most to the Republican and Democratic parties? How much was contributed to each party?_ 
1. Format "Amount" column as a number/currency
2. Insert Pivot Table of all cells
  * Add "Industry" as a Row and the SUM of "Amount" as a Value
  * Under Rows, sort by SUM of Amount to see which industries contributed the most
  * Add "Party" as a column to see totals for each party
  * SCREENSHOT OF PIVOT TABLE 12:52
3. Copy/Paste Pivot Table into a new tab
4. Add Filters to top row
5. Filter Z-A to see top Republican, Democrat, and Grand Total contributions
#### The Republican party received the most contributions from those in the Republican/Conservative industry. <br> The Democratic party received the most contributions from the Media/Entertainment industry. <br> Republicans received a total of $27,924,000 and Democrats received a total of $21,553,578.**
### Question 2
#### _How much did donors from the Misc. Business sector contribute to the Democratic party? Which donors were based in Miami Lakes, FL?_
1. Under "Sector" column, clear all and select "Misc. Business"
2. Under "Party" check only the "D" box
3. Copy/Paste these into a new sheet
4. Below last cell in column B "Amount", find the sum by using =SUM(B2:B43) or $3,520,000
5. Under "City" clear all and only select "Miami Lakes". Only Windmere Corp with two donations
#### **Donors from the Misc. Business sector contributed $3.52 million to the Democratic Party. The only donor based in Miami Lakes, FL was Windmere Corp, which made two contributions**
### Question 3
#### _What percentage of the tobacco industry’s donations does Philip Morris account for? How much is it?_
1. Reselect everything in the sheet, make sure new filters are active (or else!)
2. Create a Pivot Table
3. Use "Industry" as a row
4. Use "Donor" as a column
5. Use "Amount" as a value
6. Filter with "Industry", clear everything except for "Tobacco"
7. Under Values, Summarize by SUM and show it as "% of grand total" to see that Philip Morris contributed 65.70% of all donations. Toggle to "Default" to see the sum of his contributions, $1.82 million.
8. INSERT SCREENSHOT 12:55
#### **Philip Morris accounts for 65.7% of all of the tobacco industry's contributions, or $1.82 million in contributions.**
### Question 4
#### _Describe one potential story from this dataset that you’d find promising if this were a project you were working on. Give it a headline. Include up to three types of sources you would call to report out the story and a few of the questions you might ask. (These can be bullet points — no need for a long explanation.) Remember to detail the steps you took in analyzing the data to get to the story idea. Use the skills we’ve learned to help you._
#### **Big Tobacco funds more campaign contributions than the Republican Party who receives them**
Tobacco industry giant Philip Morris gave more campaign contributions than any single entity during this campaign cycle. What causes and candidates did Philip Morris fund, and why? Who's campaigns are benefiting the most from tobacco dollars? Sources I would reach out to would be the chair of the Republican National Committee, grassroots advocates who are trying to fight big tobacco, and a policy expert on what influence big tobacco holds on the campaign trail.
### Question 5
#### _What data might be suitable to join with this data to provide context or additional stories?_
1. It would be interesting to see this data set over time, especially if Philip Morris' contributions have increased or decreased over time
2. I would overlay this with also with a timeline of lobbying efforts from the American Lung Association or other doctor-led efforts against smoking
3. It would also be interesting to see this overlayed with lung disease rates connected to tobacco
### Question 6
