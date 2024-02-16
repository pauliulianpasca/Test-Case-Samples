# Test Case Samples

Below are some Test Case samples that I wrote while working on previous projects.

----------------

**Description:** 
Check if the login works when a person uses a correct user/pass.

**Steps to Reproduce:**
1. Go to www.website.com/login
2. Add a correct user / pass
3. Press Login button

**Expected result:**
User should be able to login and is taken to his profile page.

**Test Data:**
User: paulp & Pass: paulp


------------------------

**Description:** 
Check if forgot password functionality works as expedted and an email with reset password link is sent.

**Steps to Reproduce:**
1. Go to www.website.com/login
2. Press "Forgot Password" button
3. Add an email address
4. Press "Recover" button

**Expected result:**
User should receive an email with a reset password link. That link should allow the user to create a new password.

**Test Data:**
User: paul@email.com

**Note**
Please check the login again after running this test case.


------------------------

**Description:** 
Check if the login works when a person uses a corect user/pass.

**Steps to Reproduce:**
1. Go to website.com/login
2. Add a incorrect user / pass
3. Press Login button

**Expected result:**
User shouldn't be able to login and it gets an error message.
THe error message should be: 
"Failed login!
Incorrect username or password.
Please try again here."

**Test Data:**
User: paul.213 & Pass: paul12123


------------------------

**Description:** 
Ensure that the system prevents unauthorized access to the user's account by changing the URL.

**Steps to Reproduce:**
1. Go to website.com/login
2. Manually modify the URL from website.com/login to website.com/myaccount

**Expected result:**
The system should recognize that the user is not authenticated or authorized.
The user should be redirected to the login page or another appropriate page indicating unauthorized access.

**Test Data:**
Correct URL: website.com/login
Modified URL: website.com/myaccount


------------------------

**Description:** 
Check if the login works when a person uses a corect user/pass and Remember Me checked. 
Check if the 'Remember Me' function works for future attempts to login without re-entering credentials.

**Steps to Reproduce:**
1. Go to website.com/login
2. Insert a correct user / pass
3. Check the Remember Me
4. Press Login button
5. Logout
6. Return to website.com/login
7. Check that previous credentials are pre-filled and remember me checked
8. Press Login button without re-entering any credentials

**Expected result:**
User should be able to login and is taken to his profile page.
After logout, the user's credentials should be remembered and pre-filled for future login sessions.
The user should be able to re-login by pressing login button without reintroducing his credentials.

**Test Data:**
User: paulp & Pass: paulp


------------------------

**Description:** 
Check for SQL injection vulnerabilites in the loggin form.

**Steps to Reproduce:**
1. Go to website.com/login
2. Insert an SQL injection attempt into the user field
3. Press Login button
4. Observe the system's response to the SQL injection
5. Repeat the steps 2, 3, 4 but with the password field

**Expected result:**
The system should reject SQL injection attempts in both the username and password fields.
Any SQL injection attempts should result in appropriate error message. 

**Test Data:**
user: 59 OR 1=1
password: " or ""="


# Emag.ro Test Cases Examples 

Below are some Test Case examples for https://www.emag.ro

----------------

**Description:** 
Verify that the search bar is working with a basic search.

**Steps to Reproduce:**
1. Go to the emag.ro search bar
2. Type a common keyword into the search bar
3. Press enter key or click the "Search" button

**Expected result:**
The search results page should show only relevant items related to the entered keyword.
Ex: For keyword "iphone" the system should know that I want to search for Iphone mobile phones and the results page should show only items that are related to Iphone phones or accessories.

**Test Data:**
keywords: "iphone" "apple" "samsung"


----------------

**Description:** 
Verify that the search bar provides relevant autocomplete suggestions.

**Steps to Reproduce:**
1. Go to the emag.ro search bar
2. Enter a partial keyword 
3. Wait for some autocomplete suggestions.
4. Press enter key or click the "Search" button

**Expected result:**
The search bar should provide autocomplete suggestions correctly, after the minimul three letters.
Selecting one, it should navigate to the corresponding results.
The search bar should display the closest and most searched suggestions for the partial keyword entered, and afterward, the other items if they exist.
Example: For the keyword "app" the system should display autocomplete suggestions for Apple devices, and afterwards, should show items like "Applaws".

**Test Data:**
partial keywords: "app" "ipho" "sams" "leno" 


----------------

**Description:** 
Ensure that the search bar handles empty searches.

**Steps to Reproduce:**
1. Go to the emag.ro search bar
2. Click on the search bar but don't type anything.
3. Press enter key or click the "Search" button

**Expected result:**
The search bar should provide autocomplete suggestions correctly, after the minimul three letters.
Selecting one, it should navigate to the corresponding results.
The search bar should display the closest and most searched suggestions for the partial keyword entered, and afterward, the other items if they exist.
Example: For the keyword "app" the system should display autocomplete suggestions for Apple devices, and afterwards, should show items like "Applaws".

**Test Data:**
The search bar should remain intact, and nothing should happen.


----------------

**Description:** 
Verify that the search bar handles special characters appropriately.

**Steps to Reproduce:**
1. Go to the emag.ro search bar.
2. Type some special characters in the search bar
4. Press enter key or click the "Search" button

**Expected result:**
The search bar should successfully handle special characters and return a feedback message with an error.
The error message should be: 0 rezultate pentru: "special caracters that we was interested".
Below we should see some suggestions for finding the desired item:

"Pentru a gasi produsul dorit, incearca urmatoarele:

Verifica daca ai scris corect termenii.
Incearca sa folosesti sinonime.
Incearca din nou, folosind o cautare mai generala."

Below the suggestions, we should see the most searched items at this moment.

**Test Data:**
special characters: "^&)#*"
