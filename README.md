# Tutorial

CIP-100 Tutorial – Building the HelloRAML API

## Objective

Introduce RAML by designing a simple API.

## Completion Time

20 minutes

## Introduction

This tutorial provides the basic steps for developing a simple API.

##Assumptions</font>

You know the basics of RESTful APIs: Resources, methods, HTTP verbs, JSON, XML, If you are not familiar with these, please refer to</font> [http://raml.org/docs.html](http://raml.org/docs.html) <font color='black'>for a quick start.

##Prerequisites

*Access to API manager account.*

[https:webapi.cisco.com/accounts/#/signin](https:webapi.cisco.com/accounts/#/signin)

**_Note:_** if you are not at CISCO Live San Diego, create an account your own account of mule soft API manager using the below URL.

[https://anypoint.mulesoft.com/#/signup?apintent=apiplatform](https://anypoint.mulesoft.com/#/signup?apintent=apiplatform)</font>

##Steps</font>

**_Login to API manager_**

You need the API Designer for RAML creation and editing. API designer is a browser based RAML editor which comes as part of the API manager.

Use the below URL for accessing the API manager. Provide your credentials as given below.</font>

**_URL :_** [https://webapi.cisco.com/accounts/#/signin](https://webapi.cisco.com/accounts/#/signin)

## _![](file:///C:/Users/arubalac/AppData/Local/Temp/msohtmlclip1/01/clip_image002.jpg)_

Click the APIs tab on upper right hand corner

## _![](file:///C:/Users/arubalac/AppData/Local/Temp/msohtmlclip1/01/clip_image004.jpg)_

The above step will take you to the API creation page. Here click on _Add new API_ button.

## _![](file:///C:/Users/arubalac/AppData/Local/Temp/msohtmlclip1/01/clip_image006.jpg)_

Clicking the Add new API button will bring up the form to provide the API primary details. After filling in this form click the Add button. Use the API name in the format as shown in the screen below i.e. API name = HelloRAMLAPI - **_Your name_** or Tutorial 100 -**_Your name_**.

## _![](file:///C:/Users/arubalac/AppData/Local/Temp/msohtmlclip1/01/clip_image008.jpg)_

 After clicking the “ADD” button the following form will be displayed . Click onthe _Define API in the API designer_ link.

## _![](file:///C:/Users/arubalac/AppData/Local/Temp/msohtmlclip1/01/clip_image010.jpg)_

After clicking the link you will see the screen below. Use the central section of the API designer to enter RAML statements.. The box below the main notepad will show RAML semantics suggested for each entry of RAML.

 RAML version, title, API version and base Uri will be automatically populated in the Main Panel.

## _![](file:///C:/Users/arubalac/AppData/Local/Temp/msohtmlclip1/01/clip_image012.jpg)_

 Suggestion panel for assisting RAML development

## ![](file:///C:/Users/arubalac/AppData/Local/Temp/msohtmlclip1/01/clip_image014.jpg)

 Now let’s start writing the RAML using the API designer

**_Enter the Root_**
First, you'll enter some basic information in a text editor (Remove the default entry displayed in the api.raml file when you open the API designer). You can save your API's RAML definition as a text file with a recommended extension .raml:
```
#%RAML 0.8
title: HelloRAML API
version: 1.0.0
baseUri: http://api.helloraml.com/{version}</font></td></tr></table>
```
Everything you enter in at the [root](https://github.com/raml-org/raml-spec/blob/master/raml-0.8.md#root-section) (or top) of the spec applies to the rest of your API. This is going to come in very handy later as you discover patterns in how you build your API. The baseURI you choose will be used with every call made, so make sure it's as clean and concise as can be.

** _Enter Resources_**

As a thoughtful API designer, it's important to consider how your API consumers will use your API. It's especially important because in many ways, as the API designer YOU control the consumption.

Recalling how your API consumers will use your API, enter the following resources under your root:
```
#%RAML 0.8
title: HelloRAML API
version: 1.0.0
baseUri: http://api.helloraml.com/{version}

/employees:
```
Notice that these resources all begin with a slash (/). In RAML, this is how you indicate a resource. Any methods and parameters nested under these top level resources belong to and act upon that resource. Now, since each of these resources is a collection of individual objects.

Nested resources are useful when you want to call out a particular subset of your resource in order to narrow it. For example:
```
/employees:
   /{employeename}:
```
This lets the API consumer interact with the key resource and its nested resources. For example a GET request to http://api.helloraml.com/employees/apiuser returns details about apiuser. Now, let's think about what we want developers and API consumers to DO.

** _Enter Methods_**

Here's where it starts to get interesting, as you decide what you want the developer to be able to do with the resources you've made available.

Let's quickly review the 4 most common HTTP verbs:

**GET** - Retrieve the information defined in the request URI.

**PUT** - Replace the addressed collection. At the object-level, create or update it.

**POST** - Create a new entry in the collection. This method is generally not used at the object-level.

**DELETE** - Delete the information defined in the request URI.

Now let's focus on building out the /employees resource.
```
#%RAML 0.8
title: HelloRAML API
version: 1.0.0
baseUri: [http://api.helloraml.com/{version}](http://api.helloraml.com/%7bversion%7d)

/employees:
   /{employeename}:
              get:
```
**_Enter Responses_**

Responses MUST be a map of one or more HTTP status codes, and each response may include descriptions, examples, or schemas. Schemas are more fully explained in the Level 200 tutorial.
```
/employees:
   /{employeename}:
              get:
               description: Retrieve a specific employee details
                responses:
                      200:
                       body:
                        application/json:
                            example: |
                                 {
                                  "data": {
                                           "id": "2333",
                                           "Role": "developer",
                                           "DOJ": "01/02/2015",
                                           "datetime": 1341533193,
                                           "Group": "APG",
                                           "Wing": "WST01",
                                           "email": "abc@gmail.com",
                                           "phone": "010101010"
                                          }
                                 }
```
​Congratulations! You've just written your first API definition in RAML

**Final result**
```
#%RAML 0.8
title: HelloRAML API
version: 1.0.0
baseUri: [http://api.helloraml.com/{version}](http://api.helloraml.com/%7bversion%7d) 

/employees:
   /{employeename}:
              get:
               description: Retrieve a specific employee details
                responses:
                      200:
                       body:
                        application/json:
                            example: |
                                 {
                                  "data": {
                                           "id": "2333",
                                           "Role": "developer",
                                           "DOJ": "01/02/2015",
                                           "datetime": 1341533193,
                                           "Group": "APG",
                                           "Wing": "WST01",
                                           "email": "abc@gmail.com",
                                           "phone": "010101010"
                                          }
                                 }
```
**_API console view_**

**![](file:///C:/Users/arubalac/AppData/Local/Temp/msohtmlclip1/01/clip_image016.jpg)**

Click on the resources and see the details populated from RAML to the API console

Congratulation!!!

Now you know how to create a simple RAML based API using API designer. Let’s explore more of RAML capabilities in our next tutorial.

##Reference

[http://raml.org/docs.html](http://raml.org/docs.html)

##Next

 CIP-200 Exploring RAML resource features
