---
type: ProjectLayout
title: FINAL Project
colors: colors-a
date: '2024-12-12'
client: Durham College
description: >-
  This is the big final project for the course and was used for us to display
  all our knowledge. My group decided to make a bakery app 
media:
  type: ImageBlock
  url: /images/proj_1.png
  altText: Project image 1
featuredImage:
  type: ImageBlock
  url: /images/proj_1.png
  altText: proj_1
  caption: Caption of the image
  elementId: ''
---
Project

Flutter Bakery App

Group 1:

Adam LeBlanc - 100818716

Anh Thu Huynh - 100881942

Shah Bano – 100886157

INFT-3101-01

Mobile Development

Friday December 6<sup>th</sup>, 2024

# Project Details

## App name and description

Our app is called sunset bakery.

This bakery app is for placing an order or simply viewing our menu before coming in!

Teams roles and responsibilities:

*Project Manager* – Shah Bano

*UI/UX  Designer* – Anh thu Huynh

*Backend/Functionality Designer* – Adam LeBlanc

## App Deliverables

### Home Page

The home page features the different categories our bakery offers: cakes, cupcakes, donuts, and drinks. Additionally, the header includes a dynamic welcome message. When a user logs in, their first name is displayed next to the phrase "Good Day, \*\*\*."

These categories and all menu options are populated using a JSON file that also includes placeholders for our images. The JSON file contains information such as the category group, image, description, price, item name, and allergy ingredients to assist with filtering.

### Settings Page

Our settings page includes weekly promotions, an allergy filtering system that links to a separate page, font size adjustments, and a help center.

The weekly promotions are limited to in-store offers only.

The allergy filtering system, also linked in our main navigation bar, filters items based on ingredients. This functionality uses our menu.json file, which includes a field called "contains" that lists the key ingredients some users may be allergic to.

It includes:

*   Eggs
*   Milk
*   Walnuts
*   Almond Milk
*   Coconut Oil
*   Oat Milk
*   Wheat
*   Optional Nuts

When a user selects any setting to avoid a specific ingredient, the app displays the safe food items available at the bakery. It also integrates with the food details page, which includes an option to add items to the cart. The food details page lists additional ingredients that may be present. This can make it easier to order the filtered items rather than the customer going back to each category browsing page to look for it.

Additionally, we have included some vegan options that exclude eggs and milk to ensure accessibility for more users.

The help center features a FAQ section and our privacy policy statement.

The font size setting includes a toggle for either normal or larger font sizes, ensuring accessibility across the app. **This feature has not been successfully implemented.**

### Three core functional pages

#### Ordering page

Users can browse the menu and view details of food items, including the description, ingredients, price, image, and an "Add to Cart" button.

This data is accessed through our JSON file. There is also a toggle to adjust the quantity, allowing users to increment or decrement it within a set limit of 1 to 10.

Once an item is added to the cart, a widget pops up asking if the user would like to proceed to checkout. If they wish to continue ordering, they can simply keep browsing.

#### Checkout page

The checkout page displays all items added to the user’s cart, with the ability to adjust quantities or remove items. The total price is calculated, including a subtotal for each item, a 13% tax, and a total price display. There is also handling for the empty cart state. The cart persists across sessions.

The user then clicks "Proceed to Checkout," where they can choose whether they would like to pay in-store or by card. Each option has its own widget: for in-store payment, the widget simply advises the user to pay at the store; for card payment, a form is provided for online payment. Alternatively, the user can choose to inform the bakery that they will pay by card but complete the payment in-store.

After selecting a payment method, the user clicks "Place Order," which takes them to a separate page displaying their order number, a thank-you message, and instructions on how to pick up their order.

#### Log in page

Our login page is connected to a JSON file containing existing user data, including their email, password, and first and last name.

Additionally, to place an order, the user must be logged in. If they are not already logged in, they will be redirected to the login page during checkout. Once login is successful, they can return to their cart and continue the checkout process.

## App Drawbacks

Initially, we wanted to integrate Firebase, but across our different branches, it worked in one but failed when merged. We aimed to allow users to log in using Google accounts, but that wasn’t working, so we decided to use a JSON file due to time constraints. The data inside is mock data, but in future projects, we could implement databases with encrypted passwords. And also use databases for our menu.

Due to the aesthetic of our app being pre-set, we didn’t realize that integrating dark mode would be much more difficult with a custom theme. We were unable to implement dark mode because the design for our front end was predetermined, and we would have run out of time if we replaced all the colors with the built-in themes in Flutter.

Another feature we would have liked to implement is real-time updates. We wanted the estimated pickup times for orders to vary depending on their size. However, we decided to settle on a 10-minute wait and advised customers in our FAQ to place their orders with that time in mind. This could have been implemented by setting price limits, where the higher the price, the longer the order would take. In the final order confirmation page, we could have displayed a real-time countdown or used a "received," "preparing," or "ready" widget, similar to those found in most food ordering apps.

Lastly, we tried to integrate a font size adjuster, however due to timing issues, we were unable to fully implement this feature. This feature could make our app more accessible.

# Screenshots & Testing

**Home Page:**

The nav bar which takes us to the home page, allergy filter, cart, login page and settings.

The categories load their respective browsing page once clicked.

A welcome message, which dynamically changes according to who is logged in. In this example, the customer’s first name is Cus.

**Browsing pages:**

