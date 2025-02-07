# Collection-Widget-in-ThingWorx
A small demonstration of use of collection Widget in ThingWorx

---

**This project is for practice purposes.**

**Clone of a Caterpillar Brands website** - Caterpillar Brands

1. Download images/logos of each brand from the Caterpillar website.
2. Open ThingWorx > Media > Upload 17 images one by one.
   - **Note:** If you do not upload the images in ThingWorx, you will not be able to see the images while creating a collection widget.

**Steps:**

1. Create a Data Shape consisting of:
   - Name
   - Logo (as ImageLink)
   - Link
2. Create a Data Table and add the Data Shape you have created.
3. Add data to the Data Table.
4. Create a service that returns all the data from the Data Table.

**Mashups:**

1. You need to create 2 Mashups:
   - **Main Mashup:** Where the Collection widget is used.
   - **Template Mashup:** Where you will define the structure of the Collection widget and bindings.

**Main Mashup:**

1. Drag the Collection Widget onto the Canvas.
2. In Data, call the Data Table service that returns all the data present in the Data Table.
3. Bind the data with the Collection Widget.
4. In Properties:
   - Set UID to "name".
   - Set Mashup to "Template Mashup" (the second Mashup you created).
   - Set JSON Mashup Properties:
     ```json
     {
       "Name": "Name",
       "Logo": "Logo",
       "Link": "Link"
     }
     ```
     - The left-hand side should match the table column names.
     - The right-hand side should match the configured Mashup parameters of the other Mashup.

**Template Mashup:**

1. Drag the required widgets (Images, Label, Button) onto the Canvas.
2. Select Mashup from the left top in Explorer.
3. In the Canvas, click the arrow at the top left to see the configure Mashup parameters.
4. Add parameters with the same names you wrote in the JSON Mashup properties in the Main Mashup.
5. Link all the widgets with the dropdown from the top left arrow.

**Final Step:**

1. Go to the Main Mashup and view it. You should be able to see the Collection Widgets you have created.

---

Customise Mashup as per your need.
