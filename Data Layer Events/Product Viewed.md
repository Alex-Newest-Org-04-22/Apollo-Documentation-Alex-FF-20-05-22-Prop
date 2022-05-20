# Product Viewed

### This event is part of the page load sequence, including virtual page loads in the case of single page apps, and must be pushed between the `Page Load Started` and `Page Load Completed` events.

## Javascript Code
```js
window.appEventData = window.appEventData || [];
appEventData.push({
  "event": "Product Viewed",
    "product": [
        {
            "price": {
                "sellingPrice": "<sellingPrice>"
            },
            "productInfo": {
                "brand": "<brand>",
                "businessUnit": "<businessUnit>",
                "discountAmount": "<discountAmount>",
                "fulfillmentOptions": "<fulfillmentOptions>",
                "isOutOfStock": <isOutOfStock>,
                "isSKuAvailable": <isSKuAvailable>,
                "name": "<name>",
                "productID": "<productID>",
                "quantityAvailable": "<quantityAvailable>",
                "ratingCountAndAverageCombined": "<ratingCountAndAverageCombined>",
                "sku": "<sku>",
                "status": "<status>"
            }
        }
    ]
});
```

## Variable Definitions

|Path|Type|Description|Example|Pattern|Min Length|Max Length|Minimum|Maximum|Multiple Of|
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|product[n].price.sellingPrice|string|String representation of the price paid after coupons or discounts. Positive. Up to two decimal places for cents. No currency symbol.|200, 29.99, 50, 0|^[0-9]*(\.[0-9]{1,2})?$||||||
|product[n].productInfo.brand|string|Describes the brand of a product or offering.|Ford, Chevrolet, Dodge, Levis, Columbia, Patagonia|||||||
|product[n].productInfo.businessUnit|string|The business unit associated with each product.|Apparel, Shoes, Home|||||||
|product[n].productInfo.discountAmount|string|The product discount amount shown to the visitor for each product.|$20, 10%, $5|||||||
|product[n].productInfo.fulfillmentOptions|string|The product fulfillment options available for each product to view impact on conversion.|Shipped Only, In Store Only, Local Pickup Only, In Store or Ship, Digital \(Email or Text\)|||||||
|product[n].productInfo.isOutOfStock|boolean|Boolean flag indicating that an inventoried product is out of stock. |TRUE, FALSE|||||||
|product[n].productInfo.isSKuAvailable|boolean|True\/False flag to indicate if product SKU is known at the time of the event|true, false|||||||
|product[n].productInfo.productID|string|Unique Identifier of a product or offering.  Must match the format of back-end systems if used as a key for import of product meta data. Most often, one level above SKU for products with SKU variants. |155, 65588, 987764448|||||||
|product[n].productInfo.quantityAvailable|string|The product quantity available.|1, 10, 100|||||||
|product[n].productInfo.ratingCountAndAverageCombined|string|Combined Rating Count and Rating Average with colon as delimiter|23:4.5, 222:1.7, 1:5, 2:3.5|||||||
|product[n].productInfo.sku|string|Stock Keeping Unit \(SKU\) Unique Identifier of specific item \(typically\) held in inventory.  Must match the format of back-end systems if used as a key for import of product meta data. Most often, one level below productID for products with SKU variants. |34567890, 4567890, 00155-large-cornflower|||||||
|product[n].productInfo.status|string|Described the product's status|In Stock, Out of Stcok, Back-Ordered|||||||




