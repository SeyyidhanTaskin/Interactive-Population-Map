# Interactive-Population-Map


1- First, download information about a country of your choice, including its city name, population, latitude, and longitude, in CSV format.

2- In the "Get started by adding integrations" section of Elasticsearch's "Home" interface, click on "Upload a file."

3- Click on "Select or drag and drop a file," choose the CSV file you downloaded, and click "Import" in the bottom left corner.

4- Give your CSV file a name, then go to "Index Management" and search for the file name in the "Indices" section. Click on it.

5- After clicking on your index, go to the "Mapping" section, copy the original mappings, go to "Dev Tools," paste the mappings along with the new project name, and execute.

6- Copy the mappings again, create a new index, and paste the copied mappings under the new index.

7- Now it's time to create your custom mappings.

8- I've provided a sample file named "Original Mappings" and "Custom Mappings" for you. You can use them as a reference to create your mappings.

9- After executing the original mappings, copy them again and create a new index for your custom mappings. Paste the mappings under the new index.

10- It's time to perform "POST _reindex" with the original mappings index and the custom mappings index.

11- Don't go to the Dashboard immediately because the first "location" you created won't bring you cities and other data.

12- Create another field named "location2" in the index with custom mappings, type "geo_point," specifying latitude and longitude.

13- Create an "Ingest Pipeline" for "location2" to bring cities and populations based on latitude and longitude values.

14- After creating the Ingest Pipeline, don't forget to perform "_update_by_query" on your index with the pipeline name.

15- Go to "Stack Management," then "Data Views," and click on "Create data view." Enter a name, but make sure to write the index of your custom mappings in the "Index Pattern" section.

16- After entering the information, click on "Save data view to Kibana." Now you can go to "Kibana Maps."

17- In Kibana Maps, click on "Add layer," then select "Documents."

18- In the search bar, enter the index of your custom mappings saved in the "Data View" and explore your project.

19- The map will display all cities for the chosen country.

20- Click on "Add Layer" again, and you can customize the visualization of cities according to your preferences.
