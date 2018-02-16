# ExpandedTextAd
Represents an expanded text ad in the Bing Ads system.

Example usage:
```javascript
 var stats = ad.getStatsFor("THIS_MONTH");
```

# Methods
|Method Name|Return Type|Description|
|-|-|-
[asType](#astype)|[AdViewSpace](./AdViewSpace)|Returns an AdViewSpace object, which provides access to properties specific to the type of this ad.<br />
[enable](#enable)|void|Enables the ad.<br />
[getAdGroup](#getadgroup)|[AdGroup](./AdGroup)|Returns the parent ad group of this ad.<br />
[getApprovalStatus](#getapprovalstatus)|String|Returns the approval status of this ad. Supported values include:<br /> <br /> APPROVED,<br /> DISAPPROVED<br /><br />
[getCampaign](#getcampaign)|[Campaign](./Campaign)|Returns the parent campaign of this ad.<br />
[getDescription](#getdescription)|String|Returns the description of this ad.<br />
[getDisapprovalReasons](#getdisapprovalreasons)|String[]|Returns an array containing the reasons for which this ad was disapproved. If it is not disapproved, the array will be empty.<br />
[getEntityType](#getentitytype)|String|Returns the type of entity of this ad, which is “Ad”.<br />
[getHeadlinePart1](#getheadlinepart1)|String|Returns the first part of the headline (title) of this ad. <br />
[getHeadlinePart2](#getheadlinepart2)|String|Returns the second part of the headline (title) of this ad. <br />
[getId](#getid)|long|Returns the ID of this ad. In order to specify a unique ID for an ad, both its ad group ID and this ID need to be specified. <br />
[getPath1](#getpath1)|String|Returns the first path that appears with this ad's display URL.<br />
[getPath2](#getpath2)|String|Returns the second path that appears with this ad's display URL.<br />
[getStatsFor(String dateRange)](#getstatsfor~string-daterange~)|String|Returns stats for this ad for the given date range. Supported values include:<br /> <br /> `TODAY`<br /> `YESTERDAY`<br /> `LAST_7_DAYS`<br /> `THIS_WEEK_SUN_TODAY`<br /> `LAST_14_DAYS`<br /> `LAST_30_DAYS`<br /> `LAST_WEEK_SUN_SAT`<br /> `THIS_MONTH`<br /> `LAST_MONTH`<br /> `ALL_TIME`<br /><br />
[getStatsFor(Object dateFrom, Object dateTo)](#getstatsfor~object-datefrom_-object-dateto~)|String|Returns stats for this ad for the given custom date range. Both parameters can be either a string in YYYYMMDD format or an object with year, month and day properties. In either case, a full date must be specified. <br />
[getType](#gettype)|String|Returns the type of this ad. Supported values include:<br /> <br /> `EXPANDED_TEXT_AD` and `TEXT_AD`<br /><br />
[isEnabled](#isenabled)|boolean|Returns true if this ad is enabled. <br />
[isPaused](#ispaused)|boolean|Returns true if this ad is paused <br />
[isType](#istype)|[AdTypeSpace](./AdTypeSpace)|Returns an AdTypeSpace object which provides more information on the type of this ad.<br />
[pause](#pause)|void|Pauses this ad.<br />
[remove](#remove)|void|Removes this ad.<br />
[urls](#urls)|[AdUrls](./AdUrls)|Returns an AdUrls object which provides access to the URL fields of this <br />
&nbsp;|&nbsp;|&nbsp;

## <a name="astype"></a>asType
Returns an AdViewSpace object, which provides access to properties specific to the type of this ad.

### Returns:
|Type|Description|
|-|-
[AdViewSpace](./AdViewSpace)|An AdViewSpace.
&nbsp;|&nbsp;
## <a name="enable"></a>enable
Enables the ad.

### Returns:
|Type|Description|
|-|-
void|The ad group to which this ad belongs.
&nbsp;|&nbsp;
## <a name="getadgroup"></a>getAdGroup
Returns the parent ad group of this ad.

### Returns:
|Type|Description|
|-|-
[AdGroup](./AdGroup)|The ad group to which this ad belongs.
&nbsp;|&nbsp;
## <a name="getapprovalstatus"></a>getApprovalStatus
Returns the approval status of this ad. Supported values include:<br /> <br /> APPROVED,<br /> DISAPPROVED<br />

### Returns:
|Type|Description|
|-|-
String|
&nbsp;|&nbsp;
## <a name="getcampaign"></a>getCampaign
Returns the parent campaign of this ad.

### Returns:
|Type|Description|
|-|-
[Campaign](./Campaign)|The campaign to which this ad belongs.
&nbsp;|&nbsp;
## <a name="getdescription"></a>getDescription
Returns the description of this ad.

### Returns:
|Type|Description|
|-|-
String|The description of the ad.
&nbsp;|&nbsp;
## <a name="getdisapprovalreasons"></a>getDisapprovalReasons
Returns an array containing the reasons for which this ad was disapproved. If it is not disapproved, the array will be empty.

### Returns:
|Type|Description|
|-|-
String[]|
&nbsp;|&nbsp;
## <a name="getentitytype"></a>getEntityType
Returns the type of entity of this ad, which is “Ad”.

### Returns:
|Type|Description|
|-|-
String|Type of this entity: "Ad".
&nbsp;|&nbsp;
## <a name="getheadlinepart1"></a>getHeadlinePart1
Returns the first part of the headline (title) of this ad. 

### Returns:
|Type|Description|
|-|-
String|The first part of the ad's headline.
&nbsp;|&nbsp;
## <a name="getheadlinepart2"></a>getHeadlinePart2
Returns the second part of the headline (title) of this ad. 

### Returns:
|Type|Description|
|-|-
String|The second part of the ad's headline.
&nbsp;|&nbsp;
## <a name="getid"></a>getId
Returns the ID of this ad. In order to specify a unique ID for an ad, both its ad group ID and this ID need to be specified. 

### Returns:
|Type|Description|
|-|-
long|The ID of the ad.
&nbsp;|&nbsp;
## <a name="getpath1"></a>getPath1
Returns the first path that appears with this ad's display URL.

### Returns:
|Type|Description|
|-|-
String|The first path that appears with the ad's displayed URL.
&nbsp;|&nbsp;
## <a name="getpath2"></a>getPath2
Returns the second path that appears with this ad's display URL.

### Returns:
|Type|Description|
|-|-
String|The second path that appears with the ad's displayed URL.
&nbsp;|&nbsp;
## <a name="getstatsfor~string-daterange~"></a>getStatsFor(String dateRange)
Returns stats for this ad for the given date range. Supported values include:<br /> <br /> `TODAY`<br /> `YESTERDAY`<br /> `LAST_7_DAYS`<br /> `THIS_WEEK_SUN_TODAY`<br /> `LAST_14_DAYS`<br /> `LAST_30_DAYS`<br /> `LAST_WEEK_SUN_SAT`<br /> `THIS_MONTH`<br /> `LAST_MONTH`<br /> `ALL_TIME`<br />

### Arguments:
|Name|Type|Description|
|-|-|-
dateRange|String|Date range for which the stats are requested.
&nbsp;|&nbsp;|&nbsp;
### Returns:
|Type|Description|
|-|-
String|The stats for the specified date range.
&nbsp;|&nbsp;
## <a name="getstatsfor~object-datefrom_-object-dateto~"></a>getStatsFor(Object dateFrom, Object dateTo)
Returns stats for this ad for the given custom date range. Both parameters can be either a string in YYYYMMDD format or an object with year, month and day properties. In either case, a full date must be specified. 

### Arguments:
|Name|Type|Description|
|-|-|-
dateFrom|Object|Start date of the date range. Must be either a string in <code>YYYYMMDD</code> form,<br />                 or an object with <code>year</code>, <code>month</code> and <code>day</code> properties.
dateTo|Object|End date of the date range. Must be either a string in <code>YYYYMMDD</code> form,<br />                 or an object with <code>year</code>, <code>month</code> and <code>day</code> properties.
&nbsp;|&nbsp;|&nbsp;
### Returns:
|Type|Description|
|-|-
String|The stats for the specified date range.
&nbsp;|&nbsp;
## <a name="gettype"></a>getType
Returns the type of this ad. Supported values include:<br /> <br /> `EXPANDED_TEXT_AD` and `TEXT_AD`<br />

### Returns:
|Type|Description|
|-|-
String|The type of the ad.
&nbsp;|&nbsp;
## <a name="isenabled"></a>isEnabled
Returns true if this ad is enabled. 

### Returns:
|Type|Description|
|-|-
boolean|true if the ad is enabled.
&nbsp;|&nbsp;
## <a name="ispaused"></a>isPaused
Returns true if this ad is paused 

### Returns:
|Type|Description|
|-|-
boolean|true if the ad is paused.
&nbsp;|&nbsp;
## <a name="istype"></a>isType
Returns an AdTypeSpace object which provides more information on the type of this ad.

### Returns:
|Type|Description|
|-|-
[AdTypeSpace](./AdTypeSpace)|An AdTypeSpace.
&nbsp;|&nbsp;
## <a name="pause"></a>pause
Pauses this ad.

### Returns:
|Type|Description|
|-|-
void|Access to this ad's URL fields.
&nbsp;|&nbsp;
## <a name="remove"></a>remove
Removes this ad.

### Returns:
|Type|Description|
|-|-
void|Access to this ad's URL fields.
&nbsp;|&nbsp;
## <a name="urls"></a>urls
Returns an AdUrls object which provides access to the URL fields of this 

### Returns:
|Type|Description|
|-|-
[AdUrls](./AdUrls)|Access to this ad's URL fields.
&nbsp;|&nbsp;