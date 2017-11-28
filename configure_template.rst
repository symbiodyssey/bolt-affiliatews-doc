Configure the template
======================

The template requires some extensions : :ref:`required-extensions`.

Set the labels
##############

In the dashboard in the menu on the left, go to Label translations.

Edit the labels as follow :

=============== ========
Label           EN
=============== ========
details         Details
get-it          Get it
show-more       Show more
related_content Related content
=============== ========

You can of course change the translation if you want.

Create the Blocks
#################

The template uses a few blocks that helps modify some specific elements of the website.

Logo
****

Create a block called Logo with the slug set as /block/logo.

Upload an image that will be visible on the top left corner.

Banner
******

Create a block called Banner with the slug set as /block/banner.

Upload an image that will be visible if the index.twig file is used.

404 Error
*********

Create a block called 404 Not found with the slug set as /block/404-not-found.

In the content you can write your own message that will be displayed if a visitor access a page that does not exist.
