# Download Link Clicked

### 

## Javascript Code
```js
window.appEventData = window.appEventData || [];
appEventData.push({
  "event": "Download Link Clicked",
    "linkInfo": {
        "fileName": "<fileName>",
        "fileType": "<fileType>",
        "linkContainer": "<linkContainer>",
        "linkId": "<linkId>",
        "linkRegion": "<linkRegion>"
    }
});
```

## Variable Definitions

|Path|Type|Description|Example|Pattern|Min Length|Max Length|Minimum|Maximum|Multiple Of|
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|linkInfo.fileName|string|Indicates the filename for download link tracking.|Year End 2012.pdf, Operating Instructions.doc`|||||||
|linkInfo.fileType|string|Indicates the file type for download link tracking.|pdf, doc, csv, dmp, zip|||||||
|linkInfo.linkContainer|string|Indicates the container for a clicked link within the hierarchy \[Site &gt; Page &gt; Region &gt; Container &gt; linkID\]|Best Friends - Best Jeans, Puppy Love, Sail Away, Mens, Kids, Kids : Tops|||||||
|linkInfo.linkId|string|Identifier of the link clicked|act now, cancel, ok, 3456, 8765|||||||
|linkInfo.linkRegion|string|Indicates the region on page for a clicked link within the hierarchy \[Site &gt; Page &gt; Region &gt; Container &gt; linkID\]|Top Nav, Footer Nav, Hero, Recommended, Also Shopped, Also Bought|||||||




