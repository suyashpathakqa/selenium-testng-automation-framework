# **Automation_Exercise_Project 🧪**

![Automation Testing](https://img.shields.io/badge/Automation-Testing-blue.svg)![Selenium](https://img.shields.io/badge/Selenium-43B02A.svg)![TestNG](https://img.shields.io/badge/TestNG-6.14.3-orange.svg)![Maven](https://img.shields.io/badge/Maven-3.9.6-red.svg)**Welcome to Automation_Exercise_Project, a robust automation testing framework designed to test the Automation Exercise e-commerce platform. Built with Java, Selenium WebDriver, TestNG, and Maven, this project follows the Page Object Model (POM) design pattern for maintainability and scalability. It automates functional testing of key features like user registration, login, product browsing, checkout, and more, with utilities for browser management, JSON data handling, and test execution.**

## **📖 Project Overview**

**This project aims to automate the 26 test cases outlined on the Automation Exercise Test Cases page, covering critical user journeys on the website. The framework is structured to be modular, with separate layers for pages, tests, utilities, and test data, making it easy to expand and maintain. Currently, the project implements Test Case 9 (TC9), with plans to cover all test cases in the future.**

### **Key Components**

- **Page Object Model (POM): Encapsulates web elements and actions in page classes (**`pages/`**), reducing code duplication.**
- **Utility Classes: Includes tools for browser management, JSON data parsing, and Selenium helpers (**`utils/`**).**
- **Test Data Management: Uses JSON files (**`resources/testData/`**) for dynamic test data.**
- **TestNG Framework: Organizes test execution with** `testng.xml`**.**
- **Maven Build: Manages dependencies and test execution.**


---


## **🚀 Features**

- **Modular Design: Separates page logic, test cases, and utilities for better organization.**
- **Dynamic Test Data: JSON-based test data for flexible testing scenarios.**
- **Cross-Browser Support: Configurable browser selection (e.g., Chrome, Firefox) via** `config.properties`**.**
- **Selenium Utilities: Helper methods for common Selenium tasks (e.g., waits, clicks).**
- **Scalable Framework: Easy to add new test cases and pages.**


---


## **📋 Prerequisites**

**Before running the project, ensure you have the following installed:**

- **Java 11+: Required for Selenium and TestNG.**
- **Maven 3.9.6+: For dependency management and test execution.**
- **Google Chrome (v136.0.7103.114): Recommended browser (configurable in** `config.properties`**).**
- **Windows/WSL/Linux/Mac: Tested on Windows 10/11 and WSL (Ubuntu).**


---


## **🛠️ Setup Instructions**

1. **Clone the Repository:**

   ```bash
   git clone https://github.com/MohamedElmezayn/Automation_Exercise_Project.git
   cd Automation_Exercise_Project
   ```

2. **Install Dependencies:**

   - **Ensure Maven is installed:**

     ```bash
     mvn --version
     ```

   - **Run:**

     ```bash
     mvn clean install
     ```

3. **Configure the Browser:**

   - **Open** `src/test/resources/config.properties` **and set the desired browser:**

     ```
     browser=chrome
     url=https://www.automationexercise.com/
     ```

   - **Supported browsers:** `chrome`**,** `firefox`**.**

4. **Run Tests:**

   - **Execute all tests using TestNG:**

     ```bash
     mvn test
     ```

   - **Run a specific test (e.g.,** `TestCase9`**):**

     ```bash
     mvn test -Dtest=TestCase9
     ```


---


## **📂 Project Structure**

```
Automation_Exercise_Project/
├── src/
│   ├── test/
│   │   ├── java/
│   │   │   ├── com/
│   │   │       ├── automationexercise/
│   │   │           ├── pages/          # Page Object Models
│   │   │           │   ├── HomePage.java      # Home page elements and actions
│   │   │           │   ├── LoginPage.java     # Login page elements and actions
│   │   │           │   └── (other page classes)
│   │   │           ├── tests/          # Test cases
│   │   │           │   └── TestCase9.java     # Test Case 9 implementation
│   │   │           ├── utils/          # Utility classes
│   │   │               ├── BrowserManager.java    # Manages browser instances
│   │   │               ├── JSONReader.java        # Reads JSON test data
│   │   │               ├── SeleniumHelper.java    # Selenium utility methods
│   │   │               ├── Util.java              # General utility functions
│   │   │               └── VerifyDownload.java    # Verifies file downloads
│   │   ├── resources/
│   │       ├── testData/                  # Test data in JSON format
│   │       │   ├── AccountDetails.json    # Account-related test data
│   │       │   ├── ExistingUser.json      # Existing user credentials
│   │       │   ├── MadameBrandProducts.json # Product data for Madame brand
│   │       │   ├── PaymentDetails.json    # Payment-related test data
│   │       │   └── PoloBrandProducts.json # Product data for Polo brand
│   │       ├── allure.properties          # Allure report configuration
│   │       ├── config.properties          # Configuration file (browser, URL)
│   │       ├── sample.txt                 # Sample file (placeholder)
│   │       └── testng.xml                 # TestNG suite configuration
├── pom.xml                             # Maven configuration
└── README.md                           # Project documentation
```


---


## **🧪 Test Cases**

**The project aims to automate all 26 test cases listed on the Automation Exercise Test Cases page. Currently, Test Case 9 (TC9) is implemented, with plans to cover the remaining cases. Below is a detailed list of all test cases, including their steps as defined on the website.**

| **Test Case** | **Description** | **Steps** |
| --- | --- | --- |
| **TC1** | **Register User** | **1. Launch browser<strong><br></strong>2. Navigate to** `http://automationexercise.com`**<strong><br></strong>3. Verify home page is visible<strong><br></strong>4. Click 'Signup / Login' button<strong><br></strong>5. Verify 'New User Signup!' is visible<strong><br></strong>6. Enter name and email address<strong><br></strong>7. Click 'Signup' button<strong><br></strong>8. Verify 'ENTER ACCOUNT INFORMATION' is visible<strong><br></strong>9. Fill details: Title, Name, Email, Password, Date of birth<strong><br></strong>10. Select checkboxes for newsletters<strong><br></strong>11. Fill address details: First name, Last name, Company, Address, Country, State, City, Zipcode, Mobile Number<strong><br></strong>12. Click 'Create Account' button<strong><br></strong>13. Verify 'ACCOUNT CREATED!' is visible<strong><br></strong>14. Click 'Continue' button<strong><br></strong>15. Verify 'Logged in as username' is visible<strong><br></strong>16. Click 'Delete Account' button<strong><br></strong>17. Verify 'ACCOUNT DELETED!' is visible** |
| **TC2** | **Login User with correct email and password** | **1. Launch browser<strong><br></strong>2. Navigate to** `http://automationexercise.com`**<strong><br></strong>3. Verify home page is visible<strong><br></strong>4. Click 'Signup / Login' button<strong><br></strong>5. Verify 'Login to your account' is visible<strong><br></strong>6. Enter correct email and password<strong><br></strong>7. Click 'login' button<strong><br></strong>8. Verify 'Logged in as username' is visible<strong><br></strong>9. Click 'Logout' button<strong><br></strong>10. Verify user is navigated to login page** |
| **TC3** | **Login User with incorrect email and password** | **1. Launch browser<strong><br></strong>2. Navigate to** `http://automationexercise.com`**<strong><br></strong>3. Verify home page is visible<strong><br></strong>4. Click 'Signup / Login' button<strong><br></strong>5. Verify 'Login to your account' is visible<strong><br></strong>6. Enter incorrect email and password<strong><br></strong>7. Click 'login' button<strong><br></strong>8. Verify error 'Your email or password is incorrect!' is visible** |
| **TC4** | **Logout User** | **1. Launch browser<strong><br></strong>2. Navigate to** `http://automationexercise.com`**<strong><br></strong>3. Verify home page is visible<strong><br></strong>4. Click 'Signup / Login' button<strong><br></strong>5. Verify 'Login to your account' is visible<strong><br></strong>6. Enter correct email and password<strong><br></strong>7. Click 'login' button<strong><br></strong>8. Verify 'Logged in as username' is visible<strong><br></strong>9. Click 'Logout' button<strong><br></strong>10. Verify user is navigated to login page** |
| **TC5** | **Register User with existing email** | **1. Launch browser<strong><br></strong>2. Navigate to** `http://automationexercise.com`**<strong><br></strong>3. Verify home page is visible<strong><br></strong>4. Click 'Signup / Login' button<strong><br></strong>5. Verify 'New User Signup!' is visible<strong><br></strong>6. Enter name and already registered email address<strong><br></strong>7. Click 'Signup' button<strong><br></strong>8. Verify error 'Email Address already exist!' is visible** |
| **TC6** | **Contact Us Form** | **1. Launch browser<strong><br></strong>2. Navigate to** `http://automationexercise.com`**<strong><br></strong>3. Verify home page is visible<strong><br></strong>4. Click 'Contact Us' button<strong><br></strong>5. Verify 'GET IN TOUCH' is visible<strong><br></strong>6. Enter name, email, subject, and message<strong><br></strong>7. Upload file<strong><br></strong>8. Click 'Submit' button<strong><br></strong>9. Click OK on alert<strong><br></strong>10. Verify success message 'Success! Your details have been submitted successfully.' is visible<strong><br></strong>11. Click 'Home' button and verify home page** |
| **TC7** | **Verify Test Cases Page** | **1. Launch browser<strong><br></strong>2. Navigate to** `http://automationexercise.com`**<strong><br></strong>3. Verify home page is visible<strong><br></strong>4. Click 'Test Cases' button<strong><br></strong>5. Verify user is navigated to test cases page successfully** |
| **TC8** | **Verify All Products and product detail page** | **1. Launch browser<strong><br></strong>2. Navigate to** `http://automationexercise.com`**<strong><br></strong>3. Verify home page is visible<strong><br></strong>4. Click 'Products' button<strong><br></strong>5. Verify user is navigated to ALL PRODUCTS page<strong><br></strong>6. Click 'View Product' of first product<strong><br></strong>7. Verify product detail page with product name, category, price, availability, condition, brand** |
| **TC9** | **Search Product** | **1. Launch browser<strong><br></strong>2. Navigate to** `http://automationexercise.com`**<strong><br></strong>3. Verify home page is visible<strong><br></strong>4. Click 'Products' button<strong><br></strong>5. Verify user is navigated to ALL PRODUCTS page<strong><br></strong>6. Enter product name in search input and click search button<strong><br></strong>7. Verify 'SEARCHED PRODUCTS' is visible<strong><br></strong>8. Verify all products related to search are visible** |
| **TC10** | **Verify Subscription in home page** | **1. Launch browser<strong><br></strong>2. Navigate to** `http://automationexercise.com`**<strong><br></strong>3. Verify home page is visible<strong><br></strong>4. Scroll to subscription form<strong><br></strong>5. Enter email address in input and click arrow button<strong><br></strong>6. Verify success message 'You have been successfully subscribed!' is visible** |
| **TC11** | **Verify Subscription in Cart page** | **1. Launch browser<strong><br></strong>2. Navigate to** `http://automationexercise.com`**<strong><br></strong>3. Verify home page is visible<strong><br></strong>4. Click 'Cart' button<strong><br></strong>5. Scroll to subscription form<strong><br></strong>6. Enter email address in input and click arrow button<strong><br></strong>7. Verify success message 'You have been successfully subscribed!' is visible** |
| **TC12** | **Add Products in Cart** | **1. Launch browser<strong><br></strong>2. Navigate to** `http://automationexercise.com`**<strong><br></strong>3. Verify home page is visible<strong><br></strong>4. Click 'Products' button<strong><br></strong>5. Hover over first product and click 'Add to cart'<strong><br></strong>6. Click 'Continue Shopping' button<strong><br></strong>7. Hover over second product and click 'Add to cart'<strong><br></strong>8. Click 'View Cart' button<strong><br></strong>9. Verify both products are added to Cart<strong><br></strong>10. Verify their prices, quantity, and total price** |
| **TC13** | **Verify Product quantity in Cart** | **1. Launch browser<strong><br></strong>2. Navigate to** `http://automationexercise.com`**<strong><br></strong>3. Verify home page is visible<strong><br></strong>4. Click 'View Product' for any product<strong><br></strong>5. Verify product detail page is opened<strong><br></strong>6. Increase quantity to 4<strong><br></strong>7. Click 'Add to cart' button<strong><br></strong>8. Click 'View Cart' button<strong><br></strong>9. Verify product is displayed in cart with exact quantity** |
| **TC14** | **Place Order: Register while Checkout** | **1. Launch browser<strong><br></strong>2. Navigate to** `http://automationexercise.com`**<strong><br></strong>3. Verify home page is visible<strong><br></strong>4. Add products to cart<strong><br></strong>5. Click 'Cart' button<strong><br></strong>6. Verify Cart page<strong><br></strong>7. Click 'Proceed To Checkout'<strong><br></strong>8. Click 'Register / Login' button<strong><br></strong>9. Fill signup details and create account<strong><br></strong>10. Verify 'Logged in as username'<strong><br></strong>11. Click 'Cart' button<strong><br></strong>12. Click 'Proceed To Checkout'<strong><br></strong>13. Verify Address Details and Review Your Order<strong><br></strong>14. Enter description in comment area and click 'Place Order'<strong><br></strong>15. Enter payment details<strong><br></strong>16. Click 'Pay and Confirm Order'<strong><br></strong>17. Verify success message<strong><br></strong>18. Delete account** |
| **TC15** | **Place Order: Register before Checkout** | **1. Launch browser<strong><br></strong>2. Navigate to** `http://automationexercise.com`**<strong><br></strong>3. Verify home page is visible<strong><br></strong>4. Register user<strong><br></strong>5. Add products to cart<strong><br></strong>6. Click 'Cart' button<strong><br></strong>7. Verify Cart page<strong><br></strong>8. Click 'Proceed To Checkout'<strong><br></strong>9. Verify Address Details and Review Your Order<strong><br></strong>10. Enter description in comment area and click 'Place Order'<strong><br></strong>11. Enter payment details<strong><br></strong>12. Click 'Pay and Confirm Order'<strong><br></strong>13. Verify success message<strong><br></strong>14. Delete account** |
| **TC16** | **Place Order: Login before Checkout** | **1. Launch browser<strong><br></strong>2. Navigate to** `http://automationexercise.com`**<strong><br></strong>3. Verify home page is visible<strong><br></strong>4. Login user<strong><br></strong>5. Add products to cart<strong><br></strong>6. Click 'Cart' button<strong><br></strong>7. Verify Cart page<strong><br></strong>8. Click 'Proceed To Checkout'<strong><br></strong>9. Verify Address Details and Review Your Order<strong><br></strong>10. Enter description in comment area and click 'Place Order'<strong><br></strong>11. Enter payment details<strong><br></strong>12. Click 'Pay and Confirm Order'<strong><br></strong>13. Verify success message** |
| **TC17** | **Remove Products From Cart** | **1. Launch browser<strong><br></strong>2. Navigate to** `http://automationexercise.com`**<strong><br></strong>3. Verify home page is visible<strong><br></strong>4. Add products to cart<strong><br></strong>5. Click 'Cart' button<strong><br></strong>6. Verify Cart page<strong><br></strong>7. Click 'X' button corresponding to product<strong><br></strong>8. Verify product is removed from cart** |
| **TC18** | **View Category Products** | **1. Launch browser<strong><br></strong>2. Navigate to** `http://automationexercise.com`**<strong><br></strong>3. Verify categories are visible on left sidebar<strong><br></strong>4. Click on 'Women' category<strong><br></strong>5. Click on 'Dress' sub-category<strong><br></strong>6. Verify 'WOMEN - DRESS PRODUCTS' is displayed<strong><br></strong>7. Click on 'Men' category<strong><br></strong>8. Click on 'Tshirts' sub-category<strong><br></strong>9. Verify 'MEN - TSHIRTS PRODUCTS' is displayed** |
| **TC19** | **View & Cart Brand Products** | **1. Launch browser<strong><br></strong>2. Navigate to** `http://automationexercise.com`**<strong><br></strong>3. Click 'Products' button<strong><br></strong>4. Verify brands are visible on left sidebar<strong><br></strong>5. Click on 'Polo' brand<strong><br></strong>6. Verify 'BRAND - POLO PRODUCTS' is displayed<strong><br></strong>7. Click on 'Madame' brand<strong><br></strong>8. Verify 'BRAND - MADAME PRODUCTS' is displayed** |
| **TC20** | **Search Products and Verify Cart After Login** | **1. Launch browser<strong><br></strong>2. Navigate to** `http://automationexercise.com`**<strong><br></strong>3. Click 'Products' button<strong><br></strong>4. Verify ALL PRODUCTS page<strong><br></strong>5. Enter product name and click search<strong><br></strong>6. Verify searched products are visible<strong><br></strong>7. Add products to cart<strong><br></strong>8. Click 'Cart' button<strong><br></strong>9. Login user<strong><br></strong>10. Click 'Cart' button<strong><br></strong>11. Verify products are still in cart** |
| **TC21** | **Add review on product** | **1. Launch browser<strong><br></strong>2. Navigate to** `http://automationexercise.com`**<strong><br></strong>3. Click 'Products' button<strong><br></strong>4. Verify ALL PRODUCTS page<strong><br></strong>5. Click 'View Product' of first product<strong><br></strong>6. Verify 'Write Your Review' is visible<strong><br></strong>7. Enter name, email, and review<strong><br></strong>8. Click 'Submit' button<strong><br></strong>9. Verify 'Thank you for your review.'** |
| **TC22** | **Add to cart from Recommended items** | **1. Launch browser<strong><br></strong>2. Navigate to** `http://automationexercise.com`**<strong><br></strong>3. Scroll to 'RECOMMENDED ITEMS'<strong><br></strong>4. Click 'Add to cart' on recommended product<strong><br></strong>5. Click 'View Cart' button<strong><br></strong>6. Verify product is displayed in cart** |
| **TC23** | **Verify address details in checkout page** | **1. Launch browser<strong><br></strong>2. Navigate to** `http://automationexercise.com`**<strong><br></strong>3. Register user<strong><br></strong>4. Add products to cart<strong><br></strong>5. Click 'Cart' button<strong><br></strong>6. Click 'Proceed To Checkout'<strong><br></strong>7. Verify delivery and billing address details match registration** |
| **TC24** | **Download Invoice after purchase order** | **1. Launch browser<strong><br></strong>2. Navigate to** `http://automationexercise.com`**<strong><br></strong>3. Register user<strong><br></strong>4. Add products to cart<strong><br></strong>5. Click 'Cart' button<strong><br></strong>6. Click 'Proceed To Checkout'<strong><br></strong>7. Verify Address Details and Review Your Order<strong><br></strong>8. Enter description in comment area and click 'Place Order'<strong><br></strong>9. Enter payment details<strong><br></strong>10. Click 'Pay and Confirm Order'<strong><br></strong>11. Click 'Download Invoice' button<strong><br></strong>12. Verify invoice is downloaded<strong><br></strong>13. Click 'Continue' button<strong><br></strong>14. Delete account** |
| **TC25** | **Verify Scroll Up using 'Arrow' button and Scroll Down functionality** | **1. Launch browser<strong><br></strong>2. Navigate to** `http://automationexercise.com`**<strong><br></strong>3. Verify home page is visible<strong><br></strong>4. Scroll down to footer<strong><br></strong>5. Verify 'SUBSCRIPTION' text<strong><br></strong>6. Click 'Scroll Up' arrow button<strong><br></strong>7. Verify page scrolls to top and 'Full-Fledged practice website...' is visible** |
| **TC26** | **Verify Scroll Up without 'Arrow' button and Scroll Down functionality** | **1. Launch browser<strong><br></strong>2. Navigate to** `http://automationexercise.com`**<strong><br></strong>3. Verify home page is visible<strong><br></strong>4. Scroll down to footer<strong><br></strong>5. Verify 'SUBSCRIPTION' text<strong><br></strong>6. Scroll up to top<strong><br></strong>7. Verify page scrolls to top and 'Full-Fledged practice website...' is visible** |


---


## **⚙️ Configuration**

- **Browser Setup: Configured via** `config.properties` **(e.g.,** `browser=chrome`**).**
- **Driver Management: Uses WebDriverManager for automatic driver handling.**
- **Test Data: JSON files in** `resources/testData/` **for dynamic inputs (e.g.,** `AccountDetails.json`**,** `PaymentDetails.json`**).**
- **TestNG Suite: Defined in** `testng.xml` **for structured test execution.**

---

## **🛠️ Utilities**

**The** `utils/` **directory provides essential tools for test automation:**

- **BrowserManager.java: Initializes and manages browser instances (e.g., Chrome, Firefox).**
- **JSONReader.java: Parses JSON test data files for dynamic inputs.**
- **SeleniumHelper.java: Offers reusable Selenium methods (e.g., waits, element interactions).**
- **Util.java: General utility functions (e.g., string manipulation, random data generation).**
- **VerifyDownload.java: Verifies successful file downloads during tests (e.g., invoice downloads).**


---


## **💡 Future Improvements**

- **Integrate logging (e.g., Log4j) for detailed debugging.**
- **Add Allure or ExtentReports for enhanced test reporting.**
- **Implement remaining test cases (TC1–TC8, TC10–TC26).**
- **Add CI/CD integration with GitHub Actions for automated testing.**

---

## **📞 Contact**

**For questions or contributions, reach out to Mohamed Elmezayn through LinkedIn: https://www.linkedin.com/in/mohamedelmezayn88/ .**

---

**⭐⭐⭐ If you find this project helpful, please give it a star on GitHub. ⭐⭐⭐*

***Last updated: May 31, 2025, 04:12 PM EEST***