****![](/images/browsing_1.png)

Each item has their image, name and a more details page.

**Browsing pages (Cakes):**

****![](/images/browsing_2.png)

Each item has their image, name and a more details page.

**Browsing pages (Donut) :**

****![](/images/browsing_3.png)

Each item has their image, name and a more details page.

**Browsing pages (Drinks) :**

****![](/images/browsing_5.png)

Each item has their image, name and a more details page.

**Detail page for items:**

****![](/images/detail_page.png)

Add to cart button

The price of each item, with a quantity portion to increment amount of item, which changes price along with it

Contains field to help with allergy filtering

Item description dynamically loaded using our json file

Item title dynamically loaded using our json file

Item image dynamically loaded using our json file

**Cart page:**

****![](/images/cart_page.png)

A proceed to checkout button for payment methods

Calculating the subtotal, showing the amount of tax to be applied and the grand total

Each item in cart is featured with its image, name, price which is dependent on the quantity, an increment/decrement bar and a delete from cart button

**Checkout payment page:**

****![](/images/checkout_page.png)

Place order button to finish off the ordering process

Card form to be filled out if user wants to pay by card

Customer can pick to either pay by card, or pay in store using the pick up in store option

**Order confirmation page:**

****![](/images/ordercon_page.png)

Thank you message and pick up instructions

Order number

Back to home button

**Log in:**

****![](/images/login_page.png)

Log in form with email and password input bars

Login button

**Login page with user logged in:**

****![](/images/login_page_2.png)

Customers details are loaded into the my account page, their full name and email

Logout button

**Settings page:**

****![](/images/setting_page.png)

An FAQ button, special offers button and allergies button

A font size adjuster

**FAQ (and privacy policy):**

****![](/images/faq_pag.png)

Privacy policy for the app generated using AI

Dropdown FAQ questions with answers

**Special offers page:**

****![](/images/special_offers.png)

Showing weekly offers that can be redeemed through showing them in-store

**Allergies page (Default):**

****![](/images/allergies.png)

The filtered items that avoid selected ingredients are loaded here. Once clicked on, it will lead you to the details page to add to cart directly

User can pick which ingredients they would like to avoid, by default none are selected. You can multi-select ingredients

**Allergies page (Avoiding eggs):**

****![](/images/allergie_2.png)

Items not including eggs are displayed. Once clicked on, it leads you to the details page where you can place it in your cart directly

User selected to avoid eggs

# Reflections

## Adam LeBlanc

As the backend developer my job was to ensure that the backend functioned as we desired. Initially we were working in separate branches, one for the front end and one for the back end. Then once we combined the two branches, I made sure that the two integrated correctly. I did this by testing the functionality of each page to ensure that it worked as intended. In addition to this I helped design and implement the order confirmation page. At first, we wanted to have this display the items that you ordered as well, but we had some difficulties getting that to work. So, with the time constraint in mind we decide to leave that part out and just include the order number and some pick-up instructions to keep it simple. I also worked on the setting page; this page had several components. There was a text size scroll bar as well as links to an FAQ page and a special offers page. These pages were also designed by me, the last thing on this page is another link to the allergies page. One thing that was challenging was getting the text size to work across all the pages. Unfortunately, I couldn’t get it to fully work, this is something that I would want to add for a final version if there was more time. Another challenge that also provided a great learning experience was working on a large project as a group. We have had some assignments like this in the past, but this was a first for a mobile app. The importance of everyone being on the same page and knowing their role is very important. As well as the version control and using GitHub to our advantage. As I mentioned earlier we do have some experience with these types of projects, but they are still something that is new and can be an intimidating task.

## Anh Thu Huynh

As the UI/UX designer for our bakery app, I translated Figma designs into a cohesive and functional interface, focusing on creating a seamless user experience. My work included developing key features such as the home page, menu, allergy filter, cart, transaction flow, and login screens. I implemented auth\_state to manage user authentication, ensuring a smooth login experience, and utilized the Provider state management system to enhance the functionality of the add-to-cart feature. One of the main challenges was aligning design consistency with dynamic functionality, especially in handling real-time user interactions. This project strengthened my skills in front-end development, state management, and designing user-centric applications, deepening my expertise in creating intuitive and engaging digital experiences.

## Shah Bano

This project was very enjoyable. My teammates were collaborative and knowledgeable. I thought a bakery app would be specific enough and have good potential for many functional pages, as well as integrating data fetching and displaying. Initially, we had many ideas for features to include in our final app. However, when we started the project, we realized that we would need to adjust many of them. Each week, we made small changes. I ensured we didn't add too many major changes that could result in incomplete or non-functional code while also considering suggestions from my group members. For our functional pages, especially, it was a bit challenging to decide between a "favourites" page and a "login" page. However, we realized that a "favourites" page would require a login, so we decided to use the login page. Our biggest challenge was deciding which main features to prioritize for the app. To manage this, I created a priority list, which included mandatory features to complete, and anything additional could be considered later if time allowed. There were a lot of great ideas from my team, but we understood that, with the time available, we needed to ensure that the requirements were met.

I made sure we communicated via Microsoft Teams, as meeting in person was difficult on days we didn't have class. Additionally, Anh set up a GitHub repository, which kept track of updates and made the code accessible to everyone. I also ensured that app testing was ongoing with each page integration. Any concerns were naturally brought up, and Anh and Adam did a great job communicating those.
