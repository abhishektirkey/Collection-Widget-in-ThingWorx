# Collection-Widget-in-ThingWorx
A small demonstration of use of collection Widget in ThingWorx

This Project is made for practice purpose.

Clone of a Caterpillar Brands website - https://www.caterpillar.com/en/brands.html

1. Downloaded images/logos of each brand from Caterpillar Website
2. Open ThingWorx > Media > Upload 17 images one by one
	Note - If you do not upload the images in the thingworx than while creating a collection widget you cannot able to see the images there.

1. Make a Data Shape which consist of - Name, Logo (As ImageLink) and Link
2. Make a data table and add the datashape that you have created.
3. Add the data in the data table.
4. Create a service which return all the data table data.

1. Your need to create 2 Mashup - 1. Main Mashup where Collection widget is used
						2. Template mashup - where you will make structure of the collection widget and bindings.

1. Main Mashup
	Drag Collection Widget in Canvas
	In Data - Call the data table service which is returning all the data present in the data table.
	Bind data with collection widget
	In Properties - Set UID - name
				Set Mashup - Template Mashup (The 2nd Mahusup you have created)
				   JSON Mashup Properties - {
									"Name" : "Name",
									"Logo" : "Logo",
									"Link" : "Link"
								    };  
					left hand side should be similar to Table column name
					Right hand side should be similar to the configure mashup parameter of another mashup.
2. Template Mashup
	Drag widgets that are required - Images, Label, Button
	Select Mashup - Left top from Explorer
	In canvas left top you can see one arrow after clicking you can see configure mashup parameters - Add parameters with the same name you wrote in JSON Mashup property in main mashup.
	Link all the widgets with the left top arrow dropdown.

3. Go to main mashup and View Mashup - You can able to see the collection widgets that you have created.

Customise Mashup as per your need.
