# Order Placed

### 

## Javascript Code
```js
window.appEventData = window.appEventData || [];
appEventData.push({
  "event": "Order Placed",
    "cart": {
        "cartID": "<cartID>"
    },
    "transaction": {
        "item": [
            {
                "price": {
                    "sellingPrice": "<sellingPrice>"
                },
                "productInfo": {
                    "brand": "<brand>",
                    "businessUnit": "<businessUnit>",
                    "name": "<name>",
                    "productID": "<productID>",
                    "sku": "<sku>"
                },
                "quantity": <quantity>
            }
        ],
        "productIDList": "<productIDList>",
        "purchaseID": "<purchaseID>",
        "skuList": "<skuList>",
        "total": {
            "currency": "<currency>"
        },
        "transactionID": "<transactionID>"
    }
});
```

## Variable Definitions

|Path|Type|Description|Example|Pattern|Min Length|Max Length|Minimum|Maximum|Multiple Of|
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|cart.cartID|string|Back-end identifier for a shopping cart|12345, 435678, 34567, XCV456, XCV876|||||||
|transaction.item[n].price.sellingPrice|string|String representation of the price paid after coupons or discounts. Positive. Up to two decimal places for cents. No currency symbol.|200, 29.99, 50, 0|^[0-9]*(\.[0-9]{1,2})?$||||||
|transaction.item[n].productInfo.brand|string|Describes the brand of a product or offering.|Ford, Chevrolet, Dodge, Levis, Columbia, Patagonia|||||||
|transaction.item[n].productInfo.businessUnit|string|The business unit associated with each product.|Apparel, Shoes, Home|||||||
|transaction.item[n].productInfo.name|string|Name of the product or offering.  Should be unique and 1:1 with productID|Oceana, Corsica, Flame Tech, Air Jordan 88|||||||
|transaction.item[n].productInfo.productID|string|Unique Identifier of a product or offering.  Must match the format of back-end systems if used as a key for import of product meta data. Most often, one level above SKU for products with SKU variants. |155, 65588, 987764448|||||||
|transaction.item[n].productInfo.sku|string|Stock Keeping Unit \(SKU\) Unique Identifier of specific item \(typically\) held in inventory.  Must match the format of back-end systems if used as a key for import of product meta data. Most often, one level below productID for products with SKU variants. |34567890, 4567890, 00155-large-cornflower|||||||
|transaction.item[n].quantity|integer|Integer number of products being acted upon \(added to a cart, removed from wishlist, purchased, reserved\)|1, 2, 3, 4, 5||||1|||
|transaction.productIDList|string|A delimited list of product IDs in the transaction.|1234\|7878\|9039, abc12\|deh213, abc12|||||||
|transaction.purchaseID|string|Unique identifier of the purchase. Max Length 20. Used as Unique ID of the purchase or deduplication.|ABC-132456789, DEF-132456789, 0987654567|^[a-zA-Z0-9]{6,20}$|6|20||||
|transaction.skuList|string| A delimited list of skus in the transaction.|sku123\|sku465, 67890\|87576\|74674, 87654|||||||
|transaction.total.currency|string|Currency of the transaction. ISO 4217 \(3 character alpha\), uppercase |USD, CAD, GBP, CHF|^[A-Z]{3}$|3|3||||
|transaction.transactionID|string|Unique identifier of the transaction. Max Length 100. Used as a key for upload of post transaction data. |123e4567-e89b-12d3-a456-426614174000|^[a-zA-Z0-9]{6,100}$|6|100||||




