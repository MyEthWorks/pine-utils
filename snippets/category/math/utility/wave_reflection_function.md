# Function to generate Wave Reflection Wave.

#### Description:

Function to generate Wave Reflection Wave.

##### References:
* [noreference](/ "no reference.")


#### Code:

<details open>
  <!-- leave a blank line after summary -->
  <summary>@version=4</summary>

```javascript
f_wave_reflection(_wave_duration, _m)=>
    _pi = 3.14159265359
    _w = 2 * _pi / _wave_duration
    _r = 1 - abs(sin(_w * float(bar_index) ) - _m)
    if _r < -1.0
        _r := _r + (-1.0 - _r) * 2
    if _r > +1.0
        _r := _r + (+1.0 - _r) * 2
    _r
```

</details>


<!-- Add example bellow: --------------------------------------------------------------->
#### Example:


Generate a Wave Reflection Wave: <br/>

<details open>
  <!-- leave a blank line after summary -->
  <summary>Example Code</summary>

<!--  -->
<!-- code goes between the backticks: -->
```javascript
//@version=4
study(title="[RS]Function - Wave and Cycle Functions", overlay=false)
int length = 100

f_wave_reflection(_wave_duration, _m)=>
    _pi = 3.14159265359
    _w = 2 * _pi / _wave_duration
    _r = 1 - abs(sin(_w * float(bar_index) ) - _m)
    if _r < -1.0
        _r := _r + (-1.0 - _r) * 2
    if _r > +1.0
        _r := _r + (+1.0 - _r) * 2
    _r

wave_reflection1 = f_wave_reflection(length, 0.5)
wave_reflection2 = f_wave_reflection(length, input(0.618))

plot(series=wave_reflection1, title="Reflection1", color=color.red)
plot(series=wave_reflection2, title="Reflection2", color=color.blue)
```
</details>

##### Code Author(s):
  * ##### [Ricardo Santos](https://www.tradingview.com/u/RicardoSantos/ "@Tradingview.") 

<br/>
<br/>
<br/>

[Disclaimer](/./DISCLAIMER.md "Disclaimer.")<br/>
[License](/./LICENSE "License.")
