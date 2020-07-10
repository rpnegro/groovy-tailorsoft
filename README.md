# groovy-tailorsoft
Script Objetive: Get a Json structure from a web server and parses into a table with this columns: 
- Name of the product
- Number of orders placed for that product
- Total dollars spent on that product across all orders.

Json Structure:
{
    "products" : [
        {"id":"xx", "name" : "xx", "price" : "xx"},
        {"id":"xx", "name" : "xx", "price" : "xx"},
    ],
    "orders" : [
        { 
            "id" : "xx",
            "items" : [
                {"productId" : "xx", "quantity":xx},
                {"productId" : "xx", "quantity":xx}
            ]
        },
    ],
}

Asumtions: The Json is a static structure with no changes during the execution of this scritp. 
If this contidition change, the script need to be adjusted for data integrity and optimal results.

Considerations: Change the type of JsonSlurper to support fast processing, recommendation is to use INDEX_OVERLAY 
for JSON buffers under 2MB. https://docs.groovy-lang.org/2.5.7/html/gapi/groovy/json/JsonSlurper.html for more information. 
Require to import.json.JsonParserType. Check Groovy version for specific API information 
--> println "Groovy version: " + GroovySystem.getVersion()

Customer: TailorSoft
Version 0.1
Developer: @rpnegro
