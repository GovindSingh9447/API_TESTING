Vconnect (21-03-2022)
AQDPP8277H

api name----GET_COMPANY_DETAILS
GET
url-----https://api.probe42.in/probe_lite/companies/{companyId}/base-details
request
---------
{"companyId":"U65990MH1980PTC022973"}

headers
---------
x-api-version=1.2
x-api-key=4QxpnPFfTOajp6DOgySzh4q3je7gN1AO9EZn0oDT





APi name------PAN_VERIFICATION(vahanahub failover)     

 {"pan_number":"EQMPR2307P"}

post
url-------------
http://13.234.89.71:9040/vahanahub-failover/verification/performPanVerification

request
{"pan_number":"<pan_no>"}


headers:
p_details_required=Y
authbridgeuser=test@decimal.co.in
x-api-key=aetgkmvd81743n0bmywkod31056vwneh
primaryvendor=AUTH_BRIDGE

-------------------------------------------


========================
Check the environment we have synced…If UAT use uat URL else use sandbox url

uat url----https://vahanahub-uat.vahanacloud.com/router/engine/v1/gatewayProcessor
https://vahanahub-uat.vahanacloud.com/vahanahub/execution/executeService


In case UAT URL is not available we can use sandbox URL
Sandbox url : https://sandbox.vahanacloud.com/router/engine/v1/gatewayProcessor

Vconnect (22-03-2022)
================================================
22/3/2022
=================================================
creating get api with queryParam
=====================================

url:https://api.probe42.in/probe_lite/companies?limit=25&filters=%7B%22nameStartsWith%22%3A%22Godrej%22%7D

headers
---------
x-api-version=1.2
x-api-key=4QxpnPFfTOajp6DOgySzh4q3je7gN1AO9EZn0oDT

pass through
-------------------
APi name------PAN_VERIFICATION_PASSTHRU
post
url-------------
http://13.234.89.71:9040/vahanahub-failover/verification/performPanVerification
request
{"pan_number":"<pan_no>"}


headers:
p_details_required=Y
authbridgeuser=test@decimal.co.in
x-api-key=aetgkmvd81743n0bmywkod31056vwneh
primaryvendor=AUTH_BRIDGE

Creating Templates
---------------------------




database details
------------------------
DATABASE_TYPE : POSTGRES
DATABASE_IP : 13.127.54.186
DATABASE_PORT : 5432DATABASE_NAME : training
DATABASE_SCHEMA : public
D
ATABASE_USER : training
DATABASE_PASSWORD : training


function name:sp_get_product_details


========================================================

File_upload
—--------------------
url:https://sm-itr-sandbox.scoreme.in/itr/external/pdfFileUploadRequest


headers:clientId=a71e5bf6139cdffdb6fdee2fad13c971
, clientSecret=eef408234916ac215f3743626ef5ccbfd3042423a55a1833a887b32e7975acc9
request type:MULTI-PART-REQUEST

request:

{
  "file": [
    "https://decimal-integrations.s3.ap-south-1.amazonaws.com/MDSABD820020220211144008945_NA/MDSABD82002022021114400894519%3A17%3A07.104.pdf"
  ],
  "payload": {
    "tag": "CZWPK9724Q",
    "pan": "CZWPK9724Q"
  }
}

25/3/2022(Excercise)
==================================
1)SEVERE_WEATHER_ALERTS_BY_LAT_LON
GET  API
URL:https://api.weatherbit.io/v2.0/alerts?lat=38.123&lon=-78.543&key=e2c71cab8f9b47dfad68adbb92bb71d2

2)CREATE_HUBBLE
POST
URL:https://hub-uat.vahanacloud.com/fullerton/generateHubble
headers:client=DECIMAL
vendorurl=https://hubbleuat.fullertonindia.com/hubble
corgid=corgid
cappid=cappid
request
----------------
{
  "refId": "<Any random string>",
  "requestData": {
    "Customer_Name": "SUBHAU NATH",
    "firstName": "SUBHAU",
    "lastName": "NATH",
    "pan_FirstName": "SUBHAU",
    "pan_MiddleName": "",
    "pan_LastName": "NATH",
    "Email": "abcd1234@gmail.com",
    "l_Gender": "MALE",
    "l_PAN": "AFIPN4808G",
    "MobilePhone": "9876543213",
    "l_DOB": "10/09/1995",
    "l_MaritalStatus": "SINGLE",
    "l_Qualification": "GRADUATE",
    "accomodationType": "RENTED",
    "resident_address": "Home Line 1, Home line 2",
    "resident_pincode": "560100",
    "l_Currentpincode": "560100",
    "noOfMonthsAtCurrentAddress": "51",
    "l_Permanentiscurrent": "No",
    "l_Permanent_Landmark": "Tower",
    "l_Per_Res_Address1": "Line1",
    "l_Per_Res_Address2": "Line2",
    "l_Per_Res_Address3": "Line3",
    "l_Type_Permanent_Res": "RENTED",
    "FieldID_994": "400076",
    "l_Emp_Type": "SALARIED",
    "l_OrganizationType": "MNC",
    "CompanyName": "Company Name ",
    "office_address": "Office Line1, office Line 2 ",
    "office_pincode": "560100",
    "l_Total_Work_Exp_Mnths": "91",
    "l_Gross_Monthly_Income": "87375",
    "l_Loan_Amount_Applied": "615000",
    "l_Lead_Source": "Dealer",
    "l_Lead_Sub_source": "Mass Channels",
    "l_AIP_Tenure": "48",
    "finalTenureRequired": "48",
    "ProductCode": "DPL",
    "l_Alternate_Email": "abdef1234@gmail.com",
    "l_Current_Landmark": "Bangalore",
    "l_Office_Landmark": "Bangalore",
    "l_IndustryType": "11",
    "purposeOfLoan": "21"
  },
  "documentDetails": [
    {
      "url": "<url value>",
      "documentType": "INCOME_PRO0F"
    }
  ]
}


3)INITIATE_OTP
url:https://uat2.zumigo.com/zumigows/initiateOTP
post
Headers:
Accept=application/json
clientId=DECIMALUAT
Authorization=Basic ZGVjaW1hbHVhdHVzZXI6VEUyU0JWQiZaY1Vycj9kZQ==

request
============
{
  "mobilePossession": {
    "mdn": "<phoneno with country code>",
    "timeToLive": "<The length of time, in seconds,that the           one-time passcode is valid and Valid values are 60 to 600 >",
    "otpMethod": "sms"
  }
}

4)database details
------------------------
DATABASE_TYPE : POSTGRES
DATABASE_IP : 13.127.54.186
DATABASE_PORT : 5432
DATABASE_NAME : training
DATABASE_SCHEMA : public
DATABASE_USER : training
DATABASE_PASSWORD : training

any function starting with get_


5)
a)GET_ACCESS_TOKEN
post
url:https://dad-api.indifi.com/auth/token
body
=======
client_id=F5ZJ6YHX0E55DMCL873
client_secret=drgvTJEvsIeghj2shzphfDLMCNCMJc
grant_type=client_credentials

b)VERIFY_LEAD
PUT
https://dad-api.indifi.com/applications/create-lead/{application_id}
header
-----------
Authorization=access token generate from previous api

body:

applicationId=application_id=f20d9ba2-8b7b-453e-af7e-1f04a66dd40e
phone=8700636291
otp=9598


===============================================











