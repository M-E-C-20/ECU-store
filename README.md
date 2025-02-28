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
 
 ### Design

The following considerations were made when planning the project’s design.

#### Navigation

-   It should be simple and intuitive for a new user to land on the site and navigate it without confucion.
-   All text sould be clear in purpose to a user and positioned to allow a user to understand the site navigation.

#### Visual 

-   Products should contain images to identify to the customer the accuracy of the product.
-   Each image will be appropriately sized and positioned, allowing a user to
    understand their relationship to the products, yet not overwhelm or misuse the available screen space.
-   Text should be clear, appropriately sized and coloured.

#### Physical

-   All features will be available to all screen sizes and devices.
-   Users will be able to access and engage with this project anywhere with an
    internet connection.

#### Time

-   The site is designed to allow quick and easy purchasing of products.
-   A user will be able to log out of website at any point, and log back in on any other device and resume where they left off.

## Skeleton

### Database

This project utilises a Relational Database via PostgreSQL for storing User
Credentials, User Profiles, Products, Categories,  and Contacts. The Database went follwed a similar schema to the Boutique Ado project, as I thought it was a solid and logical place to build an e-commerce site from.

## Surface

This project utilises a
simple colour scheme, designed for a visually soft style.

### Colour Scheme

The primary colour scheme, utilised for the layout, framework, and text of the
website, focuses on a off-white to almost black colour scheme.

![Dark](documentation/screenshots/dark.jpg)

![Light](documentation/screenshots/light.jpg)

The variations of white were implemented in the navbar and backgrounds, and as text on buttons and the footer.

The shades of black were used on buttons, to signal their purpose by contrasting with the white background.

### Typography

