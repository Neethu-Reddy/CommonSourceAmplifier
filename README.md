# CommonSourceAmplifier

**Aim**
<p>To perform the DC, Transient, AC Analysis of a Common Source amplifier circuit using LTSpice and extract the associated parameters.</p>

**Components Required**
<p>TSMC 180nm NMOS transistor (CMOSN), a drain resistor and voltage sources(2).</p>

**Circuit Diagram**

**Given parameters**

**Length** :180nm<br>
**V<sub>DD</sub>** :1.8V<br>
**Power** :50uW<br>
**Threshold Voltage** :0.36V<br>
**Resistor** :1K<br>
**Supply Voltage** :1.8V<br>

**Procedure**
<p>1.Design the CS amplifier as per the circuit diagram using LTSpice.</p>
<p>2.Set the components values as per the given parameters.</p>
<p>3.Create a new folder and save the LTSpice file in this folder along with the library file</p>
<p>4.Calculate the drain current value for the given power=50uW.</p>

                
**DC Analysis**
<p>DC Analysis is done to check if the MOSFET is operating in the saturation region and to obtain the DC operation point.</p>

**Procedure**<br>
1.After setting up the circuit as per the circuit diagram, apply the dc voltage VDD=1.8V and Vgs=0.9V.<br>
2.Go to Simultae option in the tab and the DC opt option and click 'ok'.<br>
3.Click on run to run the circuit.<br>
4.DC operating point is obtained.<br>

**Tabular Column**
<table>
<tr>
  <td>Length</td>
  <td>Width</td>
  <td>I<sub>d</sub></td>
</tr>
<tr>
  <td>180nm</td>
  <td>1um</td>
  <td>0.152mA</td>
</tr>
<tr>
  <td>180nm</td>
  <td>2um</td>
  <td>0.275mA</td>
</tr>
<tr>
  <td>1um</td>
  <td>1um</td>
  <td>2.855A</td>
</tr>
<tr>
  <td>500nm</td>
  <td>500nm</td>
  <td>2.836A</td>
</tr>
</table>

**Transient Analysis**<br>
1.Apply a sine wave input of frequency 1KHz and amplitude 50mV and Vgs=0.9V.<br>
2.Go to simulate option in the tab and click on transient analysis and enter the stop time as 5ms(.tans 5ms).<br>
3.Run the circuit and observe the response of the circuit to a time varying signal.<br>

**AC Analysis**<br>
1.Go to simulate option and click on AC analysis and enter the time of sweep as decade, no. of points as 20, frequency 0.1Hz-1THz.<br>
2.Click ok and run the circuit to obtain the gain and frequency response of the circuit.<br>

**Calculation**

Power = V<sub>DD</sub>*I<sub>d</sub>
<p>I<sub>d</sub>= Power/Voltage<br>
                 = 50uW/1.8V<br>
                 = 27.78uA</p><br>

Loop equation of the above circuit:<br>
V<sub>DD</sub> = V<sub>DS</sub> + I<sub>d</sub>*R<sub>d</sub><br>
1.8 = V<sub>DS</sub> + 27.78uA*1K<br>
V<sub>DS</sub> = 1.8 - 0.027<br>
V<sub>DS</sub> = 1.77V<br>

Therefore, the operation point (V<sub>DS</sub>,I<sub>d</sub>) = (1.77V,27.7uA)

Gain = -gm*R<sub>d</sub><br>
gm = 2I<sub>d</sub>/V<sub>OV</sub><br>
gm = 55.56uA/0.54<br>
gm = 0.10mS<br>

Therefore A<sub>v</sub> = -0.1

**Result**

**DC Analysis**

I<sub>d</sub> = 27.78uA<br>
V<sub>DS</sub> = 1.77V<br>
Q-Point : (1.77V, 27.78uA)<br>

**Transient Analysis**

Vout=1.7V<br>
We can observe 180degree phase shift between i/p and o/p signals.<br>

**AC Analysis**

Gain = -20dB

**Inference**









                            
                                     





