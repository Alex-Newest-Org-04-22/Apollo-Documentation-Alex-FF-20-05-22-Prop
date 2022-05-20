# Cart Popup Displayed

### 

## Javascript Code
```js
window.appEventData = window.appEventData || [];
appEventData.push({
  "event": "Cart Popup Displayed",
    "cart": {
        "cartID": "<cartID>",
        "item": [
            {
                "productInfo": {
                    "productID": "<productID>"
                }
            }
        ]
    }
});
```

## Variable Definitions

|Path|Type|Description|Example|Pattern|Min Length|Max Length|Minimum|Maximum|Multiple Of|
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|cart.cartID|string|Back-end identifier for a shopping cart|12345, 435678, 34567, XCV456, XCV876|||||||
|cart.item[n].productInfo.productID|string|Unique Identifier of a product or offering.  Must match the format of back-end systems if used as a key for import of product meta data. Most often, one level above SKU for products with SKU variants. |155, 65588, 987764448|||||||




