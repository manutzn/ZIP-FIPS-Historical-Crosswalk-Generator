# ZIP-FIPS-Historical-Crosswalk-Generator

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

4. Use the Access Token in API Calls:
   - Include your access token in the Authorization header of your API requests using the Bearer scheme.
   - Example of how to include the token in your HTTP request headers:

     Authorization: Bearer YOUR_ACCESS_TOKEN

   - Replace YOUR_ACCESS_TOKEN with the actual token you obtained.

5. Update Your Environment Variables:
   - Do not hardcode your access token into your scripts for security reasons.
   - Store it securely as an environment variable in your development environment.
   - In R, you can add the following line to your .Renviron file:

     HUD_API_KEY=YOUR_ACCESS_TOKEN

   - Retrieve it in your script using:

     key <- Sys.getenv("HUD_API_KEY")

6. Proceed with API Calls:
   - With the access token securely stored and retrieved in your script, you can now make authenticated API calls as demonstrated in the code examples within this repository.

Note: Keep your access token confidential. Do not share it publicly or commit it to version control systems like GitHub.

By following these steps, you'll have access to the necessary data to generate the ZIP-FIPS historical crosswalk dataset using the HUD USPS ZIP Code Crosswalk Files API.
