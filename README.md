# BFund - webapp

How this web application works

Application for members to view and opt-in to PRODUCTS presented via page/posts

The site will host 4 PUBLIC pages. 3 static and 1 dynamic for LOG-IN

Site will PRIVATE sites:
DASHBOARD;
USER ACCOUNT INFO;
SELECTED OPT-INs;
USER SERVICES CONCIERGE;
PRODUCT PAGE;
API PAGE;

Site will have 4 levels of access to private sites
Public - level 0
USER (level 1) - view DASHBOARD, PRODUCT PAGE, SELECTED OPT-INs; USER SERVICES CONCIERE; edit USER ACCOUNT INFO
API/Dev (level 2) - edit DASHBOARD, PRODUCT PAGE, SELECTED OPT-INs, USER ACCOUNT INFO, API PAGE
Master (Level 3) - edit all


Log in dynamic site will check username and password against secure user database;

Upon TRUE response from database, PERMISSIONS to PRIVATE pages/posts are granted, user is forwarded to DASHBOARD page and information is displayed through a VIEWER using GET from USER database model

<DASHBOARD page
Center/BODY of the dashboard viewer LINKED PRODUCT TEASER to products will be PRINTED if they are ACTIVE for opt-in.

Left/NAV 
LINK to account info/USER DATABASE EDIT page
LINK Current product opt-ins/USER DATABASE SELECTED OPT-INS page
LINK to USER SERVICES CONCEIERGE 

</Dashboard

<Product page
Print Product descriptions/PRODUCT ASSETS 
Product Opt-in/TOGGLE BUTTON to OPTIN (EDIT USER DATABASE)
</Product page

<API page
APIuser DISPLAYS: each Product and "OPT-Ins" to product by userName
DISPLAYS each PRODUCT with toggle for ACTIVE/INACTIVE
</API page

DATABASES required:
1. USER
  DB info required: permissionLevel; userName, password, firstName, lastName, email, birthDate, phoneNumber, {repeating} productOptInX, optInForXCost.
2. PRODUCT
  DB info required: productName, productQualities, ProductActive.
