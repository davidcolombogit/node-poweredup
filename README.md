## Classes

<dl>
<dt><a href="#LPF2">LPF2</a> ⇐ <code>EventEmitter</code></dt>
<dd></dd>
<dt><a href="#Hub">Hub</a> ⇐ <code>EventEmitter</code></dt>
<dd></dd>
<dt><a href="#WeDo2Hub">WeDo2Hub</a> ⇐ <code><a href="#Hub">Hub</a></code></dt>
<dd></dd>
<dt><a href="#BoostHub">BoostHub</a> ⇐ <code><a href="#Hub">Hub</a></code></dt>
<dd></dd>
</dl>

<a name="LPF2"></a>

## LPF2 ⇐ <code>EventEmitter</code>
**Kind**: global class  
**Extends**: <code>EventEmitter</code>  

* [LPF2](#LPF2) ⇐ <code>EventEmitter</code>
    * [.scan()](#LPF2+scan)
    * ["discover" (hub)](#LPF2+event_discover)

<a name="LPF2+scan"></a>

### lpF2.scan()
Begin scanning for LPF2 Hub devices.

**Kind**: instance method of [<code>LPF2</code>](#LPF2)  
<a name="LPF2+event_discover"></a>

### "discover" (hub)
Emits when a LPF2 Hub device is found.

**Kind**: event emitted by [<code>LPF2</code>](#LPF2)  

| Param | Type |
| --- | --- |
| hub | [<code>Hub</code>](#Hub) | 

<a name="Hub"></a>

## Hub ⇐ <code>EventEmitter</code>
**Kind**: global class  
**Extends**: <code>EventEmitter</code>  

* [Hub](#Hub) ⇐ <code>EventEmitter</code>
    * [.connect([callback])](#Hub+connect)
    * [.subscribe(port, [mode])](#Hub+subscribe)
    * [.subscribe(port)](#Hub+subscribe)
    * [.connectCallback](#Hub+connectCallback) : <code>function</code>

<a name="Hub+connect"></a>

### hub.connect([callback])
Connect to the Hub.

**Kind**: instance method of [<code>Hub</code>](#Hub)  

| Param | Type |
| --- | --- |
| [callback] | [<code>connectCallback</code>](#Hub+connectCallback) | 

<a name="Hub+subscribe"></a>

### hub.subscribe(port, [mode])
Subscribe to sensor notifications on a given port.

**Kind**: instance method of [<code>Hub</code>](#Hub)  

| Param | Type | Default | Description |
| --- | --- | --- | --- |
| port | <code>string</code> |  |  |
| [mode] | <code>number</code> \| <code>boolean</code> | <code>false</code> | The sensor mode to activate. If no mode is provided, the default for that sensor will be chosen. |

<a name="Hub+subscribe"></a>

### hub.subscribe(port)
Unsubscribe to sensor notifications on a given port.

**Kind**: instance method of [<code>Hub</code>](#Hub)  

| Param | Type |
| --- | --- |
| port | <code>string</code> | 

<a name="Hub+connectCallback"></a>

### hub.connectCallback : <code>function</code>
**Kind**: instance typedef of [<code>Hub</code>](#Hub)  
<a name="WeDo2Hub"></a>

## WeDo2Hub ⇐ [<code>Hub</code>](#Hub)
**Kind**: global class  
**Extends**: [<code>Hub</code>](#Hub)  

* [WeDo2Hub](#WeDo2Hub) ⇐ [<code>Hub</code>](#Hub)
    * [.setLEDColor(color)](#WeDo2Hub+setLEDColor)
    * [.setLEDRGB(red, green, blue)](#WeDo2Hub+setLEDRGB)
    * [.setMotorSpeed(port, speed)](#WeDo2Hub+setMotorSpeed)
    * [.connect([callback])](#Hub+connect)
    * [.subscribe(port, [mode])](#Hub+subscribe)
    * [.connectCallback](#Hub+connectCallback) : <code>function</code>

<a name="WeDo2Hub+setLEDColor"></a>

### weDo2Hub.setLEDColor(color)
Set the color of the LED on the Hub via a color value.

**Kind**: instance method of [<code>WeDo2Hub</code>](#WeDo2Hub)  

| Param | Type | Description |
| --- | --- | --- |
| color | <code>number</code> | A number representing one of the LED color consts. |

<a name="WeDo2Hub+setLEDRGB"></a>

### weDo2Hub.setLEDRGB(red, green, blue)
Set the color of the LED on the Hub via RGB values.

**Kind**: instance method of [<code>WeDo2Hub</code>](#WeDo2Hub)  

| Param | Type |
| --- | --- |
| red | <code>number</code> | 
| green | <code>number</code> | 
| blue | <code>number</code> | 

<a name="WeDo2Hub+setMotorSpeed"></a>

### weDo2Hub.setMotorSpeed(port, speed)
Set the motor speed on a given port.

**Kind**: instance method of [<code>WeDo2Hub</code>](#WeDo2Hub)  

| Param | Type | Description |
| --- | --- | --- |
| port | <code>string</code> |  |
| speed | <code>number</code> | For forward, a value between 1 - 100 should be set. For reverse, a value between -1 to -100. Stop is 0. |

<a name="Hub+connect"></a>

### weDo2Hub.connect([callback])
Connect to the Hub.

**Kind**: instance method of [<code>WeDo2Hub</code>](#WeDo2Hub)  
**Overrides**: [<code>connect</code>](#Hub+connect)  

| Param | Type |
| --- | --- |
| [callback] | [<code>connectCallback</code>](#Hub+connectCallback) | 

<a name="Hub+subscribe"></a>

### weDo2Hub.subscribe(port, [mode])
Subscribe to sensor notifications on a given port.

**Kind**: instance method of [<code>WeDo2Hub</code>](#WeDo2Hub)  
**Overrides**: [<code>subscribe</code>](#Hub+subscribe)  

| Param | Type | Default | Description |
| --- | --- | --- | --- |
| port | <code>string</code> |  |  |
| [mode] | <code>number</code> \| <code>boolean</code> | <code>false</code> | The sensor mode to activate. If no mode is provided, the default for that sensor will be chosen. |

<a name="Hub+connectCallback"></a>

### weDo2Hub.connectCallback : <code>function</code>
**Kind**: instance typedef of [<code>WeDo2Hub</code>](#WeDo2Hub)  
<a name="BoostHub"></a>

## BoostHub ⇐ [<code>Hub</code>](#Hub)
**Kind**: global class  
**Extends**: [<code>Hub</code>](#Hub)  

* [BoostHub](#BoostHub) ⇐ [<code>Hub</code>](#Hub)
    * [.setLEDColor(color)](#BoostHub+setLEDColor)
    * [.setMotorSpeed(port, speed, [time])](#BoostHub+setMotorSpeed)
    * [.setMotorAngle(port, angle, [speed])](#BoostHub+setMotorAngle)
    * [.connect([callback])](#Hub+connect)
    * [.subscribe(port, [mode])](#Hub+subscribe)
    * [.connectCallback](#Hub+connectCallback) : <code>function</code>

<a name="BoostHub+setLEDColor"></a>

### boostHub.setLEDColor(color)
Set the color of the LED on the Hub via a color value.

**Kind**: instance method of [<code>BoostHub</code>](#BoostHub)  

| Param | Type | Description |
| --- | --- | --- |
| color | <code>number</code> | A number representing one of the LED color consts. |

<a name="BoostHub+setMotorSpeed"></a>

### boostHub.setMotorSpeed(port, speed, [time])
Set the motor speed on a given port.

**Kind**: instance method of [<code>BoostHub</code>](#BoostHub)  

| Param | Type | Description |
| --- | --- | --- |
| port | <code>string</code> |  |
| speed | <code>number</code> | For forward, a value between 1 - 100 should be set. For reverse, a value between -1 to -100. Stop is 0. |
| [time] | <code>number</code> | How long to activate the motor for (in milliseconds). Leave empty to turn the motor on indefinitely. |

<a name="BoostHub+setMotorAngle"></a>

### boostHub.setMotorAngle(port, angle, [speed])
Rotate a motor by a given angle.

**Kind**: instance method of [<code>BoostHub</code>](#BoostHub)  

| Param | Type | Default | Description |
| --- | --- | --- | --- |
| port | <code>string</code> |  |  |
| angle | <code>number</code> |  | How much the motor should be rotated (in degrees). |
| [speed] | <code>number</code> | <code>100</code> | How fast the motor should be rotated. |

<a name="Hub+connect"></a>

### boostHub.connect([callback])
Connect to the Hub.

**Kind**: instance method of [<code>BoostHub</code>](#BoostHub)  
**Overrides**: [<code>connect</code>](#Hub+connect)  

| Param | Type |
| --- | --- |
| [callback] | [<code>connectCallback</code>](#Hub+connectCallback) | 

<a name="Hub+subscribe"></a>

### boostHub.subscribe(port, [mode])
Subscribe to sensor notifications on a given port.

**Kind**: instance method of [<code>BoostHub</code>](#BoostHub)  
**Overrides**: [<code>subscribe</code>](#Hub+subscribe)  

| Param | Type | Default | Description |
| --- | --- | --- | --- |
| port | <code>string</code> |  |  |
| [mode] | <code>number</code> \| <code>boolean</code> | <code>false</code> | The sensor mode to activate. If no mode is provided, the default for that sensor will be chosen. |

<a name="Hub+connectCallback"></a>

### boostHub.connectCallback : <code>function</code>
**Kind**: instance typedef of [<code>BoostHub</code>](#BoostHub)  