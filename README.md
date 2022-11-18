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


# Creating a new schema
- Copy & Paste **userTable.sql** into a new Query tab in MySQL Workbench 
- Verify **Admin** user was created in your browser **Log in** page 


# ERRORS:
- Under Login, @app.route('/login', methods=['GET', 'POST'])
- I attempted to get the account type "careprovider" to log in using the coding below:

            elif session['account_type'] == 'careprovider':
                return redirect(url_for('get_gui_patients'))   
- I received a Build Error for get_patient_details, did you forget to specify values mrn?

- Resolved by: adding elif to include care providers in the get_gui_patients 
- @app.route('/patients', methods=['GET'])
def get_gui_patients():