Sub category
============

This function is only available for the architecture modes number two and three (Items, categories and reviews).
For more information, check : :doc:`website_architecture`.

This functionality allows you to create a sub category.

Create or reuse a content type as a sub category. Here is an example of a city that will belong to a country : ::

	cities:
	    name: Cities
	    singular_name: City
	    fields:
	        title:
	            type: text
	            required: true
	            pattern: "^.{1,45}$"
	            class: large
	            group: "Location"
	        slug:
	            type: slug
	            uses: [ title ]
	        content:
	            type: textarea
	            height: 150px
	            pattern: "^.{1,140}$"
	            required: true
	        image:
	            type: image
	            attrib: [alt, title]
	            extensions: [ gif, jpg, png ]
	            upload: location
	    relations:
	        countries:
	            multiple: true
	            order: title
	            label: Select zero or more countries
	    show_on_dashboard: true
	    default_status: published
	    record_template: record.twig
	    listing_template: listing.twig
	    searchable: false
	    icon_many: "fa:cubes"
	    icon_one: "fa:cube"
	    slug: cities
    
Note the relation to the countries.

Now create or reuse a content type as a category. Here is an example for cities : ::

	countries:
	    name: Countries
	    singular_name: Country
	    fields:
	        title:
	            type: text
	            required: true
	            pattern: "^.{1,45}$"
	            class: large
	            group: "Location"
	        slug:
	            type: slug
	            uses: [ title ]
	        content:
	            type: textarea
	            height: 150px
	            pattern: "^.{1,140}$"
	            required: true
	        image:
	            type: image
	            attrib: [alt, title]
	            extensions: [ gif, jpg, png ]
	            upload: location
	    show_on_dashboard: true
	    default_status: published
	    record_template: subcat_record.twig
	    listing_template: listing.twig
	    searchable: false
	    icon_many: "fa:cubes"
	    icon_one: "fa:cube"
	    slug: countries
	    
Note the use of "subcat_record.twig" that is a twig template to show the sub categories when viewing a city.

Last step, you need to modify the template for your items "item.twig".
Change the related content (it has nothing to do with the chapter :doc:`related_content` but with the relationships) to only show the relations that are items otherwise it would include the category as well.

Change the line : ::

	{% set items = record.related('') %}
	  
To : ::

	{% set items = record.related('items') %}
	
If your items are not called items anymore, please change accordingly.
 
Dont forget to modify the relations of your items to link them to your sub category instead of your category.