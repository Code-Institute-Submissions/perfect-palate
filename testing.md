# Testing

[Main README](/README.md)

Deployed site: [Perfect Palate](https://perfect-palate.herokuapp.com/)

Contents
---------
  * [1. Manual Testing of Features](#1-manual-testing-of-features)
    + [1.1. Features Before Registering](#11-features-before-registering)
    + [1.2. Register account](#12-register-account)
    + [1.3. Login](#13-login)
    + [1.4. Create (CRUD Functionalities)](#14-create--crud-functionalities-)
    + [1.5. Read (CRUD Functionalities)](#15-read--crud-functionalities-)
    + [1.6. Update (CRUD Functionalities)](#16-update--crud-functionalities-)
    + [1.7. Delete (CRUD Functionalities)](#17-delete--crud-functionalities-)
  * [2. Automated Testing](#2-automated-testing)
  * [3. Achievement of User Stories](#3-achievement-of-user-stories)
  * [4. Code Validation](#4-code-validation)
  * [5. Test on Different Browsers](#5-test-on-different-browsers)
  * [6. Test on Different Devices](#6-test-on-different-devices)
  * [7. Bugs and Problems](#7-bugs-and-problems)
    + [7.1 Solved bugs and problems](#71-solved-bugs-and-problems)
    + [7.2 Unsolved bugs and problems](#72-unsolved-bugs-and-problems)
----------

## 1. Manual Testing of Features

The Perfect Palate website was designed to give users the ability to find recipes and share them on their socials. Users that have registered an account, have the privilege of creating, editing and deleting their own recipes whenever they choose. In order to demonstrate the full manual testing of these features, I will create an account, login and then perform the CRUD functionalities.

This manual testing was performed using the Google Chrome web browser.

### 1.1. Features Before Registering

**Click View All Recipes (as Guest):**
On first arrival of the Perfect Palate website, the user will be greeted and referred to as "Guest" on the _View All Recipes_ page. At this point, the user will only be able to find and read recipes via the view buttons:<br>
<img src="static/manual-testing/guest-recipes-page.PNG" alt="all  recipes page for guest" width="50%" height="auto"/>

**Use Search bar:**
Use the search bar to search for keywords, by typing words and then pressing the search button. In this test, "irish porridge jesse" is searched. All recipes containing the keywords "irish", "porridge" and "jesse" in the index as described in section 2.1 will be displayed:<br>
<img src="static/manual-testing/initial-search.PNG" alt="search functionality testing" width="50%" height="auto"/><br>
<img src="static/manual-testing/initial-search-card-reveal.PNG" alt="search functionality testing card reveal" width="50%" height="auto"/>

**Click on the "Fried Plantain" card image:**
Confirm reveal of summary of the recipe:<br>
<img src="static/manual-testing/card-reveal.PNG" alt="testing of recipe card preview or reveal" width="25%" height="auto"/>

### 1.2. Register account

**Click _Register_ on the navigation bar:**
- Confirm that the following page loads correctly:<br>
    <img src="static/manual-testing/register-user.PNG" alt="testing user registration" width="50%" height="auto"/>

**Confirm Successful User Creation:**
- For the purpose of this test, I created an account with username of "tester" as shown in the above image. When successfully registered, the user will be redirected to their profile page:<br>
    <img src="static/manual-testing/initial-tester-profile.PNG" alt="testing the redirection to user's profile" width="50%" height="auto"/>

- Another user cannot create an account with the same email or username that "tester" used:<br>
    <img src="static/manual-testing/username-exists-flash.PNG" alt="username exists flash message" width="50%" height="auto"/><br>
    <img src="static/manual-testing/email-exists-flash.PNG" alt="email exists flash message" width="50%" height="auto"/>

- User will only be able to create account using any of the characters displayed on the label:<br>
    <img src="static/manual-testing/match-correct-format.PNG" alt="username does not match specified format" width="50%" height="auto"/>

### 1.3. Login

- If user inputs either an incorrect username or password, the following flash message will be shown:<br>
    <img src="static/manual-testing/incorrect-username-password-flash.PNG" alt="incorrect username and/or password flash message" width="50%" height="auto"/>

- Similarly with registration, if successfully logged in, user will be redirected to their profile page.

### 1.4. Create (CRUD Functionalities)

- Click _Add New Recipe_ on the navigation bar:<br>
    <img src="static/manual-testing/add-recipe-page.PNG" alt="Add Recipe page" width="50%" height="auto"/>

- Fill in all fields. (The YouTube link is not compulsory and can be left blank). "Tester" will create a new recipe called "Pecan Pie": <br>
    <img src="static/manual-testing/adding-pecan-pie.PNG" alt="Adding Pecan Pie recipe" width="50%" height="auto"/>

- Once submitted, user will received a flash message as follows:<br>
    <img src="static/manual-testing/add-recipe-successful.PNG" alt="Recipe successfully added" width="50%" height="auto"/>

### 1.5. Read (CRUD Functionalities)

- To view all recipes on the website, click _View All Recipes_ on the navigation bar. The menu items have now changed to display options relevant to a registered user namely: _Logout_, _My Profile_ and _Add Recipe_. The page displayed is now as follows:<br>
    <img src="static/manual-testing/tester-recipes-page.PNG" alt="View All Recipes page for registered user" width="50%" height="auto"/>

- "Tester" can view their newly created recipe is now populated on the _View All Recipes_ page as well as on their _Profile_ page.<br>
    <img src="static/manual-testing/tester-recipes-page2.PNG" alt="View All Recipes page for registered user" width="50%" height="auto"/><br>
    <img src="static/manual-testing/tester-new-profile.PNG" alt="Updated Profile page for registered user" width="50%" height="auto"/>

- To view any of the individual recipes, click on the view button of the desired recipe card. For this test, "tester" has chosen to view the recipe for "Fried Plantain":<br>
    <img src="static/manual-testing/full-recipe.PNG" alt="Full Recipe page" width="50%" height="auto"/>

- If user chooses to view their own recipe, there will be an "edit" button available just before the ingredients section. <br>
    <img src="static/manual-testing/pecan-pie-full-recipe.PNG" alt="Own recipe's full page" width="50%" height="auto"/>

### 1.6. Update (CRUD Functionalities)

- Click the "edit" button which can be found on the recipe cards both on the user's creation on their _Profile_ page or on the _View All Recipes_ page or on the full recipe page of the session user's recipe.<br>
    <img src="static/manual-testing/edit-recipe.PNG" alt="Testing for session user to edit recipe" width="50%" height="auto"/>

### 1.7. Delete (CRUD Functionalities)

- If the user decides that they want to delete their recipe, this will be a two-step process for extra authentication. This is to consider the events that they may have clicked the button by mistake or if they are aware of the consequences. If user decides to click "Yes", then the recipe will be permanently removed from the database and subsequently Perfect Palate.<br>
    <img src="static/manual-testing/delete-modal.PNG" alt="Delete Recipe modal" width="50%" height="auto"/><br>
    <img src="static/manual-testing/recipe-successfully-deleted.PNG" alt="Recipe successfully deleted flash message" width="50%" height="auto"/>

## 2. Automated Testing

Pytest was used to run some of Perfect Palate's test functions such as:
1. Identifying the username in lower case in the event that another user tries to create an account with the same spelling but different cases. E.g. "jesSe" vs "Jesse".
2. Ability to convert cooking_time from string into an integer which can be used in any further necessary calculations (e.g. total time).
3. Being able to correctly format the method object that will be stored in the database for easy unpacking of the key-value items of step and method respectively.

The `test_app.py` file is located in the [test folder](https://github.com/jerhabor/perfect-palate/tree/master/test).

## 3. Achievement of User Stories

User Story 1:

>"As a Vegetarian, I would like to be able to see which meals are suitable for me or not."

>"Yes, I can clearly see which meals are vegetarian by the thoughtful seedling symbol with a tooltip to further reinforce it!"


User Story 2:

>"As a food-lover and promoter, I would like to be able to share recipes on my socials!"

> "The share function on the Full Recipe page is amazing!"

User Story 3:

>"As a food newbie, I would like to learn how to cook something decent."

> "Beautifully laid out site with mouthwatering choice of images!"

User Story 4:

>"As a health-conscious male, I would like to be informed of the contents and any possible allergies"

>"Allergies listed accordingly. Very good."

User Story 5:

>"As an epicure, I would like to be able to submit lots of my recipes without constraint, but keep track of how many I have added."

>"Love the counter on My Profile page!"

## 4. Code Validation

All code is valid and the syntax has been verified using the following list of validators:
|               HTML               | CSS                                                | JS / JQuery                    | Python                                                        |
|:--------------------------------:|----------------------------------------------------|--------------------------------|---------------------------------------------------------------|
| [W3C](https://validator.w3.org/) | [Jigsaw W3C](https://jigsaw.w3.org/css-validator/) | [JS Hint](https://jshint.com/) | [Extends Class](https://extendsclass.com/python-tester.html) |

**Screenshot for CSS validation:**<br>
<img src="static/tests/validation/validated_css.PNG" alt="CSS Validated with no errors" width="50%" height="auto"/>

**Screenshot for Python validation:**<br>
<img src="static/tests/validation/validated_python.PNG" alt="Python app code validated with no errors" width="50%" height="auto"/><br>

## 5. Test on Different Browsers

The table below, summarizes the website's versatility and compability across the different type of browsers; which any user could use.

Key: &#x2714; = Website functions as intended

|    Browser (Version)   | Our Cookware | View All Recipes + Full Recipe | Add/Edit Recipe | My Profile |   Login  | Register |
|:----------------------:|:------------:|:------------------------------:|:---------------:|:----------:|:--------:|:--------:|
|       Chrome (80)      |   &#x2714;   |            &#x2714;            |     &#x2714;    |  &#x2714;  | &#x2714; | &#x2714; |
|      Firefox (74)      |   &#x2714;   |            &#x2714;            |     &#x2714;    |  &#x2714;  | &#x2714; | &#x2714; |
|       Safari (13)      |   &#x2714;   |            &#x2714;            |     &#x2714;    |  &#x2714;  | &#x2714; | &#x2714; |
| Internet Explorer (11) |   &#x2714;   |            &#x2714;            |     &#x2714;    |  &#x2714;  | &#x2714; | &#x2714; |
|        Edge (79)       |   &#x2714;   |            &#x2714;            |     &#x2714;    |  &#x2714;  | &#x2714; | &#x2714; |
|       Opera (67)       |   &#x2714;   |            &#x2714;            |     &#x2714;    |  &#x2714;  | &#x2714; | &#x2714; |

## 6. Test on Different Devices

With the help of BrowserStack, Google Chrome devTools and personal devices, the website was able to tested. The list of devices used, are below with their viewport sizes. This ensures good responsive design across all devices.

Key: &#x2714; = Displays as intended

|         Device         | Viewport (Width x Height) | Our Cookware | View All Recipes + Full Recipe | Add/Edit Recipe | My Profile |   Login  | Register |
|:----------------------:|:-------------------------:|:------------:|:------------------------------:|:---------------:|:----------:|:--------:|:--------:|
|         Moto G4        |         360 x 640         |   &#x2714;   |            &#x2714;            |     &#x2714;    |  &#x2714;  | &#x2714; | &#x2714; |
|        Galaxy S5       |         360 x 640         |   &#x2714;   |            &#x2714;            |     &#x2714;    |  &#x2714;  | &#x2714; | &#x2714; |
|        Galaxy S9       |         360 x 740         |   &#x2714;   |            &#x2714;            |     &#x2714;    |  &#x2714;  | &#x2714; | &#x2714; |
|         Pixel 2        |         411 x 731         |   &#x2714;   |            &#x2714;            |     &#x2714;    |  &#x2714;  | &#x2714; | &#x2714; |
|       Pixel 2 XL       |         411 x 823         |   &#x2714;   |            &#x2714;            |     &#x2714;    |  &#x2714;  | &#x2714; | &#x2714; |
|       iPhone 5/SE      |         320 x 568         |   &#x2714;   |            &#x2714;            |     &#x2714;    |  &#x2714;  | &#x2714; | &#x2714; |
|      iPhone 6/7/8      |         375 x 667         |   &#x2714;   |            &#x2714;            |     &#x2714;    |  &#x2714;  | &#x2714; | &#x2714; |
|   iPhone 6/7/8  Plus   |         414 x 736         |   &#x2714;   |            &#x2714;            |     &#x2714;    |  &#x2714;  | &#x2714; | &#x2714; |
|        iPhone X        |         375 x 812         |   &#x2714;   |            &#x2714;            |     &#x2714;    |  &#x2714;  | &#x2714; | &#x2714; |
|          iPad          |         768 x 1024        |   &#x2714;   |            &#x2714;            |     &#x2714;    |  &#x2714;  | &#x2714; | &#x2714; |
|        iPad Pro        |        1024 x 1366        |   &#x2714;   |            &#x2714;            |     &#x2714;    |  &#x2714;  | &#x2714; | &#x2714; |
| Sony Bravia Television |   55-inch diagonal (4K)   |   &#x2714;   |            &#x2714;            |     &#x2714;    |  &#x2714;  | &#x2714; | &#x2714; |

## 7. Bugs and Problems

### 7.1 Solved bugs and problems

- Navigation items were intially unable to have the `.active` class targeted - even after adding `!important`. I was able to target the element by using the `::focus` CSS selector and applying a slightly darker shade of the green.

- The images on the _Our Cookware_ page did not initially render well on mobile view. I then realised that Materialize uses a "push-pull" class to reorder content across the grid structure.

### 7.2 Unsolved bugs and problems

It is likely that the JQuery code for validating the select option input on the forms may not render properly on much older devices. However, I have tested on an iPad, iPhone, Safari, Firefox, Internet Explorer and Google Chrome. It is still worth giving a heads up for the event that the bug arises without me having access to seeing it.