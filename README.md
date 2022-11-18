# pssp-enhancements
HHA 504 / Cloud Computing / Assignment 9 / PssP Enhancements


## This repo aims to:
- Enhance the **Patient Service Portal** I previously created in [PSSP](https://github.com/alicewu1/PssP) with the goals below

<br>

# GOALS
# 1. Stylizing the landing page to look more like a realistic fake patient portal

# 2. Create a new account type called: care provider
- The care provider should have permissions to edit existing patients
- There should be a new endpoint for creating this account type; and a new dropdown field value within SQL for account_type

# 3. Create *EDIT* functionality for profile 
- Be able to update email and username

# 4. Create a video demo showcasing the PSSP
- Demonstrate accomplishments
- Discuss any errors encountered 

# Creating a new schema for user accounts
- Copy & Paste **userTable.sql** into a new Query tab in MySQL Workbench 
- Verify **Admin** user was created in your browser **Log in** page 

<br>

# Images Folder
- contains screenshots of my live patient portal, styling, and functionalities

# ERRORS:
- **[ERROR 1]** Under @app.route('/login'), I received a "Build Error for get_patient_details, did you forget to specfiy values mrn?" 
    - (screenshot included in images folder)
    - When attempting to add account type "careprovider" to log in using the coding below:
             https://github.com/alicewu1/pssp-enhancements/blob/cccceff6f64405322b89b84e44b701835b75dbba/app.py#L231-L257 

- **[RESOLVED]** by: adding **elif** to include care providers in the get_gui_patients 
             https://github.com/alicewu1/pssp-enhancements/blob/cccceff6f64405322b89b84e44b701835b75dbba/app.py#L447-L457

- **[ERROR 2]** When I **Add New Patient** on the patients list page, the **Date of Birth** and **Zip Code** values are swapped
