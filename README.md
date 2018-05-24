# BFund - webapp

How this web application works

Application is for members to view and opt-in to PRODUCTS presented via pages

The site will host 4 PUBLIC pages. 3 static and 1 dynamic for LOG-IN

Site will 6 PRIVATE pages:<br>
&nbsp;&nbsp;&nbsp;&nbsp;DASHBOARD;<br>
&nbsp;&nbsp;&nbsp;&nbsp;USER ACCOUNT INFO;<br>
&nbsp;&nbsp;&nbsp;&nbsp;SELECTED OPT-INs;<br>
&nbsp;&nbsp;&nbsp;&nbsp;USER SERVICES CONCIERGE;<br>
&nbsp;&nbsp;&nbsp;&nbsp;PRODUCT PAGE;<br>
&nbsp;&nbsp;&nbsp;&nbsp;API PAGE;<br>

Site will have 4 levels of access to PRIVATE sites<br><br>
Public - level 0<br><br>
USER (level 1) - <br>&nbsp;&nbsp;&nbsp;&nbsp;view DASHBOARD, <br>&nbsp;&nbsp;&nbsp;&nbsp;view SELECTED OPT-INs; <br>&nbsp;&nbsp;&nbsp;&nbsp;view USER SERVICES CONCIERE; <br>&nbsp;&nbsp;&nbsp;&nbsp;toggle PRODUCT PAGE, <br>&nbsp;&nbsp;&nbsp;&nbsp;edit USER ACCOUNT INFO<br><br>
API/Dev (level 2) - <br>&nbsp;&nbsp;&nbsp;&nbsp;edit SELECTED OPT-INs, <br>&nbsp;&nbsp;&nbsp;&nbsp;edit USER ACCOUNT INFO, <br>&nbsp;&nbsp;&nbsp;&nbsp;view DASHBOARD, <br>&nbsp;&nbsp;&nbsp;&nbsp;edit PRODUCT PAGE, <br>&nbsp;&nbsp;&nbsp;&nbsp;view API PAGE<br><br>
Master (Level 3) - edit all<br><br>

LOG IN dynamic page will check username and password against USER database;

Upon TRUE response from database, PERMISSIONS to PRIVATE pages are granted, user is forwarded to DASHBOARD page and information is displayed through a VIEWER using GET from USER database model

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
  DB info required: <br>&nbsp;&nbsp;&nbsp;&nbsp;permissionLevel; <br>&nbsp;&nbsp;&nbsp;&nbsp;userName, <br>&nbsp;&nbsp;&nbsp;&nbsp;password, <br>&nbsp;&nbsp;&nbsp;&nbsp;firstName, <br>&nbsp;&nbsp;&nbsp;&nbsp;lastName, <br>&nbsp;&nbsp;&nbsp;&nbsp;email, <br>&nbsp;&nbsp;&nbsp;&nbsp;birthDate, <br>&nbsp;&nbsp;&nbsp;&nbsp;phoneNumber, <br>&nbsp;&nbsp;&nbsp;&nbsp;{repeating} productOptInX, optInForXCost.<br><br>
2. PRODUCT
  DB info required: <br>&nbsp;&nbsp;&nbsp;&nbsp;productName, <br>&nbsp;&nbsp;&nbsp;&nbsp;productQualities(tradeSecret), <br>&nbsp;&nbsp;&nbsp;&nbsp;productActive.
