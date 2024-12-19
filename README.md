# CS360-Inventory-Tracker-Android

Developed by Michael Lorenz
Developed for SNHU CS360 - Mobile Architect & Programming course

### Briefly summarize the requirements and goals of the app you developed. What user needs was this app designed to address?

The Inventory Tracker app was developed to address the user needs for an application that can track items in a warehouse. The goals of the app include the ability for users to login in, as well view and store inventory items by adding, removing, and modifying specific items in the inventory. The app also required the ability to notify the user when an item's quantity is reduced to zero.

---
### What screens and features were necessary to support user needs and produce a user-centered UI for the app? How did your UI designs keep users in mind? Why were your designs successful?

User needs were supported by implementing the following screens and features:
- A login screen with components to enter credentials and login or sign up by communicating with the user login table of a database
- A display screen that displays all items stored in an inventory table of a database as a grid. The screen includes components to add or remove items and increase or decrease the quantity.
- An Item edit screen that allows users to input and modify an item's name, description, quantity, and UPC fields with a "Save" button to update the database and a "Delete" button to remove from the database.
- A notification settings screen that allows users to opt-in to SMS inventory alerts, grant SMS permission, and input their phone number, and a feature to automatically send an SMS to users opted in when quantity is reduced to zero.

---
### How did you approach the process of coding your app? What techniques or strategies did you use? How could those techniques or strategies be applied in the future?
Following this process applies to many future software development projects, which I will apply by following an analysis, planning, design, development, and testing cycle and iterating the cycle throughout development. 
1. Identified user needs/goals through guidelines and requirements. Documented types of users, such as business owners and warehouse associates, and their needs.
2. Outlined the screens, components, and features required to support each user's need and the navigation between screens depending on the data flow for the goal.
3. Designed the UI layout of each screen using XML to structure the project.
4. Developed the functionality of each screen thoroughly before moving on to the next screen while testing throughout development.
5. Refined app UI and functionality as needed and identified/resolved defects.

---
### How did you test to ensure your code was functional? Why is this process important, and what did it reveal?

I tested frequently as I added each feature to verify they produced expected results through manual tests of different scenarios/user goals or attempting to find ways to produce unexpected results. Testing many situations helps catch defects early, reducing the complexity/cost of fixing them later and preventing inconveniences or harmful failures. My testing revealed issues like SMS alerts not producing the correct results. In the future, I will implement automated unit and integration tests for increased reliability. 

---
### Consider the full app design and development process from initial planning to finalization. Where did you have to innovate to overcome a challenge?

The process was straightforward overall, though due to the project's scope, I had to innovate my debugging methods to address defects. For example, when SMS alerts would not send when expected, I used the LogCat android feature to log debug messages for SMS inputs like the phone number, SMS permission, and alert setting. I discovered that the phone number wasn't saving to the database properly and that there was a flaw in the SMS alert logic, and I fixed them accordingly. 

---
### In what specific component of your mobile app were you particularly successful in demonstrating your knowledge, skills, and experience?

I was successful in controlling the navigation between screens and programmatically modifying screen components to enhance user experience. For example, I reused the "Item" screen fragment for either adding new items or modifying existing items by passing an itemID argument, allowing the screen to prefill with the item's attributes from the database. I adapted the UI to the user's task, such as changing the "Add New Item" button text to "Save Changes". 

