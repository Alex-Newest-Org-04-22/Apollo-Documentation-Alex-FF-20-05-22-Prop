# Listing Filter Removed

### 

## Javascript Code
```js
window.appEventData = window.appEventData || [];
appEventData.push({
  "event": "Listing Filter Removed",
    "listingRefined": {
        "filterList": "<filterList>"
    }
});
```

## Variable Definitions

|Path|Type|Description|Example|Pattern|Min Length|Max Length|Minimum|Maximum|Multiple Of|
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|listingRefined.filterList|string|A twice delimited string of filterType and filterValue pairs.  Use \~ between type and value.  Use \| between pairs|sort\~price ascending\|color\~green\|size\~medium|||||||




