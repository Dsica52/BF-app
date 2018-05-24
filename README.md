# BFund - webapp

How this web application works

Application is for members to view and opt-in to PRODUCTS presented via pages

The site will host 4 PUBLIC pages. 3 static and 1 dynamic for LOG-IN

Site will 6 PRIVATE pages:<br>
DASHBOARD;<br>
USER ACCOUNT INFO;<br>
SELECTED OPT-INs;<br>
USER SERVICES CONCIERGE;<br>
PRODUCT PAGE;<br>
API PAGE;<br>

Site will have 4 levels of access to PRIVATE sites<br>
Public - level 0<br><br>
USER (level 1) - <br>view DASHBOARD, <br>view SELECTED OPT-INs; <br>view USER SERVICES CONCIERE; <br>toggle PRODUCT PAGE, <br>edit USER ACCOUNT INFO<br><br>
API/Dev (level 2) - <br>edit SELECTED OPT-INs, <br>edit USER ACCOUNT INFO, <br>view DASHBOARD, <br>edit PRODUCT PAGE, <br>view API PAGE<br><br>
Master (Level 3) - edit all<br>

Log in dynamic site will check username and password against USER database;

Upon TRUE response from database, PERMISSIONS to PRIVATE pages/posts are granted, user is forwarded to DASHBOARD page and information is displayed through a VIEWER using GET from USER database model

DASHBOARD page

  Center/BODY of the dashboard viewer LINKED PRODUCT TEASER to products will be PRINTED if they are ACTIVE for opt-in.

  Left/NAV 
  LINK to account info/USER DATABASE EDIT page
  LINK Current product opt-ins/USER DATABASE SELECTED OPT-INS page
  LINK to USER SERVICES CONCEIERGE 
</

USER ACCOUNT INFO page
  Print USER info fields: userName, firstName, lastName, email, phoneNumber
  Request edits and allow updates
</

SELECTED OPT-INS page
  Print PRODUCTS which USER has selected to opt-in 
  Link to product page
</

USER SERVICES CONCIERGE page 
  FAQ tabs
  Report requests
  USER history widget

PRODUCT page
  Print Product descriptions/PRODUCT ASSETS 
  Product Opt-in/TOGGLE BUTTON to OPTIN (EDIT USER DATABASE)
</  

API page
  APIuser DISPLAYS: each Product and "OPT-Ins" to product by userName
  DISPLAYS each PRODUCT with toggle for ACTIVE/INACTIVE
</

DATABASES required:
1. USER
  DB info required: permissionLevel; userName, password, firstName, lastName, email, birthDate, phoneNumber, {repeating} productOptInX, optInForXCost.
2. PRODUCT
  DB info required: productName, productQualities(tradeSecret), productActive.
