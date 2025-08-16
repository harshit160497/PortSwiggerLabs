In Burp's browser, access the lab and click on a product.

In Proxy > HTTP history, notice the API request for the product. For example, /api/products/3/price.

Right-click the API request and select Send to Repeater.

In the Repeater tab, change the HTTP method for the API request from GET to OPTIONS, then send the request. Notice that the response specifies that the GET and PATCH methods are allowed.

Change the method for the API request from GET to PATCH, then send the request. Notice that you receive an Unauthorized message. This may indicate that you need to be authenticated to update the order.

In Burp's browser, log in to the application using the credentials wiener:peter.

Click on the Lightweight "l33t" Leather Jacket product.

In Proxy > HTTP history, right-click the API/products/1/price request for the leather jacket and select Send to Repeater.

In the Repeater tab, change the method for the API request from GET to PATCH, then send the request. Notice that this causes an error due to an incorrect Content-Type. The error message specifies that the Content-Type should be application/json.

Add a Content-Type header and set the value to application/json.

Add an empty JSON object {} as the request body, then send the request. Notice that this causes an error due to the request body missing a price parameter.

Add a price parameter with a value of 0 to the JSON object {"price":0}. Send the request.

In Burp's browser, reload the leather jacket product page. Notice that the price of the leather jacket is now $0.00.

Add the leather jacket to your basket.

Go to your basket and click Place order to solve the lab.

