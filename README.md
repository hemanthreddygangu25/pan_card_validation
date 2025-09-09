# pan_card_validation
pan card validation using sql


⚙️ Steps Implemented
1. Data Preparation

Load raw data into a staging table (stg_pan_numbers_dataset).

Identify and handle:
Missing values
Duplicates
Leading/trailing spaces
Case sensitivity

2. Data Cleaning
Created a cleaned table (pan_numbers_dataset_cleaned) with properly formatted PAN numbers.

3. Validation Rules
Two PL/pgSQL functions were created:
fn_check_adjacent_repetition() → Checks if adjacent characters are repeated.
fn_check_sequence() → Checks for sequential patterns (e.g., ABCDE, 1234).

4. Valid vs Invalid PAN Classification
A SQL View (vw_valid_invalid_pans) categorizes each PAN as Valid PAN or Invalid PAN.

5. Reporting
A summary report provides:
Total processed records
Count of valid PANs
Count of invalid PANs
Missing/incomplete PANs


| Total Records | Valid PANs | Invalid PANs | Missing/Incomplete |
| ------------- | ---------- | ------------ | ------------------ |
| 1000          | 850        | 120          | 30                 |
