# CallCentre_DataCleaning

### Project Background

A call center has provided a dataset containing details of all the customers they have contacted. The dataset, however, is quite messy and unorganized. The call center has requested our assistance in cleaning up this dataset and generating a new, organized list of customers to contact. Our goal is to process the provided data, remove any inconsistencies, duplicates, and errors, and deliver a refined list that the call center can use for their future outreach efforts.

### Objectives

1. **Data Cleaning**: Identify and rectify inconsistencies and errors in the provided dataset.
2. **Duplicate Removal**: Detect and remove duplicate entries to ensure each customer is listed only once.
3. **Data Standardization**: Ensure that all customer information is formatted consistently, including contact details, names, and addresses.
4. **List Generation**: Produce a new, organized list of customers ready for contact, meeting the call center's requirements.

### Methodology

1. **Initial Data Assessment**:
   - **Load the Data**: Import the dataset into a DataFrame using Pandas.
   - **Explore the Data**: Examine the dataset's structure, column names, and types to understand its contents.
   - **Identify Issues**: Detect common issues such as missing values, inconsistent formats, and potential duplicates.

2. **Data Cleaning Process**:
   - **Error Identification and Correction**:
     - **Missing Values**: Use methods like `dropna()` to remove rows with missing values or `fillna()` to impute missing data.
     - **Error Correction**: Identify and correct typographical errors or inconsistencies using functions like `replace()` or string operations.
   - **Consistency Checks**:
     - **Standardize Formats**: Use Pandas functions to normalize formats for phone numbers, email addresses, and addresses. For example, use regex patterns with `str.replace()` to ensure uniform phone number formatting.
     - **Normalize Data**: Convert all text to lowercase or uppercase where appropriate using `str.lower()` or `str.upper()`.

3. **Duplicate Detection and Removal**:
   - **Identify Duplicates**: Use `duplicated()` to find duplicate rows based on specific columns, such as customer IDs or email addresses.
   - **Remove Duplicates**: Use `drop_duplicates()` to eliminate duplicate entries, ensuring that each customer appears only once.

4. **Data Standardization**:
   - **Consistent Formatting**: Apply uniform formatting rules across the dataset, including date formats and address structures. Use functions like `pd.to_datetime()` for date conversion and string operations for address standardization.
   - **Validation**: Validate data against predefined rules or patterns to ensure accuracy.

5. **New List Creation**:
   - **Prepare Final Data**: Compile the cleaned and standardized data into a new DataFrame.
   - **Export Data**: Save the final list in a suitable format (e.g., CSV) using `to_csv()` for the call center's use.

### Pandas Tools and Techniques Used

1. **Data Loading**: 
   - `pd.read_csv()`: For importing the dataset into a DataFrame.
   
2. **Data Exploration**: 
   - `df.head()`: To preview the first few rows of the dataset.
   - `df.info()`: To get a summary of the DataFrame including column names and data types.
   - `df.describe()`: For statistical summaries of numerical data.

3. **Data Cleaning**:
   - `df.dropna()`: To remove rows with missing values.
   - `df.fillna()`: To fill in missing values with specified replacements.
   - `df.replace()`: For correcting specific errors or inconsistencies.

4. **Data Standardization**:
   - `df.str.lower()`: To convert text to lowercase.
   - `df.str.upper()`: To convert text to uppercase.
   - `df.apply()`: For applying functions to columns or rows.

5. **Duplicate Handling**:
   - `df.drop_duplicates()`: To remove duplicate entries.


### Project Result

The project resulted in a significantly improved dataset for the call center. The cleaned dataset now features:

- **Enhanced Accuracy**: Errors have been corrected, and inconsistencies have been resolved, providing reliable customer information.
- **Eliminated Duplicates**: Duplicate entries have been removed, ensuring that each customer appears only once.
- **Standardized Data**: All customer details are now formatted consistently, making the data easier to use and integrate with other systems.
- **Organized Contact List**: A new, refined list of customers ready for outreach has been delivered, meeting the call center's needs for effective communication.
