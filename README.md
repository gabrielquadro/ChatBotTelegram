# ChatBotTelegram
ChatBot system on telegram for serving a restaurant or snack shop developed in Java.

![image](https://user-images.githubusercontent.com/61526044/189543045-43122394-739c-41da-b434-104e79a2e696.png)

![image](https://user-images.githubusercontent.com/61526044/189543073-381877a2-5095-47a5-ab69-5e2c24823ad1.png)

![image](https://user-images.githubusercontent.com/61526044/189543087-69767937-0d31-433d-8a51-e4b49519cabc.png)

![image](https://user-images.githubusercontent.com/61526044/189543104-292c5b48-00ae-46cf-a69d-6216a08025a4.png)


The customer's interaction with the Bot occurs as follows:
1. Client sends any message;
2. Bot inserts the record into the customer table (if there is no such id yet) and responds
with a standard greeting asking the customer which category of snacks they
would like to look (listing the options);
3. Assuming that the customer chooses to see category 3 – pizzas;
4. The Bot responds with the list of products in this category (code, description and
price);
5. Assuming that the customer chooses option 2 – Average Pizza;
6. The Bot asks the amount;
7. Assuming the customer answers 1;
8. The Bot asks if you have any observations;
9. Assuming that the customer answers “With cheddar edge”;
10. Bot enters the order body and order item and then asks if the
customer wants to add some more product to the order;
11. If the customer answers yes, display the categories again and repeat the steps to
from 3;
12. If the customer answers no, then it updates the order as finished=1 and returns
a message thanking you for your order and informing you that you can pick it up in 40
minutes.

- Category Maintenance: allow including, changing and deleting categories of
snacks (you can only delete if there is no linked product yet);
- Product Maintenance (snacks): allow including, changing and deleting
products (you can only delete it if it is not already in an order).
- Order inquiry: The system displays a screen in
master-detail. In the first table display all orders that were completed by the
customer, but have not yet been delivered. In the second table list the order items
selected. When clicking on the “Update Screen” button, the query in the DB must be redone. O
“Finish Delivery” button must update the field delivered=1 for the order
selected and reload the screen (so that the order leaves the screen).

Bot configuration:
You need to open Telegram, locate the profile
“BotFather” and send the command /newbot. Then you need to specify a name, such as
example “LancheriaMilliway” and a username (which ends with the word bot, for
example “Lancheria Milliwaybot”). Finally, you will receive a token to use in your
Java program which accesses the Bot via API and responds to user requests. The documentation
API usage is available at https://core.telegram.org/api.

Database:

![image](https://user-images.githubusercontent.com/61526044/189542660-04be51f7-edbf-4640-836c-9464487e7714.png)
