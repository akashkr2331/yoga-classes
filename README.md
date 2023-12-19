#Payment for Yoga Classes Project

![photo_2023-12-19_23-46-35](https://github.com/akashkr2331/yoga-classes/assets/84612937/e18ad13c-1376-4f92-898f-2ee42be0befc)


Firstly,in the backend we create mongoose schema for user database. 
It stores data of a user with unique Mobile Number throughout the year.
user Schema contain its name, date of birth, mobile number, slot for current month and status of payment for current month. Unique id is generated automatically by mongoDb database.
Two users can't have same mobile number. A user can use a unique Mobile Number for a particular month.

In frontend, form is made with validation for name (not be empty), phone number (of 10 digits), date of birth, Through date of birth, we process whether the user can be permitted to join or not.
if they fulfill the condition then the user data is sent to server and it checks in database whether he have paid for this month or not.. if the user with the given mobile number has paid then they proceed to payment section.
else they are sent to payment gateway.
In payment gateeway, stripe api is used to check card validity. If the card is valid, then the dat is sent to backend and in bacjkend it uses another stripe api to process the payment. 

