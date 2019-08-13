# Function to generate Square Wave.

#### Description:

Function to generate Square Wave.

##### References:
* [noreference](/ "no reference.")


#### Code:

<details open>
  <!-- leave a blank line after summary -->
  <summary>@version=4</summary>

```javascript
f_wave_square(_wave_duration)=>
    _pi = 3.14159265359
    _w = 2 * _pi / _wave_duration
    _r = sign(2 * sin(_w * float(bar_index)))
```

</details>


<!-- Add example bellow: --------------------------------------------------------------->
#### Example:


Generate a Square Wave: <br/>

<details open>
  <!-- leave a blank line after summary -->
  <summary>Example Code</summary>

<!--  -->
<!-- code goes between the backticks: -->
```javascript
//@version=4
study(title="[RS]Function - Wave and Cycle Functions", overlay=false)
int length = 100

f_wave_square(_wave_duration)=>
    _pi = 3.14159265359
    _w = 2 * _pi / _wave_duration
    _r = sign(2 * sin(_w * float(bar_index)))

float wave = f_wave_square(length)

plot(series=wave, title="Square", color=color.black)
```
</details>

##### Code Author(s):
  * ##### [Ricardo Santos](https://www.tradingview.com/u/RicardoSantos/ "@Tradingview.") 

<br/>
<br/>
<br/>

[Disclaimer](/./DISCLAIMER.md "Disclaimer.")<br/>
[License](/./LICENSE "License.")
