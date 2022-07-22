#Diagnostic and changes proposed
##Diagnostic
Test with default values (user is not admin)
| HTTP Verb | Route | Result | Expected |
| --------- | ------------------ | ------ | -------- |
| POST | /api/auth/register | 201 | Yes |
| POST | /api/auth/login | 403 | Yes |
| GET | /api/products | 200 | Yes |
| GET | /api/users | 401 | Yes |
| GET | /api/carts | 401 | Yes |
| GET | /api/orders | 401 | Yes |
* Current rules at User establish some properties as unique, this has not been taken into account at auth.js

##Changes proposed
* Use OpenAPI for testing
* Add Express Error Handler
* Add morgan and cors
* Use always gitignore