# Function to generate Round Sawtooth Wave.

#### Description:

Function to generate Round Sawtooth Wave.

##### References:
* [noreference](/ "no reference.")


#### Code:

<details open>
  <!-- leave a blank line after summary -->
  <summary>@version=4</summary>

```javascript
f_wave_round_sawtooth(_wave_duration)=>
    _r = 1.0 - (2.0 / (float(bar_index) % _wave_duration))
    _r := na(_r) ? 1 : _r
```

</details>


<!-- Add example bellow: --------------------------------------------------------------->
#### Example:


Generate a Round Sawtooth Wave: <br/>

<details open>
  <!-- leave a blank line after summary -->
  <summary>Example Code</summary>

<!--  -->
<!-- code goes between the backticks: -->
```javascript
//@version=4
study(title="[RS]Function - Wave and Cycle Functions", overlay=false)
int length = 100

f_wave_round_sawtooth(_wave_duration)=>
    _r = 1.0 - (2.0 / (float(bar_index) % _wave_duration))
    _r := na(_r) ? 1 : _r

float wave = f_wave_round_sawtooth(length)

plot(series=wave, title="Round Sawtooth", color=color.black)
```
</details>

##### Code Author(s):
  * ##### [Ricardo Santos](https://www.tradingview.com/u/RicardoSantos/ "@Tradingview.") 

<br/>
<br/>
<br/>

[Disclaimer](/./DISCLAIMER.md "Disclaimer.")<br/>
[License](/./LICENSE "License.")
