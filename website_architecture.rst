Website architecture
====================

The template offers three different architectures.

Default mode
############

With this architecture you don't have to configure anything. The pages that you will create will be displayed as cards on the first page and links to see the pages.

How to activate
***************

This is the default mode you don't have to do anything. If you want to come back to this mode, in the dashboard, in the menu on the left go to File management -> view/edit templates -> affiliatews -> theme.yml

Set the variable ws_mode to 1 : ::

	ws_mode: 1

Items and categories
#####################

This architecture requires more configuration as it is based on personalized content types.

The website is organized with items and categories. An item can belong to zero, one or multiple categories.

It is possible to create different kinds of categories.

The template offers the following categories :

* Location
* Period
* Price

Based on these examples, it's very easy to create new ones that suit exaclty your needs such as brand, size, color, ...

Moreover, every item can be tagged and a menu per category can be set to show the categories for a very quick and friendly navigation.

Our content types are available on : https://github.com/symbiodyssey/bolt-affiliate-template/tree/master/contentTypes

The official documentation explains how to use content types in Bolt : https://docs.bolt.cm/3.4/contenttypes/intro

With this architecture if a visitor clicks on an item he/she will be directly redirected to an external website of your choice.

How to activate
***************

To activate this mode, in the dashboard, in the menu on the left go to File management -> view/edit templates -> affiliatews -> theme.yml

Set the variable ws_mode to 2 : ::

	ws_mode: 2

Items, categories and reviews
#############################

This architecture is very similar to the previous one except that clicking on a item will lead first to a review page where one can read a long and detailed article about the item.

How to activate
***************
In the dashboard, in the menu on the left go to File management -> view/edit templates -> affiliatews -> theme.yml

Set the variable ws_mode to 3 : ::

	ws_mode: 3