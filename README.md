# ZIP-FIPS-Historical-Crosswalk-Generator (2010-2023)

This repository provides code for constructing a historical, quarterly dataset that systematically maps USPS ZIP codes to their corresponding FIPS codes. By utilizing data from the HUD USPS ZIP Code Crosswalk Files API, the code establishes a consistent and structured relationship between these geographical identifiers across different time periods. This tool is essential for precise spatial linkage in empirical research and policy analysis, enabling scholars and analysts to integrate and align datasets that employ varying geographical coding schemes over time. By ensuring accurate and reliable correspondence between ZIP codes and FIPS codes historically, it enhances the robustness and validity of analyses that depend on consistent geographical identifiers.


# Getting Started
## Getting an Access Token

To use the HUD USPS ZIP Code Crosswalk Files API with this repository, you'll need to obtain an access token. Follow these steps to create an account and get your access token:

1. Sign Up for an Account:
   - Visit the HUD User API Registration Page: https://www.huduser.gov/portal/dataset/uspszip-api.html
   - Click on "Register Now" to create a new account.
   - During registration, select the Datasets API you want to access.

2. Confirm Your Account:
   - Check your email inbox for a confirmation message from HUD User.
   - Click the confirmation link provided in the email to activate your account.

3. Log In and Generate an Access Token:
   - Log in to your account on the HUD User Portal: https://www.huduser.gov/portal/home.html
   - Navigate to the API section or your Account Dashboard.
   - Click on "Create New Token" to generate a new access token.

4. Proceed with API Calls:
   - With the access token securely stored and retrieved in your script, you can now make authenticated API calls as demonstrated in the code examples within this repository.

Note: Keep your access token confidential. Do not share it publicly or commit it to version control systems like GitHub.

By following these steps, you'll have access to the necessary data to generate the ZIP-FIPS historical crosswalk dataset using the HUD USPS ZIP Code Crosswalk Files API.

## Understanding the generated files

After running the ZIP-FIPS-Historical-Crosswalk-Generator.R script, two files will be generated:

quarterly_crosswalk_zip_county.csv
quarterly_crosswalk_zip_county.rds

## Variable Descriptions:

zipcode: A 5-digit USPS ZIP code.

fips_code: A 5-digit unique Census county GEOID, combining the state FIPS code and county FIPS code.

res_ratio: Represents the proportion of residential addresses within the ZIP–County area relative to the total residential addresses in the entire ZIP code.

bus_ratio: Represents the proportion of business addresses within the ZIP–County area relative to the total business addresses in the entire ZIP code.

oth_ratio: Represents the proportion of other (non-residential and non-business) addresses within the ZIP–County area relative to the total other addresses in the entire ZIP code.

tot_ratio: Represents the proportion of all types of addresses within the ZIP–County area relative to the total number of all addresses in the entire ZIP code.


