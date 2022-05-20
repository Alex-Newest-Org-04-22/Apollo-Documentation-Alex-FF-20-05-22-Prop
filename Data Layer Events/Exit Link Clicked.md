# Exit Link Clicked

### 

## Javascript Code
```js
window.appEventData = window.appEventData || [];
appEventData.push({
  "event": "Exit Link Clicked",
    "linkInfo": {
        "linkContainer": "<linkContainer>",
        "linkId": "<linkId>",
        "linkRegion": "<linkRegion>",
        "linkTarget": "<linkTarget>"
    }
});
```

## Variable Definitions

|Path|Type|Description|Example|Pattern|Min Length|Max Length|Minimum|Maximum|Multiple Of|
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|linkInfo.linkContainer|string|Indicates the container for a clicked link within the hierarchy \[Site &gt; Page &gt; Region &gt; Container &gt; linkID\]|Best Friends - Best Jeans, Puppy Love, Sail Away, Mens, Kids, Kids : Tops|||||||
|linkInfo.linkId|string|Identifier of the link clicked|act now, cancel, ok, 3456, 8765|||||||
|linkInfo.linkRegion|string|Indicates the region on page for a clicked link within the hierarchy \[Site &gt; Page &gt; Region &gt; Container &gt; linkID\]|Top Nav, Footer Nav, Hero, Recommended, Also Shopped, Also Bought|||||||
|linkInfo.linkTarget|string|HREF of the link.  Primarily useful for exit link tracking. |https:\/\/www.usda.gov. https:\/\/msnbc.com|||||||




