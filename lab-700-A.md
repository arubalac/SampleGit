##Tutorial

CIP-700-A Tutorial - Create a portal for the API

##Objective

Create a portal and notebook for CIP-100 tutorial API created earlier.

##Completion Time 

30 minutes

##Introduction

This tutorial will guide you through the development of an API portal.

##Assumptions

You know how to create an API in API designer and how to test your API using API console.

Basics knowledge and understanding on HTML and JavaScript

The following may be useful as references for the above

[http://raml.org/docs.html](http://raml.org/docs.html) - For RAML

[http://api-notebook.anypoint.mulesoft.com/](http://api-notebook.anypoint.mulesoft.com/) - For API notebook

[http://www.w3schools.com/](http://www.w3schools.com/) - For HTML and JavaScript

##Prerequisites

Access to API manager

**_URL:_** [https://webapi.cisco.com/accounts/#/signin](https://webapi.cisco.com/accounts/#/signin)

Completed the CIP-100 tutorial and CIP-600 tutorial.

**_Note:_** if you are not at CISCO Live San Diego, create an account your own account of mule soft API manager using the below URL.

[https://anypoint.mulesoft.com/#/signup?apintent=apiplatform](https://anypoint.mulesoft.com/#/signup?apintent=apiplatform)

And download the Postman REST client using the below URL and install it in your machine .

[https://www.getpostman.com/](https://www.getpostman.com/)

##Steps

**_Login to API manager_**

Use the below URL for accessing the API manager. Provide your credentials as given below.

[https://webapi.cisco.com/accounts/#/signin](https://webapi.cisco.com/accounts/#/signin)

## _![Figure](/posts/files/cip-lab-700A/LoginScreen.png)_

Click the APIs tab on upper right hand corner

## _![Figure](/posts/files/cip-lab-700A/CIPHomeScreen.png)_

The above step will take you to the API creation\search page. Enter the API name you have created on CIP-100 tutorial and click “Enter”..

## _![Figure](/posts/files/cip-lab-700A/SelectHelloRAMLAPI.png)_

Click on the API name. HelloRAML API.

This will bring up the API detail page.

**_Creating an API Portal_**

Click on the drop down box in the API Portal as shown i below and select the option **Create new portal**.

## _![Figure](/posts/files/cip-lab-700A/HelloRAMLHomeScreen.png)_

 This will take you the new portal page shown below.

## _![Figure](/posts/files/cip-lab-700A/PortalHomePageEdit.png)_

We create content starting with the **Home** page. Click on the **Edit** button as shown below

Enter text as shown below.

## _![Figure](/posts/files/cip-lab-700A/AddingContentHome.png)_

You can preview your page by clicking the Preview button on top right of Home page as shown in  screen below.

## _![Figure](/posts/files/cip-lab-700A/PreviewButton.png)_

The preview will result in a page as shown below.

## _![Figure](/posts/files/cip-lab-700A/PreviewPage.png)_

If satisfied with this content click on the **Save** button .

## _![Figure](/posts/files/cip-lab-700A/SaveButton.png)_

The API portal pages support HTML tags.

To place HTML tags in the Home Page click on the **Edit** button again and ad the HTML tags shown below.
```
<h1>my first html tag entry....... <h1>

<h2 > <font size="8" color="red"><b> my html entry with color...... </b></font></h2>

<h3><i>An italic entry.....</i></h3>
```
## _![Figure](/posts/files/cip-lab-700A/HtlmEntry.png)_
Click on the **Preview** button to see the page content as modified with the HTML Tags..

## _![Figure](/posts/files/cip-lab-700A/PreviewHTMLEntry.png)_

If satisfied with this content click on the **Save** button.

Click on the API reference link on the left hand side of the editor to view the API resources available for API.

## _![Figure](/posts/files/cip-lab-700A/APIRefernceConsole.png)_

You can a new page to your portal by clicking on the **Add** drop down on left side of the portal editor and select **Page** option as shown in the screen below.

## _![Figure](/posts/files/cip-lab-700A/CreateAdditonalPage.png)_

This will give you a screen where you can edit the page with either text or HTML.

## _![Figure](/posts/files/cip-lab-700A/EditNewPage.png)_

Congratulation, now you have created the API portal for your API.

Great way to go.

For more detailed feature reference and capabilities of API portal check the reference section.

##Reference

[http://raml.org/docs.html](http://raml.org/docs.html) - For RAML

[http://api-notebook.anypoint.mulesoft.com/](http://api-notebook.anypoint.mulesoft.com/) - For API notebook

[http://www.w3schools.com/](http://www.w3schools.com/) - For HTML and JavaScript

##Next                                                          

*  CIP-700-B Tutorial - Create a notebook for the API
