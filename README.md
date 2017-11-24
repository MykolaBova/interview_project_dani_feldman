Using the data from Google places https://developers.google.com/places/web-service/search create a simple app to save places based on city and have the CRUD operations on them.

Implementation:

1. Create login in one of 3 ways:
  - Simple hash mapping similar to Basic HTTP authentication
  - Shiro
  - Login with Google (prefered one)
2. Have a list with places based on city, have a combo or something to select the city and show places only from that location
3. Populate the list by doing a search with let’s’ say 5km radius and keep the results in db and on a future search match the existing ones and override the data only if the user did not changed the data from your app, simple dirty flag will do
First you can only save the basic info in list and on first edit on a place you could fetch the details using the details api. If you want to make your life more complicated you could implement and async fetch and get the details also, you can use Quartz or my prefered one ExecutorService
4. Implement CRUD operations on each of  these places, also show images and show it on map when you edit it
5. In list view show a map with all the places. I think this will help https://developers.google.com/maps/documentation/javascript/tutorial if not google is your friend :)
6. Implement various filters on the list, choose the fields you think it would matter for you as a traveler :)

Bonus:
   - Save values to elasticsearch https://www.elastic.co/ and do list filters from there. Use the java api, it will make your life easier
  - Expose a basic REST service, you can use Jersey https://jersey.java.net

Technologies to use:

PostgreSQL
Jetty
GWT
Guice
JPA
Elasticsearch
Jersey
