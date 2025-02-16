# CommonSourceAmplifier

**Aim**
<p>To perform the DC, Transient, AC Analysis of a Common Source amplifier circuit using LTSpice and extract the associated parameters.</p>

**Components Required**
<p>TSMC 180nm NMOS transistor (CMOSN), a drain resistor and voltage sources(2).</p>

**Circuit Diagram**

**Given parameters**

**Length** :180nm<br>
**VDD** :1.8V<br>
**Power** :50uW<br>
**Threshold Voltage** :0.36V<br>
**Resistor** :1K<br>
**Supply Voltage** :1.8V<br>

**Procedure**
<p>1.Design the CS amplifier as per the circuit diagram using LTSpice.</p>
<p>2.Set the components values as per the given parameters.</p>
<p>3.Create a new folder and save the LTSpice file in this folder along with the library file</p>
<p>4.Calculate the drain current value for the given power=50uW.</p>

Power = VDD*I<sub>d</sub>
<p>I<sub>d</sub>= Power/Voltage<br>
                 = 50uW/1.8V<br>
                 = 27.78uA</p><br>
                
**DC Analysis**
<p>DC Analysis is done to check if the MOSFET is operating in the saturation region and to obtain the DC operation point.</p>

**Procedure**<br>
1.After setting up the circuit as per the circuit diagram, apply the dc voltage VDD=1.8V and Vgs=0.9V.<br>
2.Go to Simultae option in the tab and the DC opt option and click 'ok'.<br>
3.Click on run to run the circuit.<br>
4.DC operating point is obtained.<br>


                





