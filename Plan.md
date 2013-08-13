
# First version
## Client
### EmailLoginCustom.js - this file will be customized

### EmailLogin.js - this file will not be customized

### EmailLogin.html - a test program

## Server
### EmailLogin.php - server side
1. GenerateEmail(*email address*) - generates password and sends email
	1. creates new password for email
	2. calls CustomConnectToDB/CustomWritePasswordForEmail/CustomDisconnectFromDB
	3. calls CustomSendEmail
2. AuthenticateEmail(*email address*, *password*) - returns true for success, false for error
	1. calls CustomConnectToDB/CustomReadPasswordForEmail/CustomDisconnectFromDB
		* if password does not exist, or wrong password - returns false
		* if password is good returns true, and calls GenerateEmail(...) depending on settings


### EmailLoginCustom.php - this will be customized
1. CustomSendEmail(*email address*) - sends out email
2. CustomConnectToDB() - connects to database
3. CustomReadPasswordForEmail(*email address*) -  returns password for email address
4. CustomWritePasswordForEmail(*email address*, *password*) - returns password
5. CustomDisconnectFromDB() - disconnects from database

