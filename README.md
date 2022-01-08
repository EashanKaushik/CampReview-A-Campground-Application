# CampReview-A-Campground-Application

## Introduction

Yelp Camp is a more complex application built from scratch using the latest website creating tools. The project aims to create a fully functional website with UI application using JavaScript. Innovative styling will be done by CSS3 and an easy index HTML code created using HTML5. It focuses on using NodeJS as the backend tool as the website will be heavily integrated with JavaScript and also use Jquery. The authentication part is handled with PassportJs, I also used a non relationnal database: MongoDB. Finally, all geolocations and maps come from the Google Map API. You can inspect the package.json's file to check all the npm modules used.
Our application is hosted using heroku and we have used GroomIDE as our development environment. This entire project is made on cloud infrastructure as a result we have used MongoDB on cloud known as MongoDB Atlas.

## Modules/Features

• Authentication:  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;o	User login with username and password  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;o	Admin sign-up with admin code  
•	Authorization:  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;o	One cannot manage posts and view user profile without being authenticated  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; o	One cannot edit or delete posts and comments created by other users  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; o	Admin can manage all posts and comments  
•	Manage campground posts with basic functionalities:  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;    o	Create, edit and delete posts and comments  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;    o	Upload campground photos  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;    o	Display campground location on Google Maps  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;    o	Search existing campgrounds  
•	Manage account with basic functionalities:  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;    o	Profile page setup with sign-up  
•	Flash messages responding to users' interaction with the app  
•	Responsive web design  

## Proposed System Design 

Class Diagram 

![image](https://user-images.githubusercontent.com/50113394/148662688-6b437b0e-007b-42f6-ae06-ad6ff15e1f3d.png)

State Diagram

![image](https://user-images.githubusercontent.com/50113394/148662695-bb1b84df-4a38-4162-b071-4eee90b057c7.png)

## Steps to Deploy

### Step 1
In the Sample.env file:
Port=3002
IP=0.0.0.0
Geocoder= (geocoder api)

### Step 2
For generating google api You need to set a billing accout and create two API keys(Javascript api).
1. Geocoder api
The first api key should be unrestricted and after generating it add it to .env file. 
2. Map api
This api should be restricted.
Go to views > campgrounds > show.ejs
At line 269 add your Map api key.

### Step 3
Create MongoDB cluster here https://www.mongodb.com/cloud/atlas.
After creatring cluster follow path Connect > Connect Your Application > Copy connect link. In app.js replace 'Your mongodb cluster link here' with the generated link.
mongoose.Promise = global.Promise;
mongoose.connect('Your mongodb cluster link here',{useNewUrlParser: true, useUnifiedTopology: true
}).then(() => console.log("Database connected!"))
    .catch((err) => console.log("Database error: " + err.message));
mongoose.set('useFindAndModify', false);
mongoose.set('useCreateIndex', true);


### Step 4: Use GoormIDE to run the application(Perferably)

## Results

### Database Connectivity

![image](https://user-images.githubusercontent.com/50113394/148662780-907630f2-7e7b-4d21-98f2-567c3161e3b4.png)

Database

![image](https://user-images.githubusercontent.com/50113394/148662784-8e33c3da-1d9f-4c58-b0e5-772305ccb935.png)
![image](https://user-images.githubusercontent.com/50113394/148662787-193da7df-4080-4325-9138-0c4af3097fcb.png)

Users

![image](https://user-images.githubusercontent.com/50113394/148662790-b4a3dc39-93ba-4299-83ef-950cbe61781d.png)

Campgrounds

![image](https://user-images.githubusercontent.com/50113394/148662793-2fda27de-eeed-4e2b-b8f1-c19b8d5ce519.png)

Reviews

![image](https://user-images.githubusercontent.com/50113394/148662799-2a88b19f-b45a-4066-8a3e-71ad6dadd710.png)

Comments

![image](https://user-images.githubusercontent.com/50113394/148662801-1725382c-c452-447e-bcf0-4e19607e8233.png)

### Output
![image](https://user-images.githubusercontent.com/50113394/148662748-96edfa7e-bac0-48af-bfe9-065cc927a072.png)
![image](https://user-images.githubusercontent.com/50113394/148662751-4d6c44e1-8d78-4b2f-a245-8934267357db.png)
![image](https://user-images.githubusercontent.com/50113394/148662752-c204c7ee-cfd2-4efb-b543-80bf28ac92c0.png)
![image](https://user-images.githubusercontent.com/50113394/148662757-759da195-865f-42f0-9bb1-0b5ba5eedc21.png)
![image](https://user-images.githubusercontent.com/50113394/148662760-b88f6d28-e0bc-4e6b-9830-31cbaf8bfccc.png)
![image](https://user-images.githubusercontent.com/50113394/148662765-5728bbb9-e25a-4970-9a54-1f2e7a91282f.png)






