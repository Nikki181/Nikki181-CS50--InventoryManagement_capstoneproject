# Nikki181-CS50--InventoryManagement_capstoneproject
**
• Inventory Management System:**
- The main purpose of inventory management system is to track stocks of different products within the inventory and can order more if the item is low in stock or out of stock. This system is used for keeping inventory operations smooth and efficient in each inventory created by particular user. User can also manage multiple inventories in one place and categorize the items in multiple categories within the inventory.
- In this web application, user can create/edit/delete inventories as well as categories within the inventory and also manage items within individual category.
- User can also download their all-inventories data into excel and get the idea about its item under each category. And apply filters to search particular item, or filter items by its status and category.
	
**
• Why you believe your project satisfies the distinctiveness and complexity requirements, mentioned above.**

- In addition to basic features which are included in previous projects like Responsive web application, Django models utilization, CRUD operations, Exception handling. I have implemented following new features:   
	- view-notification will scan all the inventories of that particular user and fetch all the categories items which are low in stock or out of stock and remind user to refill the stock of that item.
  	- apply filters in the displayed data. User can filter items by its name, category type or item status as well, 
  	- download displayed data in the excel sheets so that user have some idea of all the stock items and its related data with its current status,
	- User can add multiple inventories in just one system and manage all the data in just one place.
	- User can also perform create/Edit/Delete operations on individual items, category within inventory and entire inventory.
	- 
**
• How to run your application.**

1.	Download my code and unzip it.
2.	In the terminal, cd into "inventorymanagement" directory.
3.	Run "python.manage.py makemigrations" to make migrations for the inventorymanagement app.
4.	"python manage.py migrate" to apply migrations to my database.
5.	"python manage.py runserver" to run the application and click on the URL appears in the terminal – you can see the login page of the application.
**
• What’s contained in each file you created.**

- In the distribution code is a Django project called inventorymanagement that contains a single app called inventory.
- urls.py - inventory/urls.py, where the URL Configuration of all the pages for this app is defined.
- views.py - inventory/views.py to see the views that are associated with each of the routes mentioned in the urls.py  
- models.py - Here, I have defined all the models for this web application, where each model represents different columns with which type of data it stores in the database. 
			   Here, I have defined User, Inventory, Category and Item models.

Inside static/inventory/
- table_download.js - File used for downloading the details(Category, Item Name, Manufacturer, Color, Price, Storage Place, Quantity, Min Quantity needed for that product and its status) of all the products with its category inside that inventory.
- style.css - defined the style for each components used in the HTML pages.

Inside template/inventory/
- login.html - (view name - login) The login view renders a login form when a user tries to GET the page. When a user submits the form using the POST request method, the user is authenticated, logged in, and redirected to the index page. 
- logout.html - (view name - logout) The logout view logs the user out and redirects them to the login page. 
- register.html - (view name - register) The register route displays a registration form to the user, and creates a new user when the form is submitted. When user fills the registeration form, one inventory must be generated for that user. So there will always be minimum one inventory per user.
- index.html - (view name - index) After login, it will redirects to index page which is home page of the Inventorymanagement application. Manage (items, category, inventory) and view-notification option will be visible, once user logged in successfully.
				  User can see current inventory, all the category which is present in that particular inventory and also items which are present in that category for that inventory.
				  Also, user can edit category and item from the home page.
  			 	  User can filter display data by its category, by its status and also by its name.
				  User can also download the display data (on the index page) in the excel sheet. 
				  Through manage button on the navigation bar, user can manage item, category and inventories.

- create-category.html - (view name - createcategory) - User can choose inventories which are already created by that user. User can create new category inside selected inventory.
- create-inventory.html - (view name - createinventory) - User can create new inventory.
- create-item.html - (view name - createitem) - User can choose category from the dropdown and add item in selected category.

- edit-category.html - (view name - editcategory) - User can edit category name and description.
- edit-inventory.html - (view name - editinventory) - User can edit inventory name and description here.
- edit-item.html - (view name - edititem) - User can also edit the item details.

- remove-category.html - (view name - removecategory) - User can remove particular category and it will also delete all the associated items.
- remove-inventory.html - (view name - removeinventory) - User can remove inventory only if that user has more than one inventory. And once inventory is removed, all the associated category and items are deleted forever.
- remove-item.html - (view name - removeitem) - User can also remove item.

- select-category.html - (view name - selectcategory) - This page is used to choose category for edit.
- select-inventory.html - (view name - selectinventory) - This page is used to choose inventory for edit.
- select-item.html - (view name - selectitem) - This page is used to choose item for edit.

- view-notification.html - (view name - viewnotification) -  User can see all the products of his inventories if its status is out of stock or less than minimum quantity.
- filters - (view name - applyfilter) - User can filter display data by its category , by its status and also by its name.
