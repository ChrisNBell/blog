---
layout: post
title: Introduction Post
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
