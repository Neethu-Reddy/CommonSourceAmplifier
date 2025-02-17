# CommonSourceAmplifier
## Circuit 1

**Aim**
<p>To perform the DC, Transient, AC Analysis of a Common Source amplifier circuit using LTSpice and extract the associated parameters.</p>

**Components Required**
<p>TSMC 180nm NMOS transistor (CMOSN), a drain resistor and voltage sources(2).</p>

**Circuit Diagram**

![image](https://github.com/user-attachments/assets/73aaa79e-0a39-4354-8a70-12257f968516)

**Given parameters :**

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
  <td>480nm</td>
  <td>2.738A</td>
</tr>
</table>

**Transient Analysis**<br>
1.Apply a sine wave input of frequency 1KHz and amplitude 50mV and Vgs=0.9V.<br>
2.Go to simulate option in the tab and click on transient analysis and enter the stop time as 5ms(.tans 5ms).<br>
3.Run the circuit and observe the response of the circuit to a time varying signal.<br>

![image](https://github.com/user-attachments/assets/0284b9c3-0453-45bb-8ce5-8296d806765f)


**AC Analysis**<br>
1.Go to simulate option and click on AC analysis and enter the time of sweep as decade, no. of points as 20, frequency 0.1Hz-1THz.<br>
2.Click ok and run the circuit to obtain the gain and frequency response of the circuit.<br>

![image](https://github.com/user-attachments/assets/29dac24a-713f-4c72-8164-21d91f6129a4)


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

![image](https://github.com/user-attachments/assets/9db60f72-feb8-4a21-a998-5fe943e85111)

I<sub>d</sub> = 27.78uA<br>
V<sub>DS</sub> = 1.77V<br>
Q-Point : (1.77V, 27.78uA) for length 500nm and width 480nm.<br>

**Transient Analysis**

![image](https://github.com/user-attachments/assets/3d1851ea-acdd-43aa-a400-e0821cb694e6)

Vout=1.7V<br>
We can observe 180degree phase shift between i/p and o/p signals.<br>

**AC Analysis**

![image](https://github.com/user-attachments/assets/ad524e72-e1b1-466c-bd8a-e2782763901d)

Gain = -20dB

**Inference**

**DC Analysis**<br>
Current directly depends on the width of the MOSFET.Current varies with the width of the MOSFET.<br>
Variation in I<sub>d</sub> is due to the channel length modulation.<br>
If I<sub>d</sub> is too low, we need to increase W for proper biasing.

**Transient Analysis**<br>
Analysis used to determine the signal distortion, DC shift between input and output and signal amplification.<br>
Vds needs to be checked to ensure saturation if distortion occurs.<br>
Increase in gain if there is low amplitude output.

**AC Analysis**<br>
Small signal analysis of the circuit to determine the gain of the circuit.<br>
We observe that there is low gain due to low value of gm and rd.Increase gm and Rd to increase gain of the circuit.


## Circuit 2

**Aim**
<p>To perform the DC, Transient, AC Analysis of a Common Source amplifier circuit using LTSpice and extract the associated parameters.</p>

**Components Required**
<p>TSMC 180nm NMOS transistor (CMOSN),PMOS transistor(PMOSN) and voltage sources(2).</p>

**Circuit Diagram**

![image](https://github.com/user-attachments/assets/a2d884f8-391a-4ecd-978e-45d2188c39e7)

**Given parameters :**

**Length** :180nm<br>
**V<sub>DD</sub>** :1.8V<br>
**Power** :50uW<br>

**Procedure**
<p>1.Design the CS amplifier as per the circuit diagram using LTSpice.</p>
<p>2.Set the components values as per the given parameters.</p>
<p>3.Create a new folder and save the LTSpice file in this folder along with the library file</p>
<p>4.Calculate the drain current value for the given power=50uW.</p>

**DC Analysis**

**Procedure**<br>
1.After setting up the circuit as per the circuit diagram, apply the dc voltage VDD=1.8V and Vgs=0.7V.<br>
2.Go to Simultae option in the tab and the DC opt option and click 'ok'.<br>
3.Do the trail and error method to get the appropriate biasing point by adjusting the width and length of the PMOS and NMOS. Click on run to run the circuit.<br>
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
  <td>22.72uA</td>
</tr>
<tr>
  <td>180nm</td>
  <td>2um</td>
  <td>54.45uA</td>
</tr>
<tr>
  <td></td>
  <td></td>
  <td></td>
</tr>
<tr>
  <td></td>
  <td></td>
  <td></td>
</tr>
</table>

**Transient Analysis**<br>
1.Apply a sine wave input of frequency 1KHz and amplitude 50mV and Vgs=0.7V.<br>
2.Go to simulate option in the tab and click on transient analysis and enter the stop time as 5ms(.tans 5ms).<br>
3.Run the circuit and observe the response of the circuit to a time varying signal.<br>

**AC Analysis**<br>
1.Go to simulate option and click on AC analysis and enter the time of sweep as decade, no. of points as 20, frequency 0.1Hz-1THz.<br>
2.Click ok and run the circuit to obtain the gain and frequency response of the circuit.<br>























                            
                                     





