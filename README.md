# Crowdfunding ETL Mini Project

## Overview

This mini project involves building an ETL (Extract, Transform, Load) pipeline using Python and Pandas. You will work with a partner to extract and transform data from Excel files using Python dictionary methods or regular expressions. The goal is to create CSV files, an Entity Relationship Diagram (ERD), and a table schema for a Postgres database. Follow the instructions below to complete the project.

## Before You Begin

1. Create a new repository named `Crowdfunding_ETL` for this project. Add your partner as a collaborator.

2. Clone the repository to your computer.

3. Rename the `ETL_Mini_Project_starter_code.ipynb` file with the first name initial and last name of each member of the group (e.g., `ETL_Mini_Project_NRomanoff_JSmith.ipynb`). Add this Jupyter notebook file and the `Resources` folder (containing `crowdfunding.xlsx` and `contacts.xlsx` files) to your repository.

4. Push the changes to GitHub.

5. Have your partner pull the changes to ensure both have the same notebook available.

## Instructions

### Create the Category and Subcategory DataFrames

Extract and transform the `crowdfunding.xlsx` Excel data to create a category DataFrame with columns:
- "category_id" (entries sequentially from "cat1" to "catn")
- "category" (category titles)

Export as `category.csv` to your repository.

Extract and transform the `crowdfunding.xlsx` Excel data to create a subcategory DataFrame with columns:
- "subcategory_id" (entries sequentially from "subcat1" to "subcatn")
- "subcategory" (subcategory titles)

Export as `subcategory.csv` to your repository.

### Create the Campaign DataFrame

Extract and transform the `crowdfunding.xlsx` Excel data to create a campaign DataFrame with specific columns.

Export as `campaign.csv` to your repository.

### Create the Contacts DataFrame

Choose either Option 1 (Python dictionary methods) or Option 2 (regular expressions) to extract and transform data from `contacts.xlsx`.

#### Option 1:

- Import `contacts.xlsx` into a DataFrame.
- Iterate through the DataFrame, converting each row to a dictionary.
- Split "name" into first and last names.
- Clean and export as `contacts.csv`.

#### Option 2:

- Import `contacts.xlsx` into a DataFrame.
- Extract "contact_id", "name", and "email" columns using regular expressions.
- Split "name" into first and last names.
- Clean and export as `contacts.csv`.

Check that the final DataFrame resembles the provided example.

### Create the Crowdfunding Database

Inspect the four CSV files and sketch an ERD using [QuickDBD]([link_to_quickdbd](https://app.quickdatabasediagrams.com/)).

Use the ERD information to create a table schema for each CSV file. Save the schema as `crowdfunding_db_schema.sql` in your repository.

Create a new Postgres database named `crowdfunding_db`. Create tables in the correct order to handle foreign keys.

Verify table creation by running a SELECT statement for each table.

Import each CSV file into its corresponding SQL table.

Verify correct data insertion by running a SELECT statement for each table.

## Hints

- Use `df[["new_column1","new_column2"]] = df["column"].str.split()` to split values into new columns.
- Create a NumPy array for unique category and subcategory values.
- Use list comprehension to add "cat" or "subcat" to identification numbers.
- Use `astype()` to convert columns to the float data type.
- Refer to Pandas documentation for creating DataFrames and merging DataFrames.

## Support and Resources
Data for this dataset was generated by edX Boot Camps LLC, and is intended for educational purposes only.


