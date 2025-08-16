Lab: Exploiting a mass assignment vulnerability


Solution
In Burp's browser, log in to the application using the credentials wiener:peter.

Click on the Lightweight "l33t" Leather Jacket product and add it to your basket.

Go to your basket and click Place order. Notice that you don't have enough credit for the purchase.

In Proxy > HTTP history, notice both the GET and POST API requests for /api/checkout.

Notice that the response to the GET request contains the same JSON structure as the POST request. Observe that the JSON structure in the GET response includes a chosen_discount parameter, which is not present in the POST request.

Right-click the POST /api/checkout request and select Send to Repeater.

In Repeater, add the chosen_discount parameter to the request. The JSON should look like the following:

{
    "chosen_discount":{
        "percentage":0
    },
    "chosen_products":[
        {
            "product_id":"1",
            "quantity":1
        }
    ]
}

Send the request. Notice that adding the chosen_discount parameter doesn't cause an error.

Change the chosen_discount value to the string "x", then send the request. Observe that this results in an error message as the parameter value isn't a number. This may indicate that the user input is being processed.

Change the chosen_discount percentage to 100, then send the request to solve the lab.
