# Product Listing Item Clicked

### This event is part of the page load sequence, including virtual page loads in the case of single page apps, and must be pushed between the `Page Load Started` and `Page Load Completed` events.

## Javascript Code
```js
window.appEventData = window.appEventData || [];
appEventData.push({
  "event": "Product Listing Item Clicked",
    "listingDisplayed": {
        "sortOrder": "<sortOrder>"
    },
    "listingItemClicked": {
        "filterList": "<filterList>",
        "listing": [
            {
                "itemPosition": <itemPosition>,
                "price": {
                    "priceType": "<priceType>"
                },
                "productInfo": {
                    "brand": "<brand>",
                    "name": "<name>",
                    "productID": "<productID>",
                    "ratingAverage": "<ratingAverage>",
                    "ratingCount": <ratingCount>,
                    "sku": "<sku>",
                    "status": "<status>"
                }
            }
        ]
    }
});
```

## Variable Definitions

|Path|Type|Description|Example|Pattern|Min Length|Max Length|Minimum|Maximum|Multiple Of|
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|listingDisplayed.sortOrder|string|Indicates the sort order.|high-low, low-high, nearest-farthest, a-z, newest-oldest|||||||
|listingItemClicked.filterList|string|A twice delimited string of filterType and filterValue pairs.  Use \~ between type and value.  Use \| between pairs|sort\~price ascending\|color\~green\|size\~medium|||||||
|listingItemClicked.listing[n].itemPosition|integer|Integer position of a property within a sorted result. The first returned is position 1. For map results, this value can be the rank by distance from POI.|1, 2, 3, 4, 5||||0|||
|listingItemClicked.listing[n].price.priceType|string|Describes the type of price offered using commonly used terms. |1st mark, 2nd mark, 3rd mark, clearance, sale, doorbuster|||||||
|listingItemClicked.listing[n].productInfo.brand|string|Describes the brand of a product or offering.|Ford, Chevrolet, Dodge, Levis, Columbia, Patagonia|||||||
|listingItemClicked.listing[n].productInfo.name|string|Name of the product or offering.  Should be unique and 1:1 with productID|Oceana, Corsica, Flame Tech, Air Jordan 88|||||||
|listingItemClicked.listing[n].productInfo.productID|string|Unique Identifier of a product or offering.  Must match the format of back-end systems if used as a key for import of product meta data. Most often, one level above SKU for products with SKU variants. |155, 65588, 987764448|||||||
|listingItemClicked.listing[n].productInfo.ratingAverage|string|String representation of the average customer rating.  Positive. Up to two decimal places. This is most often a number between 0 and 5. |1.1, 2, 5|^[0-9]*(\.[0-9]{1,2})?$||||||
|listingItemClicked.listing[n].productInfo.ratingCount|integer|Integer number of customer ratings. |1, 5, 11, 200||||0|||
|listingItemClicked.listing[n].productInfo.sku|string|Stock Keeping Unit \(SKU\) Unique Identifier of specific item \(typically\) held in inventory.  Must match the format of back-end systems if used as a key for import of product meta data. Most often, one level below productID for products with SKU variants. |34567890, 4567890, 00155-large-cornflower|||||||
|listingItemClicked.listing[n].productInfo.status|string|Described the product's status|In Stock, Out of Stcok, Back-Ordered|||||||




