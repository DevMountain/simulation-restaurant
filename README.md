<img src="https://devmounta.in/img/logowhiteblue.png" width="250" align="right">

# Project Summary

This project is designed to replicate what you might receive on the job. There won't be any guided instruction on what you'll need to do. We will only provide you with design specifications and technical requirements. Your mentors have also been asked to provide only minimal guidance. They can point you in the right direction, but cannot help you code. This project is a chance for you to combine and showcase the skills you've learned so far.

With this specification/requirement only structure, we believe this project will showcase what you can do at this point of the program. Because of this, we feel this project will be worth putting in your portfolio.

Good luck and work hard!

# Color Palette & Font

<img src="https://github.com/Be-The-Bert/library-simulation/blob/master/assets/design-guide.png" />

<b><a href="https://fonts.google.com/specimen/Open+Sans?selection.family=Open+Sans">Google Font - Open Sans</a></b>
<br/>
<b><a href="https://fonts.google.com/specimen/Alegreya?selection.family=Alegreya:700i">Google Font - Alegreya</a></b>

### The icons are included in the assets folder of this repository


# Application Design

## Auth View

<img src="https://github.com/Be-The-Bert/library-simulation/blob/master/views/login.png" />

## Browsing View

<img src="https://github.com/Be-The-Bert/library-simulation/blob/master/views/browse.png" />

## Book Details View

<img src="https://github.com/Be-The-Bert/library-simulation/blob/master/views/details.png" />

## Edit Book View

<img src="https://github.com/Be-The-Bert/library-simulation/blob/master/views/edit.png" />

## Add Book View

<img src="https://github.com/Be-The-Bert/library-simulation/blob/master/views/add.png" />

## Cart View

<img src="https://github.com/Be-The-Bert/library-simulation/blob/master/views/cart.png" />

## Bookshelf View

<img src="https://github.com/Be-The-Bert/library-simulation/blob/master/views/shelf.png" />

# Technical Requirements - Front-end

## Auth View

* User can login into their account.
* User can register for an account.
* User should be navigated to the Browsing View on a successful login or successful registration.

## Browsing View

* User can view all products available for purchase/checkout
* User can filter books by genre / availability
* User can reset an applied filter to see a list of all books again
* User can navigate to Book Details View by clicking on the books in the list
* User can navigate to Add Book View
* User can logout and be redirected back to the Auth View

## Book Details View

* User is able to add book to cart from here
* User is able to navigate to Edit Book View 
* User is able to delete a book from the database
  * This should redirect the user back to the Browsing View
* User is able to navigate to previous view
* User should be redirected to the Browsing View after adding the book to the cart

## Edit Book View

* User populates an editable section based on the selected books details to update and change information about book 
* User is able to navigate to previous view, canceling the edit
* User should be redirected to the Browsing View on completion

## Add Book View
* User can add a new book to the library with all the appropriate values
  * Title, Author, Genre, Description, img url, (The book should start in stock by default)
  * User can see a preview of the image
    * The image cannot break out of the preview container if the image is bigger
    * The preview container's size should remain static
* User is able to navigate to previous view, canceling the addition of a new book
* User should be redirected to the Browsing View on completion

## Checkout / Cart View
* User is able to remove an item from cart and cart is updated 
* User can checkout
  * Should add the books in the cart to the user's bookshelf
  * Should clear the cart
  * Should update books from in stock to out of stock
* User should be redirected to the Browsing View on checkout

## Bookshelf View
* User can see list of books currently checked out on their account
* User can return books
  * Should remove the book from the user's shelf
  * Should update the books from out of stock to in stock

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


