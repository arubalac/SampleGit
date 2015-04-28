##Tutorial

CIP-700-B Tutorial - Create a portal and a notebook for the API

##Objective

Create a notebook for CIP-100 tutorial API created earlier.

Completion Time: 30 minutes

##Introduction

This tutorial will guide you through the development of an API notebook. API notebook will provide documentation and executable App examples for App developers.

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

**Note:** if you are not at CISCO Live San Diego, create an account your own account of mule soft API manager using the below URL.

[https://anypoint.mulesoft.com/#/signup?apintent=apiplatform](https://anypoint.mulesoft.com/#/signup?apintent=apiplatform)

And download the Postman REST client using the below URL and install it in your machine.

[https://www.getpostman.com/](https://www.getpostman.com/)

##Steps

**_Login to API manager_**

Use the below URL for accessing the API manager. Provide your credentials as given below.

[https://webapi.cisco.com/accounts/#/signin](https://webapi.cisco.com/accounts/#/signin)

## _![Figure](/posts/files/cip-lab-700B/LoginScreen.png)_

Click the APIs tab on upper right hand corner

## _![Figure](/posts/files/cip-lab-700B/CIPHomeScreen.png)_

The above step will take you to the API creation\search page. Enter the API name you have created on CIP-100 tutorial and click “Enter”..

## _![Figure](/posts/files/cip-lab-700B/SelectHelloRAMLAPI.png)_

Click on the API name. HelloRAML API.

This will bring up the API detail page.

**_Creating an API Portal_**

Click on the drop down box in the API Portal as shown in below and select the option Create new portal.

If you have already created a portal in CIP 700-A tutorial then click on **Edit portal**.

## _![Figure](/posts/files/cip-lab-700B/EditHelloRAMLPortal.png)_

 This will take you the new portal page shown below.

## _![Figure](/posts/files/cip-lab-700B/EditHelloRAMLPortal.png)_

**_API Notebook_**

To create the notebook for your API click on the Add drop down on the left panel of the Portal editor and select the **API Notebook** option as shown below.

## _![Figure](/posts/files/cip-lab-700B/SelectAPINotebook.png)_

Once you click the API Notebook option, you could see the below screen with default JavaScript client for your API created. The client will be used for invoking the resource for your API.

Before writing the notebook code snippets and running the default client script. Ensure that your default client script executes properly for which you need go back to you API designer as done in CIP-100 tutorial

and verify the mock service is in **on** state and the base URI is shown as mock service URI as shown in the screen below.

## _![Figure](/posts/files/cip-lab-700B/EnableMockService.png)_

To ensure that the mock service URL is saved and not lost when jumping into notebook click on the **Save** button on top panel of your API designer as shown in the below screen and then click on the **Save All** sub option.

## _![Figure](/posts/files/cip-lab-700B/SaveAllAfterMockEnable.png)_

We can test the default client script shown in the API notebook by clicking

the **Play notebook** button on top right of the notebook editor as shown in the screen below.

## _![Figure](/posts/files/cip-lab-700B/ClickPlayButton.png)_

**Note:** Once you are in preview mode in API notebook editor . To add further code snippet you need to click on the **Edit** button on the top right of your notebook editor.

Once you click the **Play notebook** button you should see the execution successful without any error as shown in the screen below.

## _![Figure](/posts/files/cip-lab-700B/ClientExecuted.png)_

Now let’s try accessing the /employee/details resource of HelloRAML API. To do this select the code cell below the client code block as shown in the screen below.

## _![Figure](/posts/files/cip-lab-700B/IinsertCodeCell.png)_

In the new code cell type the below snippet of code to get the complete response of your **/employees/details** resource. Check the screen below.

```
client.employees.details.get()
```
## _![Figure](/posts/files/cip-lab-700B/insertCodeinCell.png)_

Once you added the code snippet let’s try running the notebook and see the result. In the below screen you can see that the execution of the API notebook retuned the example response of your API.

## _![Figure](/posts/files/cip-lab-700B/OutputOfNotebookforCodeCell.png)_

Now let’s assign the response of the API to a variable and try to access the variable in a new code snippet. For this let edit the earlier snippet of the code by adding a variable as shown below.

```
var response = client.employees.details.get()
```
And add the below snippet of code in a new code cell as shown in below screen. Using the below snippet you will retrieving the **_Group_** value from the response (shown in above screen) payload from your API

```
response.body.data.Group
```

## _![Figure](/posts/files/cip-lab-700B/BodyGroup.png)_ 

In the above screen you can see that the Group value returned is **“APG”**

** **

Now one of the unique parts of the API notebook is that you can add text details in between your scripts for the app developers \ API users to understand you code easily and also for better explanation of your use case.

** **

Let’s try adding some texts in between the scripts. For this take your mouse cursor on top the first code snippet and select the text cell option as shown in the screen below.

## _![Figure](/posts/files/cip-lab-700B/InsertTextCell.png)_ 

Once the text cell is inserted add the content you need to add as shown in the below screen.

## _![Figure](/posts/files/cip-lab-700B/AddConentinTextCell.png)_ 

You can use HTML also as part of the text cell. Let’s try by adding another text cell above the third code snippet and apply a simple HTML as shown below.

<table>
<tbody>
<tr>
<td width="638">
<h3><i><font size="8" color="red"><b> The below code will return the Group name of the employee</b></font></i></h3>

</td>

</tr>

<tr>
<td width="638">

</td>

</tr>

</tbody>

</table>

## _![Figure](/posts/files/cip-lab-700B/AddHTML.png)_

Let’s see the preview of the API notebook by clicking the Preview button on top right.

## _![Figure](/posts/files/cip-lab-700B/PreviewNotebook.png)_

Now let’s try running the API notebook for the final finale of this tutorial. As done earlier click on the **Play notebook**.

## _![Figure](/posts/files/cip-lab-700B/PlayNoteAfterPreview.png)_

Congratulation, now you have created the API notebook for your API.

Great way to go.

For more detailed feature reference and capabilities of API notebook check the reference section.

**Reference**

[http://raml.org/docs.html](http://raml.org/docs.html) - For RAML

[http://api-notebook.anypoint.mulesoft.com/](http://api-notebook.anypoint.mulesoft.com/) - For API notebook

[http://www.w3schools.com/](http://www.w3schools.com/) - For HTML and JavaScript

**Next                                                          **

*   CIP-800 Challenge - Create the portal and notebook for CIP-500 challenge API
