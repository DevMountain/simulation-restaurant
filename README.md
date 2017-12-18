<img src="https://devmounta.in/img/logowhiteblue.png" width="250" align="right">

# Project Summary

This project is designed to replicate what you might receive on the job. There won't be any guided instruction on what you'll need to do. We will only provide you with design specifications and technical requirements. Your mentors have also been asked to provide only minimal guidance. They can point you in the right direction, but cannot help you code. This project is a chance for you to combine and showcase the skills you've learned so far.

With this specification/requirement only structure, we believe this project will showcase what you can do at this point of the program. Because of this, we feel this project will be worth putting in your portfolio.

Good luck and work hard!

# Color Palette & Font

<img src="https://github.com/bethtelford/restaurant-simulation/blob/master/assets/design-guide.png" />

<b><a href="https://fonts.google.com/specimen/Open+Sans+Condensed?selection.family=Open+Sans+Condensed:300">Google Font - Open Sans</a></b>
<br/>
<b><a href="https://fonts.google.com/specimen/Pacifico?selection.family=Pacifico">Google Font - Alegreya</a></b>

### The icons and images are included in the assets folder of this repository


# Application Design

## Auth View

<img src="https://github.com/bethtelford/restaurant-simulation/blob/master/views/login.png" />

## Browsing View

<img src="https://github.com/bethtelford/restaurant-simulation/blob/master/views/browse.png" />

## Details View

<img src="https://github.com/bethtelford/restaurant-simulation/blob/master/views/details.png" />

## Edit View

<img src="https://github.com/bethtelford/restaurant-simulation/blob/master/views/edit.png" />

## Add Item View

<img src="https://github.com/bethtelford/restaurant-simulation/blob/master/views/add.png" />

## Cart View

<img src="https://github.com/bethtelford/restaurant-simulation/blob/master/views/cart.png" />

# Technical Requirements - Front-end

## Auth View

* User can login into their account.
* User can register for an account.
* User should be navigated to the Browsing View on a successful login or successful registration.

## Browsing View

* User can view all items available for purchase
* User can filter books by meal
* User can reset an applied filter to see a list of all items again
* User can navigate to Item Details View by clicking on the items in the list
* User can navigate to Add Item View
* User can logout and be redirected back to the Auth View

## Details View

* User is able to add item to cart from here
* User is able to navigate to Edit Item View 
* User is able to delete a item from the database
  * This should redirect the user back to the Browsing View
* User is able to navigate to previous view
* User should be redirected to the Browsing View after adding the item to the cart

## Edit View

* User populates an editable section based on the selected item's details to update and change information about the item 
* User is able to navigate to previous view, canceling the edit
* User should be redirected to the Browsing View on completion

## Add View
* User can add a new item to the menu with all the appropriate values
  * Name, Price, and Description
* User is able to navigate to previous view, canceling the addition of a new item
* User should be redirected to the Browsing View on completion

## Cart View
* User is able to remove an item from cart and cart is updated 
* User can checkout
  * Thi should clear the cart
* User should be redirected to the Browsing View on checkout

# Technical Requirements - Back-end
* The back-end should be created using express.
* Massive will be used to establish a connection to your database and manipulate/retrieve data with SQL files
* Student will create tables using the supplied data

## Endpoints

### Authorization Endpoints

* POST - /api/auth/login - Sets the user information on the session.
  * On success return a status of 200 and the user object.
  * A user object should have the following properties:
    * id - This is the UserId you are using for your database.
    * username - This is the username associated with the UserId.
  * The database should store the password, but you should not send this information to the front end as part of the user object
  * On failure return a status of 500.
* POST - /api/auth/register - Registers a user to the database. Sets the user information on the session.
  * On success return a status of 200 and the user object.
  * A user object should have the following properties:
    * id - This is the UserId you are using for your database.
    * username - This is the username associated with the UserId.
  * The database should store the password, but you should not send this information to the front end as part of the user object
  * On failure return a status of 500.
* POST - /api/auth/logout - Destroys the session. Sends a status of 200.

#### NOTE: This is in no way a secure or effective way of storing user credentials. This is required for you to demonstrate your knowledge of data transfer and correspondence between the user and your server using sessions. Do not ever rely on this method in anything bound for production.


