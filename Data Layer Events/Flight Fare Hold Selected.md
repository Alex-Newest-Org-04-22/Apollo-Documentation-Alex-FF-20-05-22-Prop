# Flight Fare Hold Selected

### 

## Javascript Code
```js
window.appEventData = window.appEventData || [];
appEventData.push({
  "event": "Flight Fare Hold Selected",
    "airTravel": {
        "bookingLeadTime": "<bookingLeadTime>",
        "flightList": [
            {
                "tripId": "<tripId>"
            }
        ]
    }
});
```

## Variable Definitions

|Path|Type|Description|Example|Pattern|Min Length|Max Length|Minimum|Maximum|Multiple Of|
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|airTravel.bookingLeadTime|string|Number of days ahead of departure for the first segment of a trip.|zero, 1, 20, 22, 33|^([0-9])|(zero)$||||||
|airTravel.flightList[n].tripId|string|A unique representation of the main departure and arrival points for all primary trip legs \(not including connections\). |SFO&gt;YYC:YYC&gt;SFO, SFO&gt;YYC, SFO&gt;YYC:YYC&gt;YXC:YKA&gt;SFO|^([A-Z]{3}>[A-Z]{3}:?)+$||||||




