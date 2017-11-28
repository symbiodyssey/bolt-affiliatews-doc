Google Analytics
================

First, you need to create a Google Analytics account : https://www.google.com/analytics

The extension "Google Analytics" (bolt/googleanalytics) allows you to link your Google Analytics account.
Install it : :ref:`required-extensions`.

Please follow their instructions to set it correctly.

Activate the click events
*************************

This function is only available for the architecture modes number two and three.
For more information, check : :doc:`website_architecture`.

This mode allows you to trigger an event on Google Analytics every time someone clicks on an affiliate link ("Get it" button).

In the dashboard, in the menu on the left go to File management -> view/edit templates -> affiliatews -> theme.yml

Set the variable ws_ga to 1 : ::

	ws_ga: 1
	
For more information about events : https://support.google.com/analytics/answer/1033068?hl=en