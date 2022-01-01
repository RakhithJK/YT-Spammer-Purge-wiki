# Setting Up a Google Cloud Project / Obtaining API Credentials

### To use the program, you will need an "Oauth2" credential to access the scanning and deletion functions via YouTube's Data API. Otherwise this script won't work at all.  
* ### **Video Walkthrough Here: <https://www.youtube.com/watch?v=c6ebWvay8dE>** 
***

## Steps:

#### 1. Log into [Google Developer's Console](https://console.cloud.google.com/apis/dashboard) with your Google account that has your YouTube channel.  

#### 2. On the top blue bar nex to where it says "Google Cloud Platform", click the dropdown to 'Select a Project'. (If you have existing projects, it may instead show the name of one)

   <p align="center"><img width="530" alt="2" src="https://user-images.githubusercontent.com/12518330/139733945-f80b9eed-9847-4459-bbe2-7f252707b20d.png"></p>

#### 3. In the "Select a Project" Window click "New Project"

   <p align="center"><img width="599" alt="3" src="https://user-images.githubusercontent.com/12518330/139733959-72cf691f-7332-4be6-8c61-adbe437b2386.png"></p>

#### 4. Enter some project name, it doesn't really matter, then click 'Create'

   <p align="center"><img width="440" alt="4" src="https://user-images.githubusercontent.com/12518330/139733967-e233a183-f9c3-4f5b-89de-606b08996848.png"></p>

#### 5. Make sure the project you just created is active, with it showing at the top, then click "Library" on the left menu.

   <p align="center"><img width="617" alt="5" src="https://user-images.githubusercontent.com/12518330/139733984-fd2163fd-5848-47bc-bb96-a7cde8534e6c.png"></p>

#### 6. Scroll down and click the box that says "YouTube Data API v3"

   <p align="center"><img width="635" alt="6" src="https://user-images.githubusercontent.com/12518330/139733998-b309d84b-e2ab-4af3-bd71-2e2c921a62bc.png"></p>

#### 7. Click "Enable" and wait for it to load. It will take you to another page.

   <p align="center"><img width="503" alt="7" src="https://user-images.githubusercontent.com/12518330/139734007-091f7402-cca4-468f-9f68-61b10dd5f510.png"></p>

#### 8. Click "Create Credentials".
(Note: If you don't see this page, open the left pop-out menu and click "APIs & Services" > "Dashboard". Then in the table/list on the page, look in the 'Name' column, and click "YouTube Data API v3")

   <p align="center"><img width="759" alt="8" src="https://user-images.githubusercontent.com/12518330/139734018-cd85d035-2d21-4f3d-aa06-70aa2b2daa6f.png"></p>

#### 9. In the dropdown, select "YouTube Data API v3", then select "User Data", and click Next

   <p align="center"><img width="625" alt="9" src="https://user-images.githubusercontent.com/12518330/139734039-454c1a5d-8927-4a51-826f-84927b0e2148.png"></p>

#### 10. Under "Oauth Consent Screen", fill out the required fields with some name, select your email, and enter an email below too. It doesn't really matter what you put here. Then click "Save and Continue"

   <p align="center"><img width="461" alt="10" src="https://user-images.githubusercontent.com/12518330/139734052-6b5ab0b6-9a0d-41fd-a2fa-c36dfce599a3.png"></p>

#### 11. Click "Add or Remove Scopes", then find the one that says ".../auth/youtube.force-ssl", click the check box, then at the bottom click "Update". Then click "Save and Continue"

   <p align="center"><img width="422" alt="11 1" src="https://user-images.githubusercontent.com/12518330/139734064-221fedee-988f-4103-8718-f082eae9df12.png">
   <img width="546" alt="11 2" src="https://user-images.githubusercontent.com/12518330/139734072-9be172a0-8b12-418a-ba8d-feab6e303058.png"></p>

#### 12. Under "Oauth Client ID", just select 'Desktop App'. You can set a name or not. Then click "create".

   <p align="center"><img width="452" alt="12" src="https://user-images.githubusercontent.com/12518330/139734091-2ee876c0-b4b2-4324-9f13-2f6f80d7e8bf.png"></p>

#### 13. Now click "Download" to download the credentials json file. Rename it to `client_secrets.json` and save it into the same directory as the python script. Then click done.

   <p align="center"><img width="462" alt="13" src="https://user-images.githubusercontent.com/12518330/139734114-95ce0476-fcf2-4618-8966-525734b2a3bb.png">
   <img width="354" alt="13 2" src="https://user-images.githubusercontent.com/12518330/139736335-ee5f3b95-2ed4-4f8e-971c-06d659018d4e.png"></p>

#### 14. When trying to log in you may get a "403 Access_Denied" error. If so, you need to add yourself as an authorized user. On the left menu, go to APIs & Services > Oauth Consent Screen > Under Test Users, Click "Add Users". On the pop out window, type in your same Google/channel account email into the box and hit Save.

   <p align="center"><img width="584" alt="14" src="https://user-images.githubusercontent.com/12518330/139734123-64eb4583-686a-4b5a-a4a1-54393f6b97f0.png"></p>
   <p align="center"><img width="595" alt="14 2" src="https://user-images.githubusercontent.com/12518330/139734814-26d04eed-76b6-4b4f-9689-e6960f781faa.png"></p>

#### 15. Now you should be able to run the python script, and it will ask you to log in.
