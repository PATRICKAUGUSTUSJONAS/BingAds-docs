# AdGroupUrls
Provides access to the URLs for this ad group.

# Methods
|Method Name|Return Type|Description|
|-|-|-
[clearTrackingTemplate](#cleartrackingtemplate)|void|Clears the tracking template of this ad group.<br />
[getCustomParameters](#getcustomparameters)|Object|Returns the custom parameters of this ad group. The returned object is in the format:<br /><br /><code>{ key: 'value1', key2: 'value2', key3: 'value3' }</code><br />
[getTrackingTemplate](#gettrackingtemplate)|String|Returns the tracking template of this ad group.<br />
[setCustomParameters(Object customParameters)](#setcustomparameters~object-customparameters~)|void|Sets the custom parameters of this ad group.<br />
[setTrackingTemplate(String trackingTemplate)](#settrackingtemplate~string-trackingtemplate~)|void|Sets the tracking template of this ad group.<br />
&nbsp;|&nbsp;|&nbsp;

## <a name="cleartrackingtemplate"></a>clearTrackingTemplate
Clears the tracking template of this ad group.

### Returns:
|Type|Description|
|-|-
void|The custom parameters of the ad group as a map of the following form: {key1: 'value1', key2: 'value2', key3: 'value3'}.
&nbsp;|&nbsp;
## <a name="getcustomparameters"></a>getCustomParameters
Returns the custom parameters of this ad group. The returned object is in the format:<br /><br /><code>{ key: 'value1', key2: 'value2', key3: 'value3' }</code>

### Returns:
|Type|Description|
|-|-
Object|The custom parameters of the ad group as a map of the following form: {key1: 'value1', key2: 'value2', key3: 'value3'}.
&nbsp;|&nbsp;
## <a name="gettrackingtemplate"></a>getTrackingTemplate
Returns the tracking template of this ad group.

### Returns:
|Type|Description|
|-|-
String|The tracking template of the ad group.
&nbsp;|&nbsp;
## <a name="setcustomparameters~object-customparameters~"></a>setCustomParameters(Object customParameters)
Sets the custom parameters of this ad group.

### Arguments:
|Name|Type|Description|
|-|-|-
customParameters|Object|The custom parameters of the ad group as a map of the<br />        form <code>{key1: 'value1', key2: 'value2', key3: 'value3'}</code>.
&nbsp;|&nbsp;|&nbsp;
### Returns:
|Type|Description|
|-|-
void|
&nbsp;|&nbsp;
## <a name="settrackingtemplate~string-trackingtemplate~"></a>setTrackingTemplate(String trackingTemplate)
Sets the tracking template of this ad group.

### Arguments:
|Name|Type|Description|
|-|-|-
trackingTemplate|String|The tracking template of the ad group.
&nbsp;|&nbsp;|&nbsp;
### Returns:
|Type|Description|
|-|-
void|
&nbsp;|&nbsp;