The font [Lato](https://fonts.google.com/specimen/Lato) was used across the whole project, as I think it suits the simple and minimalistic purpose o fthe site, and is easily readable.

#### Underlined Links

The navbar within the project produce an underlined effect when hovered (desktop) or pressed (mobile). This helps communicate that the elements
are interactive, and produces appropriate user feedback when a user engages with
these elements.

#### Button Effect 

When a user hovers (desktop) or pressed (mobile) buttons, the colour is changed slightly to indicate this event.

---

# Features

## Existing Features

### General

- Navigation bar on top of each page that consists of:
    - Site logo
    - Search bar
    - Main manvigation menu
    - Menu entries to Login/Register for anonymous users
    - My Account menu entry with a dropdown sub menu for authorized users
    - Shopping bag menu entry with a total amount displayed
- Footer with social links and copyright message.
- Responsive layout that is adapted to desktop and mobile screen sizes.
- Supported by all of the most popular web browsers.
- Instant feedback from the site to the user with the help of pop-up messages when important actions take place.

### Products

- View multiple products on single page.
- View each product on separate page.
- Search box where products can be found by name or description.
- Sort products by price, name and categories, both ascending and descending.
- Filter products by categories.
- Add product to the shopping bag with specified quantity.

### Bag

- View shopping bag.
- Update quantity or Remove product(s) from the shopping bag.
- View checkout page.

### Checkout
- Submit delivery information and payment details on checkout page.
- Complete an order and make a payment.
- View order details on payment completion.
- Receive an email with order details on payment completion.

### Profile
- Update personal delivery information that will be used to prefill checkout form
- View order history
- Logout from the site

### Contact
- Contact store owners.

### Admin
- Execute all the feautures of users mentioned above.
- Add new product(s) to the site.
- Modify or delete existing products on the site.
- View contact forms submitted by users.

### Future features
- Add possibility for authorised users to create a wishlist.
- Add a newsletter signup.
- Add a product testimones page.

---

# Technologies Used

## Development

-   The project was written and tested in
    [gitpod](https://www.gitpod.io/).
-   The project was debugged using Google
    Chrome [Dev
    Tools](https://developer.chrome.com/docs/devtools/).
-   The project uses [GitHub](https://github.com/) for hosting source code and utilising git version control.

## Design

-   The project's wireframes were designed in
    [Balsamiq](https://balsamiq.com/wireframes/).

## HTML/CSS

HTML5 and CSS3 are used throughout this project.

-   The project uses [Bootstrap](https://getbootstrap.com/) 5 as the HTML/CSS Framework..
-   The project uses [FontAwesome](https://fontawesome.com/) v5.15.4, for the site icons.
-   The project uses [Google Fonts](https://fonts.google.com/) for typography.

## Python

This project uses Python version 3.9.6 for back-end infrastructure and data
pre-processing.

A list of the packages dependencies can be found at [requirements.txt](requirements.txt).

## JavaScript

This project uses JavaScript ES6.

-   The project uses [jQuery](https://jquery.com/), a JavaScript library, for
    DOM Traversal, HTML Manipulation, and Event Handling.
-   The project uses the [Stripe.js](https://stripe.com/docs/js) library for
    handling Stripe payment objects.

## Hosting
-   This project is hosted through [Heroku](https://www.heroku.com/).
-   This project’s images are hosted via [AWS S3](https://aws.amazon.com/s3/).

## Database

The project uses [PosteSQL](https://www.postgresql.org/), a relational Database,
for data storage, and this is managed via
[Heroku](https://www.heroku.com/postgres).

## Testing Technologies

-   The project's HTML was validated using [W3C HTML Markup Validator](https://validator.w3.org/).
-   The project's CSS was validated using [W3C Jigsaw CSS Validator](https://jigsaw.w3.org/css-validator/).
-   The project's JS was validated using [JSHint](https://jshint.com/).
-   The project’s Python was validated using [Pylint](https://pylint.org/).
-   The project's accessibility was assessed via Google Chrome's [Lighthouse](https://developers.google.com/web/tools/lighthouse).

---

# Testing

Testing documentation, processes, and outcomes can be found under
[TESTING.md](TESTING.md).

---

# Deployment

## How this project was deployed

This project was deployed to Heroku via the following steps:

### Initial Deployment

-   Navigate to [Heroku](https://www.heroku.com/).
-   [Log in](https://id.heroku.com/login) or [Sign Up](https://signup.heroku.com/) for an account.
    -   If Creating an account, select **Python** as the Primary development
        language.
    -   Activate the account via the confirmation email.
    -   Accept the Terms of Service.
-   Click on **Create new app**.
-   Enter a suitable **App Name** and **Region**.
-   Click **Create App**.
-   Under the **Deploy** tab, under the heading **Deployment Method**, click the
    **GitHub** icon, and proceed to click the button which states **Connect to
    GitHub**.
-   Enter your credentials for **GitHub.**
-   Search for the repository required (in this instance, **ECU-Store**), and click
    **Connect.**

### Automatic Deployment

This project was set up to automatically re-deploy with any changes made to the
Master Branch. The following steps were taken to enable this.

-   Navigate to the **Automatic deploys** section within the **Deploy** tab.
-   Select the **branch** you would like to link to automatic deployment.
    -   As stated above, the ‘master’ branch was chosen for automatic
        deployment.
-   Click **Enable Automatic Deploys**.

### Database Setup Stage 1

-   Within Heroku, navigate to **Resources.**
-   Search for **Heroku Postrgres.**
-   Ensure the plan name is **Hobby Dev – Free**.
-   Click **Submit Order Form.**

### Environment Variables

The following environment variables must be set within your Heroku Server for
the site to deploy and function correctly. Navigate to the **Settings** tab, and
under the heading **Config Vars**, select **Reveal Config Vars,** and add the
following variables:

-   AWS_ACCESS_KEY_ID
-   AWS_SECRET_ACCESS_KEY
    -   These keys can be obtained by creating an [S3
        Bucket](https://aws.amazon.com/s3/) on AWS.
-   DATABASE_URL
    -   This can be obtained by viewing your PostreSQL database within your [Heroku Dashboard](https://dashboard.heroku.com/), and accessing the URI under Settings Database Credentials.
-   DJANGO_SECRET_KEY
    -   A random sequence of characters, required for maintaining session security. One method of obtaining a Secret Key is through [RandomKeygen](https://randomkeygen.com/).
-   DOMAIN_URL
    -   The URL of the hosted project (i.e https://ecu-store.herokuapp.com/)
-   EMAIL_HOST_PASS
        - The app password for designated email account.
-   EMAIL_HOST_USER
    -   The email address and app password for designated email account.
-   STRIPE_PRICE_ID
-   STRIPE_PUBLISHABLE_KEY
-   STRIPE_SECRET_KEY
-   STRIPE_WH_SECRET
    -   Create a [Stripe](https://stripe.com/en-gb) account.
    -   Set up a one-off payment [Stripe
        Product](https://stripe.com/docs/billing/prices-guide), and set the
        resultant ID to the STRIPE_PRICE_ID.
    -   In developer settings, under API Keys, obtain the Publishable and Secret
        Key.
    -   In developer settings, under Webhooks, add an endpoint as:
        -   DOMAIN_URL+premium/webhook
        -   Set the WH_SECRET as the Signing Secret generated as a result.
-   USE_AWS
    -   Set as True.

### Database Setup Stage 2

-   Once the PostreSQL add-on has been set up, environment variables have been
    added and the project has been deployed, open the **Heroku Terminal** and
    execute the following lines of code:

> `heroku run python manage.py migrate`

> `heroku run python manage.py loaddata categories`

> `heroku run python manage.py loaddata products`

-   This will migrate the databases and load the Products.

## Running this project from locally

### Running this project locally

#### Cloning the Repository

1.  Visit the project’s [GitHub Repository](https://github.com/M-E-C-20/ECU-store).
2.  Click the "Code" dropdown box above the repository's file explorer.
3.  Under the "Clone" heading, click the "HTTPS" sub-heading.
4.  Click the clipboard icon, or manually copy the text presented:
    `https://github.com/M-E-C-20/ECU-store.git`
5.  Open your preferred IDE.
6.  Ensure your IDE has support for Git, or has the relevant Git extension.
7.  Open the terminal, and create a directory where you would like the
    Repository to be stored.
8.  Type git clone and paste the previously copied text
    (`https://github.com/M-E-C-20/ECU-store.git`) and press enter.
9.  The Repository will then be cloned to your selected directory.

#### Manually Downloading the Repository

1.  Visit the project’s [GitHub Repository](https://github.com/M-E-C-20/ECU-store).
    -   Ensure you have selected the appropriate branch.
2.  Click the "Code" dropdown box above the repository's file explorer.
3.  Click the "Download ZIP" option; this will download a copy of the selected
    branch's repository as a zip file.
4.  Locate the ZIP file downloaded to your computer, and extract the ZIP to a
    designated folder which you would like the repository to be stored.

#### Opening the Repository

1.  Open your preferred IDE.
2.  Navigate to the chosen directory where the Repository was Cloned/Extracted.
3.  **Optional:** Create a new Python [Virtual
    Environment](https://docs.python.org/3/tutorial/venv.html)
4.  Type `pip install requirements.txt` to install all the required packages.
5.  Type ` python manage.py migrate` in the terminal to migrate the database.
6.  Type `python manage.py loaddata categories` first in the terminal to set up the categories.
7.  Type `python manage.py loaddata products` next in the terminal to set up the products.
8.  You can now be hosting the repository from your IDE.

### Environment Variables

-   When running this project locally, the **Environment Variables** must be set in order for it to function as intended.
-   If using gitpod, this can be done in your workspace settings:
    - EMAIL_HOST_PASS - *variable*
    - EMAIL_HOST_USER - *variable*
    - SECRET_KEY - *variable*
    - STRIPE_PUBLIC_KEY - *variable*
    - STRIPE_SECRET_KEY - *variable*
    - STRIPE_WH_SECRET - *variable*
    - DEVELOPMENT - yes
-   Within this file, declare the environment variables described previously,
    replacing the *variable* with the required variables.
-   Please note that using a local/development environment may use:
    -   `DEVELOPMENT: “Yes”`
-   However, it’s important to note that in Development mode, Email/Key and USE_AWS are not required.

---

# Credits

## Content

-   The Boutique Ado project from Code Institute was used as a base for this project, and much of the code and style of the site is based on it. In particular the products, profile, login/registration and product maangement aspects.

## Media

-   ECU images were taken from shutterstock, courtesy of [Aleksandr Kondratov](https://www.shutterstock.com/g/AleksandrKondratov).
- The background image is a scope image of a faulty diesel injector compared to a good one which I captured myself.

## Code

-   HTML/CSS/JS: Code for Back to Top button was original devised from Code
    Institute’s Boutique Ado project.
-   HTML/CSS/JS: The Bootstrap
    [documentation](https://getbootstrap.com/docs/5.0/getting-started/introduction/)
    was extensively utilised to implement various features of the framework.
-   Python: Code extracts have been taken from Code Institute’s Boutique-Ado project for
    creating many of the app, specifically the bag, checkout, products and profiles apps. Some customisation has been applied to make it suitable for this project.
- Python: The fixed it button was created using this video as a guide: [Create Blog Like Button - Django Blog #18](https://www.youtube.com/watch?v=PXqRPqDjDgc&ab_channel=Codemy.com)
-   Python: The Django [documentation](https://docs.djangoproject.com/en/3.2/)
    was extensively utilised to learn and to implement various features of the framework.

---

# Acknowledgements

-   The concept for this project was devised from my background in the automotive trade, and the Boutique Ado project from Code Institute
-   Thank you to the slack community for their guidance.
-   Thank you to my family for suppoting me in a hugely stressful time for us.

---

# Disclaimer

This website is for educational purposes only; the project is not intended for
profit and therefore the Stripe account will remain in Test mode.
