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

Site will have 4 levels of access to PRIVATE sites<br><br>
Public - level 0<br><br>
USER (level 1) - <br>view DASHBOARD, <br>view SELECTED OPT-INs; <br>view USER SERVICES CONCIERE; <br>toggle PRODUCT PAGE, <br>edit USER ACCOUNT INFO<br><br>
API/Dev (level 2) - <br>edit SELECTED OPT-INs, <br>edit USER ACCOUNT INFO, <br>view DASHBOARD, <br>edit PRODUCT PAGE, <br>view API PAGE<br><br>
Master (Level 3) - edit all<br><br>

Log in dynamic site will check username and password against USER database;

Upon TRUE response from database, PERMISSIONS to PRIVATE pages/posts are granted, user is forwarded to DASHBOARD page and information is displayed through a VIEWER using GET from USER database model

DASHBOARD page<br><br>

  &nbsp;&nbsp;&nbsp;&nbsp;Center/BODY of the dashboard viewer LINKED PRODUCT TEASER to products will be PRINTED if they are ACTIVE for opt-in.<br>
  &nbsp;&nbsp;&nbsp;&nbsp;Left/NAV <br>
  &nbsp;&nbsp;&nbsp;&nbsp;LINK to account info/USER DATABASE EDIT page<br>
  &nbsp;&nbsp;&nbsp;&nbsp;LINK Current product opt-ins/USER DATABASE SELECTED OPT-INS page<br>
  &nbsp;&nbsp;&nbsp;&nbsp;LINK to USER SERVICES CONCEIERGE <br>

USER ACCOUNT INFO page<br><br>
&nbsp;&nbsp;&nbsp;&nbsp;Print USER info fields: userName, firstName, lastName, email, phoneNumber<br>
&nbsp;&nbsp;&nbsp;&nbsp;Request edits and allow updates<br>


SELECTED OPT-INS page<br><br>
&nbsp;&nbsp;&nbsp;&nbsp;Print PRODUCTS which USER has selected to opt-in <br>
&nbsp;&nbsp;&nbsp;&nbsp;Link to product page<br>


USER SERVICES CONCIERGE page <br><br>

&nbsp;&nbsp;&nbsp;&nbsp;FAQ tabs<br>
&nbsp;&nbsp;&nbsp;&nbsp;Report requests<br>
&nbsp;&nbsp;&nbsp;&nbsp;USER history widget<br>

PRODUCT page<br><br>
&nbsp;&nbsp;&nbsp;&nbsp;Print Product descriptions/PRODUCT ASSETS <br>
&nbsp;&nbsp;&nbsp;&nbsp;Product Opt-in/TOGGLE BUTTON to OPTIN (EDIT USER DATABASE)<br>

API page<br><br>

&nbsp;&nbsp;&nbsp;&nbsp;APIuser DISPLAYS: each Product and "OPT-Ins" to product by userName<br>
&nbsp;&nbsp;&nbsp;&nbsp;DISPLAYS each PRODUCT with toggle for ACTIVE/INACTIVE<br>


DATABASES required:
1. USER
  DB info required: <br>permissionLevel; <br>userName, <br>password, <br>firstName, <br>lastName, <br>email, <br>birthDate, <br>phoneNumber, <br>{repeating} productOptInX, optInForXCost.<br>
2. PRODUCT
  DB info required: <br>productName, <br>productQualities(tradeSecret), <br>productActive.
