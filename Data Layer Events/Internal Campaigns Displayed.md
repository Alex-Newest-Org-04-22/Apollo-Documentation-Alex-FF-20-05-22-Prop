# Internal Campaigns Displayed

### 

## Javascript Code
```js
window.appEventData = window.appEventData || [];
appEventData.push({
  "event": "Internal Campaigns Displayed",
    "internalCampaign": {
        "campaignList": [
            {
                "internalCampaignCreative": "<internalCampaignCreative>",
                "internalCampaignID": "<internalCampaignID>",
                "internalCampaignName": "<internalCampaignName>"
            }
        ]
    }
});
```

## Variable Definitions

|Path|Type|Description|Example|Pattern|Min Length|Max Length|Minimum|Maximum|Multiple Of|
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|internalCampaign.campaignList[n].internalCampaignCreative|string|Describes the creative treatment for an internal campaign|Girl with bike, Mountain Top, River Cruise Danube|||||||
|internalCampaign.campaignList[n].internalCampaignID|string|Unique Identifier of an internal campaign|2345, 56789, 9876|||||||
|internalCampaign.campaignList[n].internalCampaignName|string|The name of the promotion.|Trek bikes for kids, REI Spring Sale 2019, Viking Cruise Fall Specials|||||||




