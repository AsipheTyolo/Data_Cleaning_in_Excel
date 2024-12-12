# Data Cleaning in Excel: BetXchange Project

## Overview

Welcome to the **BetXchange Project** repository! This project involves cleaning and preparing datasets for analysis, focusing on Users, Slips, and Transaction data for the months of **May**, **June**, and **July**. 

### Objectives
- Standardize data to ensure consistency.
- Remove duplicates and irrelevant information.
- Prepare datasets for seamless import into SQL databases.

---

## Step-by-Step Data Cleaning Process

### Users Dataset (May, June, July) 🧹

1. **Remove Duplicates**:
   - Navigate to the **Data** tab in Excel and select **"Remove Duplicates"** under the **Data Tools** group.
   - All columns were checked; no duplicates were found.

2. **Standardize Country Names**:
   - Created a new column titled `Country_Fixed`.
   - Converted all country names to uppercase using `=UPPER(D2)`.
   - Corrected invalid or misspelled country names:
     - `B` to `BANGLADESH`, `Z` to `ZIMBABWE`.
     - `CONGO {DEMOCRATIC REP}` to `CONGO`.
     - `Johannesburg` and `SA` to `SOUTH AFRICA`.
     - Adjusted foreign translations, e.g., `Africa Do Sul` (Portuguese) to `SOUTH AFRICA`.

3. **Consistency Across Months**:
   - Applied the above steps to June and July datasets.
   - Standardized variations like `Moçambique` to `MOZAMBIQUE` and `P` to `PAKISTAN`.

4. **Column Name Refinement**:
   - Renamed `Registration Date` to `Registration_Date`.

5. **Handle Blank Cells**:
   - Preserved blank cells in the `Country` column for data integrity.

6. **Finalization**:
   - Converted formula-based values to static values.
   - Removed temporary columns and formulas.

7. **SQL Import Preparation**:
   - Saved all files in CSV format for seamless import into Microsoft SQL Server Management Studio (SSMS).
   - This step can be used if you want to analyse data using SQL
   - How to import the datasets into SQL Server Management Studio (SSMS): Right click the database you created in SSMS > Go to Tasks > Click "Import flat file" > Next > Browse for location of the file to be imported > Give it a table name > Click next > Uncheck "Use Rich Data Type Detection" > Click next > Finish

---

### Slips Dataset (May, June, July) 🛠️

1. **Set Proper Headers**:
   - Assigned the first row as column headers and removed it from the data body.
   - Renamed columns for clarity and consistency.

2. **Remove Irrelevant Rows**:
   - Filtered out rows containing `Total` or other irrelevant summaries.

3. **Format Tables**:
   - Converted range tables into structured table formats.

4. **Unmerge Columns**:
   - Unmerged the `user_id` column to ensure unique entries.

5. **Handle Null Values**:
   - Replaced null or empty cells in betting categories with zeros.

6. **Standardize Formatting**:
   - Corrected issues in the `user_id` and `resolve_time` columns.

---

### Transact Folder Dataset (May, June, July) 📊

1. **Unmerge Columns**:
   - Ensured distinct entries in the `user_id` column by unmerging.

2. **Remove Duplicates**:
   - Eliminated redundant rows using **"Remove Duplicates"**.

3. **Filter Irrelevant Rows**:
   - Removed rows containing `Total` or irrelevant summaries.

4. **Handle Null Values**:
   - Replaced empty cells in betting categories with zeros.

5. **Parse Data Structure**:
   - Ensured proper parsing for seamless analysis.

6. **Standardize Formats**:
   - **Numeric Columns**: Converted to numeric types using **"Text to Columns"**.
   - **Date Columns**: Reformatted to follow consistent date formats.

7. **Enhance Data with Power Query**:
   - Leveraged Power Query for advanced cleaning and standardization.

---

## Tools Used

- **Microsoft Excel**: Data cleaning and transformation.
- **Power Query**: Advanced data standardization.
- **Microsoft SQL Server Management Studio (SSMS)**: Data storage and analysis.

---

## How to Use

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/betxchange-project.git
   ```
2. Navigate to the folder containing datasets.
3. Follow the outlined steps to replicate or analyze the data.

---

## Contact

For questions or collaboration, please reach out to **Asiphe Tyolo** at [asiphetyolo@gmail.com](mailto:asiphetyolo@gmail.com).
