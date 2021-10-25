# **ECU Store**: Code Institute MS4 Project

This project is a Full Stack e-commerce website using the Django web framework. Users can create a purchase without signing up, or can register and save their details to a personal profile and mark products as having fixed their vehicle.

View the deployed site: [ECU Store](https://ecu-store.herokuapp.com/).

# Table of contents

> 1.  [Overview](#overview)
> 2.  [UX](#ux)
>     1.  [Strategy](#strategy)
>     2.  [Scope](#scope)
>     3.  [Structure](#structure)
>     4.  [Skeleton](#skeleton)
>     5.  [Surface](#surface)
> 3.  [Features](#features)
>     1.  [Existing Features](#existing-features)
>     2.  [Future Feature Considerations](#future-feature-considerations)
> 4.  [Technologies Used](#technologies-used)
> 5.  [Testing](#testing)
> 6.  [Deployment](#deployment)
> 7.  [Credits](#credits)
>     1.  [Readme](#readme)
>     2.  [Content](#content)
>     3.  [Media](#media)
>     4.  [Code](#code)
> 8.  [Acknowledgements](#acknowledgements)
> 9.  [Disclaimer](#disclaimer)


# Overview

**ECU Store** is a full stack e-commerce store, which allows users to purchase automotive ECU's for specific vehicles. Unregistered users can purchase without needing to register, registered users can mark an item as "Fixed It!", which lets other users know that the product repaired their vehicle. The store is designed to be easy to navigate andintuitive for the user.

The project was developed using **Python** (Django), **HTML**, **CSS**, **JavaScript**, and utilises an SQL database via **PostreSQL**.

---

# UX

## Strategy

### User Stories  

| User Story ID                      | As A/An        | I want to be able to                                                                | So that I can                                                                                         |
|------------------------------------|----------------|-------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| **Viewing and Navigation**         |                |                                                                                     |                                                                                                       |
| 1                                 | Site User      | View a list of products                                      | Select some to purchase                                                             |
| 2                                 | Site User      | View individual product details                      | Identify the price, description, product rating, product image and availability                                                                          |
| 3                                 | Site User      | View how products worked for other users                                                 | Feel confident that the products are effective                                                                               |
| 4                                 | Site User      | Easily view the total of my purchases at any time                                                | Avoid overspending                                                                               |
| 5                                 | Site User      | Contact the store                                                | Make queries about a product, deliveries or to see if an item can be repaired                                                                               |
| **Registration and User Accounts** |                |                                                                                     |                                                                                                       |
| 6                                 | Site User      | Easily register for an account                                                             | Have a personal account and view my profile                                                                                       |
| 7                                 | Site User      | Log In and logout                                                                   | Access my personal account information                                                                 |
| 8                                 | Site User      | Recover my password                                                                 | Recover access to my account.                                                                         |
| 9                                 | Site User | Receive an email confirmation after registering                                                                   | Verify my account registration was successful                                                                         |                                                                                                      |
| 10                                | Site User      | Have a personalised user profile                                              | View my order history and order confirmations, and save my payment information                                               |
| **Sorting and searching**                           |                |                                                                                     |                                                                                                       |
| 11                                 | Site User      | Sort the list of available products                                                       | Easily identify the best rated, best priced and categorically sorted products                                                      |
| 12                                 | Site User | Sort a specific category of product                                                              | Find the best priced or best rated product in a specific category, or sort the products in that category by name                                                                               |
| 13                                 | Site User | Sort multiple categories of products simultaneously                                                        | Find the best priced or best rated products across broad categories                                                            |
| 14                                 | Site User | Search for a product by name or description                                                               | Find a specific product I'd like to purchase                                                                            |
| 15                                 | Site User | Easily see what I've searched for and the number of results                           | Quickly decide whether the product I want is available                                                                              |                                                                |
| **Purchasing and checkout**                    |                |                                                                                     |                                                                                                       |
| 16                                 | Site User      | Easily select the quantity of a product when purchasing it                                                                | Ensure I don't accidentally select the wrong product or quantity                                                                |
| 16                                 | Site User      | View items in my bag to be purchased                                                 | Identify the total cost of my purchase and all items I will receive                                                               |
| 18                                 | Site User      | Adjust the quantity of individual items in my bag                                                     | Easily make changes to my purchase before checkout                                                                      |
| 19                                 | Site User      | Easily enter payment information                                                  | Check out quickly and with no hassle |
| 20                                 | Site User      | Feel my personal and payment information is secure                                                  | Confidently provide the needed information to make a purchase |
| 21                                 | Site User      | View an order confirmation after checkout                                                  | Verify that I haven't made any mistakes |
| 22                                 | Site User      | Receive an email confirmation after checking out                                                  | Keep confirmation of what I've purchased for my records |
| **Admin and store management**                          |                |                                                                                     |                                                                                                       |
| 23                                 | Store owner      | Add a product                                                                      | Add new items to my store                                                                |
| 24                                 | Store owner      | Edit/update a product                                                           | Change product prices, descriptions, images and other product criteria         |
| 25                                 | Store owner          | Delete a product                                                            | Remove items that are no longer for sale                                                                              |
| 26                                 | Store owner          | View site user messages                                                         | Resond to their queries                                                                           |

## Scope

### Functional Requirements

#### Simple and Intuitive Interface

-   Users must be able to navigate, and interact with, the site with ease.
-   Ensure site is responsive to all device sizes.

#### User Management

-   Allow users to create an account, confirm their email address, change their
    password, log in, and log out.

#### Profile

-   Allow users to visit their profile.
-   Allow users to see their order history.
-   Allow users to edit their profile details and edit it if desired.

#### Products

-   Allow users to easily view available products.
-   Allow users to se what vehicles each product is available for.
-   Allow users to view if the product has helped other users.

#### Contact

-   Allow users to reach out to the store owners for product related queries.
-   Have a predefined structure to make it easier for the user to define their issue, and for the store owner to interpret.

#### Admin Tools

-   Allow the store owner to add new products to the database.
-   Allow the store owner to edit or delete existing products from the database.
-   Allow the store owner to view contact requests from site users, and to delete messages if necessary.

## Structure

### Informational Architecture

In order to create a simple interface for the user, each of the project’s core
functions will be isolated into different pages. In an attempt to implement an
intuitive navigation system, a persistent Navbar (Navbar) will be utilised. This will allow a user to navigate the
project with ease, spending minimal time finding attempting to make a purchase, which should help retain users.

#### Navbar

The Navbar will be present across the site and allow users to navigate across the site with ease.

<details>
  <summary>Show Details</summary>

>Applicable User Stories:
>-   1, 4, 6, 7, 14, 17, 18, 23, 26
>
>Applicable Functional Requirements:
>-   Simple, Intuitive, and Engaging Interface
>-   View Products
>-   View Profile
>-   Contact
>-   Register
>-   Login/Logout
>
>Navigational Routes:
>-   All logical pages.
  
</details>  
  

#### Home 

The home page is the initial landing page, and provides a brief overview of the
project’s concept and the appropriate CTAs.

<details>
  <summary>Show Details</summary>

>Applicable User Stories:
>-   1, 6, 7
>
>Applicable Functional Requirements:
>-   Direct users to view products.
>-   Prompt to register
>-   Prompt to login
>
>Navigational Routes:
>-   Products
>-   Log In (Logged Out)
>-   Register (Logged Out)

</details>  
  

#### Account Management

Account Management will allow users to register, create an account, log in, log
out,and reset their password.

<details>
  <summary>Show Details</summary>

>Applicable User Stories:
>-   6, 7, 8, 9, 10
>
>Applicable Functional Requirements:
>-   User Management
>
>Navigational Routes:
>-   Account verification
>-   Login Redirect

</details>  
  

#### Contact 

The will allow users to direct queries to the store manager.

<details>
  <summary>Show Details</summary>

>Applicable User Stories:
>-   5, 26
>
>Applicable Functional Requirements:
>-   Contact store owners.
>-   Predetermined subjects help both the owner and the user to narrow down the query.
>-   Contact admin will allow the store owner to view user messages.
>
>Navigational Routes:
>-   N/A

</details>  
  

#### Products

The products page will allow all users to view all products available in the store. From there the user can filter on category, price, manufacturer or ECU. Users can select products to view further information on them and decide to add to bag if a site user, or edit/delete items if a store owner.

<details>
  <summary>Show Details</summary>

>Applicable User Stories:
>-   1, 2, 3, 11, 12, 24, 25
>
>Applicable Functional Requirements:
>-   Simple, Intuitive, and Engaging Interface
>-   View products.
>-   Sort products.
>-   Add to bag.
>-   Edit/delete products.
>
>Navigational Routes:
>-   Bag
>-   Edit/delete products (Admin)

</details>  
  

#### Profile

The profile will allow users to see their account details and order history. A user can update their account details to enable faster checkout.

<details>
  <summary>Show Details</summary>

>Applicable User Stories:
>-   10, 19, 21
>
>Applicable Functional Requirements:
>-   Simple, Intuitive, and Engaging Interface
>-   User Management
>-   View order history
>
>Navigational Routes:
>-   N/A 

</details>  
  

#### Admin Tools

The admin tools page will allow the store owner to add products and to view messages from site users.

<details>
  <summary>Show Details</summary>

>Applicable User Stories:
>-   23, 26
>
>Applicable Functional Requirements:
>-   Simple and Intuitive Interface
>-   Add new products
>-   View messages
>
>Navigational Routes:
>-   N/A

</details>  
 