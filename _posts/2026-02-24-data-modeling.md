---
layout: post
title: Data Modeling
author: Chris Bell
---

Write a post on your Jekyll Github blog that discusses the assumptions you made to convert your scenario into this data modeling framework, and the User Stories you wrote along with their sizes and connections.

Include with your post a discussion of the PNG exports of your LucidChart ER diagram and Redgate schema. Are you satisfied with your resulting data representation? What are some complications that you could encounter implementing this model?

## User Stories

1. As an owner, I can list items for sale so that items can be sold to customers and for the company to make a profit.
   - Size: 7 – must consider getting all items up onto the website, get the entire customer side of things set up, like getting them logged in, collecting their information, processing the orders, etc.

2. As a customer, I can order pickup or delivery so that I can get food regardless of if I have a vehicle or not.
   - Size: 1 – a simple Boolean, where we can decide to either send it to their home or have them come pick it up.

3. As a customer, I can select food items so I can feed my household
   - Size: 5 – must set up to where multiple items can be selected, while also updating quantity and other item information. Also, we have to consider substitutions.

4. As a customer, I can choose the time and date for the order to be fulfilled so that I can order ahead of time/when it is convenient.
   - Size: 1- simply the date, in which we can send the order to their doorstep at a certain time/date or have them come pick it up at a specific time/date

5. As a customer, I can note the quantity desired so that I have enough food for my household.
   - Size: 2 - must be applicable to all items, and we must consider which items are out of stock or not. We must also consider substitute items.

User stories 1, 3, and 5 heavily rely on the implementation of items, meaning all items and all of their specific information must be integrated within the website. User stories 2 and 4 also relate to the items, but more so in a foreign way, as these stories primarily relate to the order itself. The order will affect the items, as the quantity will decrease as more items are selected while the customer orders. Stories 3 and 5 relate to one another as they both consider substitute items, as if the quantity is out of stock, we must be able to select/be given a substitute item in place of the unavailable item.

## Creating the ER Diagram and Redgate Schema

Converting the scenario into the ER Diagram was fairly simple. At first, my three entities were:

1. Store
2. Item
3. Customer

where the store sells items and the customer orders items. However, because the store only had one attribute, being the owner, it really served no purpose. Instead, I created a new entity: Manufacterer, which replaced store. Now, we know which manufacterer produced which item, which is a lot more useful piece of information. In this way, we can still identify which store we send the items to without any redundant attributes. After this change, the construction of the ER diagram was straightforward, as an item belongs to 1 manufacterer, but a manufacterer can create multiple items. Then, a customer can either order nothing or perform many orders, and an item can either not be sent out to an order or many of that item can be sent through an order. This concludes the construction of the ER Diagram.

![ER Diagram]({{ '/assets/images/ER.png' | relative_url }})

Using the ER Diagram, I constructed the Redgate Schema. To do this, I simply created the entities and relationships, and created each of their resepctive attributes. I then created respective primary keys, and utilizing the same connections as the ER Diagram (which are set up differently) automatically created foreign keys for each entity (manufacterer_id should be a FK in Items, but it didn't register for some reason).

![Redgate Schema]({{ '/assets/images/REDGATE.jpg' | relative_url }})

## Complications and Conclusion

I would say that I am satisfied with this data representation, as it covers the basic design of this web model. I would definitely say it could be expanded with more entities and relationships, which may enhance the functionailty of the webpage. I encountered some complications with creating the redgate schema, as it was not allowing me to make connections/relations between entities. The differences between the ER Diagram and Redgate Schema relationships (1 to many, 1 and 1 only, etc) are confusing, but I was able to construct a decent model to represent the given prompt.
