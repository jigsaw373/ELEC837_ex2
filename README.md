## 1. Fig. 1 shows a Thyristor-Controlled Reactor (TCR) connected to an ideal sinusoidal voltage source e.
Let's break down your request step by step:

1. **Sketch the waveform for \(e = E \sin \omega t\)**:

This is simply a sinusoidal waveform with a period of \(T\). The waveform will start at zero, rise to a positive maximum at \(t = T/4\), return to zero at \(t = T/2\), dip to a negative maximum at \(t = 3T/4\), and then return to zero at \(t = T\). This cycle will repeat.

2. **Sketch the waveform for current \(i_1\) when the delay angle for firing the thyristor is \( \pi/2 < \alpha < \pi \)**:

The current waveform will be delayed with respect to the voltage waveform by the firing angle \( \alpha \). The thyristor will start conducting at the firing angle and will turn off when the current waveform crosses zero. Given \( \pi/2 < \alpha < \pi \), the current will start conducting in the negative half-cycle of the voltage and turn off before the end of the negative half-cycle.

3. **Analytical expression for current \(i_1\) during the conduction interval**:

The analytical expression for the current during the conduction interval can be obtained using Ohm's and Kirchhoff's laws:

\[ i_1(t) = \frac{E \sin(\omega t)}{Z} \]

Where:
- \(Z\) is the impedance of the circuit.
- The above expression is valid for \( \alpha \) to \( \pi \).

4. **Fourier series coefficients for the hth harmonic**:

The Fourier series for any function can be represented as:

\[ f(t) = a_0 + \sum_{n=1}^{\infty} [a_n \cos(n \omega t) + b_n \sin(n \omega t)] \]

The coefficients \( a_h \) and \( b_h \) can be found using:

\[ a_h = \frac{2}{T} \int_{0}^{T} f(t) \cos(h \omega t) dt \]

\[ b_h = \frac{2}{T} \int_{0}^{T} f(t) \sin(h \omega t) dt \]

5. **Fourier series coefficients for the fundamental component**:

The fundamental component is the \( h = 1 \) harmonic. Simply plug in \( h = 1 \) into the above formulas to get the Fourier coefficients for the fundamental component.

6. **Plot of Fourier coefficients vs. \( \beta \) for \( h=1,3,5,7,9,11 \)**:

\( \beta = \pi - \alpha \). The plots will showcase how the Fourier coefficients vary with the firing angle. You'll see the magnitude of harmonics decreasing as \( h \) increases.

Note: It is beyond the scope of this platform to actually sketch and plot the waveforms. You would typically use specialized software or graph paper for this. The above steps are to guide you on how to do it. If you require the mathematical derivation or any further explanation on any part, do let me know!

## 2.	In Fig. 2 the angle of phasor  relative to the phasor   is stipulated to be fixed at  , the phase shifter is known as a Quadrature Booster (QB). Find the transferred power and the reactive power supplied by the QB, and 

Alright, this is a comprehensive set of questions related to a Quadrature Booster (QB). Let's tackle each of them step by step.

**1. Transferred Power and Reactive Power by QB**:

The power transferred between the two ends can be expressed as:
\[ P = \frac{V_p V_q}{X} \sin(\delta) \]
Where:
- \( V_p \) and \( V_q \) are the magnitudes of the voltages at the terminals p and q, respectively.
- \( X \) is the reactance between the terminals.
- \( \delta \) is the phase difference between the two terminal voltages.

The QB does not influence the real power transfer but only influences the reactive power transfer. Therefore, the reactive power supplied by the QB can be defined as:
\[ Q_{QB} = V_{pq} \cdot I - \frac{V_p^2}{X} \cos(\delta) \]
Where:
- \( V_{pq} \) is the voltage introduced by the QB.
- \( I \) is the current through the line.

**2. V.A rating of the 3-phase QB**:

The apparent power or V.A rating for the QB in a 3-phase system can be given by:
\[ S_{QB} = \sqrt{3} \times V_{pq} \times I \]
Where \( V_{pq} \) is the maximum voltage the QB can introduce and \( I \) is the line current.

**3. Phasor Diagram**:

For positive \( V_{pq} \), the QB boosts the voltage while for negative \( V_{pq} \), it reduces the voltage. When drawing the phasor diagram, consider:
- The reference phasor, usually \( V_p \).
- The resultant voltage phasor, \( V_q \), which will be at an angle \( \delta \) to \( V_p \).
- The QB voltage \( V_{pq} \) which is in quadrature to the line current phasor.

**4. Power Transfer Curve**:

The curve is a sinusoidal representation with respect to the angle \( \delta \) showing the variation of power with the phase angle. A QB, by varying \( V_{pq} \), can change the voltage profile and thereby influence the reactive power in the system. By managing the reactive power, the QB can enhance the transient stability, ensuring that the system returns to stable operation following a disturbance.

**5. Selection of \( V_{max} \)**:

The maximum voltage \( V_{max} \) is chosen based on the requirement to control the power flow and the design and insulation limits of the equipment.

**6. Power Structure of a QB**:

A QB built using three-phase transformers consists of a main transformer and an auxiliary transformer. The main transformer carries the line current, while the auxiliary transformer introduces the voltage \( V_{pq} \).

**7. Control of Series Voltage**:

The series voltage \( V_{pq} \) in a QB can be controlled by varying the turns ratio of the auxiliary transformer or by using power electronics-based approaches, such as a series-connected Voltage Source Converter (VSC).

It's important to note that while I provided a general explanation, a detailed analysis, especially the drawings, would require specialized software or tools. If you need more in-depth explanations or mathematical derivations on any aspect, please let me know!

## 3. Static Var Compensator (SVC) Circuit Diagram:
An SVC typically consists of a combination of capacitors (TSC) and reactors (TCR) that are controlled by thyristors. 
```
                              +------+
                              |      |
        +----+ TCR    +----+   | SVC  |   +----+
       -|----|-//////-|----|-  |      |  -|----|-
    AC |    |        |    |   +------+   |    | AC
Supply |    | TSC    |    |               |    | Supply
       +----+        +----+               +----+
```

## a) TSC Control:
The Thyristor-Switched Capacitor (TSC) is controlled by firing the thyristor to connect or disconnect the capacitor to the system.

### Control System:
1. **Reference Setting**: This is the desired VAR setting based on system requirements.
2. **Measurement System**: Measures the system voltage, current, or reactive power.
3. **Comparison**: The reference and measurement are compared.
4. **Control Signal**: Based on the comparison, a control signal is generated to turn on/off the thyristor.
5. **Thyristor Gate Control**: Controls the firing angle of the thyristor.

## b) TCR Control:
The Thyristor-Controlled Reactor (TCR) works by controlling the firing angle of the thyristors, which controls the amount of time the reactor is connected to the system during each cycle.

### Control System:
1. **Reference Setting**: Desired VAR setting.
2. **Measurement System**: Measures system parameters.
3. **Comparison**: Compares reference with measurement.
4. **Control Signal**: Based on the error, a control signal is generated to adjust the firing angle.
5. **Thyristor Firing Control**: Adjusts the firing angle of the thyristor.

## c) 5 TSC branches:
To control 1 per-unit capacitive reactive power continuously, you would divide the total power by the number of branches. If total capacitive reactive power is `Q`, then each branch will be `Q/5`.

## d) Qout vs. Qdemand:
Typically, the Qout vs. Qdemand curve is linear in both capacitive and inductive ranges. There's a dead zone around zero where no compensation occurs.

## e) TCR Power Rating:
The power rating of the TCR branch should be a bit higher than the power rating of the TSC branches because it provides continuous adjustability and needs to compensate for system inductance and also for situations where full TSC compensation isn't sufficient.

## f) SVC Response Time:
A three-phase SVC typically responds very quickly to control commands, often within a few milliseconds.

## g) Adding Damping:
To add damping to the power system using SVC, a supplementary damping control can be added to the SVC control system. This can be achieved by adding a feedback loop in the control system that measures system oscillations and modulates the SVC output to dampen these oscillations.

For the SVC control system:
1. **Damping Controller**: Measures the system oscillations.
2. **Modulation Signal**: Based on the oscillations, a modulation signal is generated.
3. **Integration**: This signal is integrated with the SVC control signal to modulate the SVC output.

Note: While I've provided descriptions and basic diagrams in text format, actual circuit diagrams would require specialized software or graphics tools. If you need a detailed graphical representation, consider using tools like MATLAB/Simulink, PSCAD, or other power system analysis software.


## 4.	Draw the circuit diagram of a Thristor-Controlled Series Capacitor (TCSC).

Certainly! Let's address your questions step by step:

1. **Thyristor-Controlled Series Capacitor (TCSC) Circuit Diagram**:
   A TCSC consists of a series capacitor (C) in parallel with a thyristor-controlled reactor (TCR). The TCR is essentially a combination of an inductor (L) and a thyristor valve.

```
         +-----||------+------/\/\------+
         |       C            L          |
   -----+-------------------------------+-----
         |                            Thyristor
         +------------------------------+
```

2. **Three Different Modes of Operation**:

   a. **Blocking Mode**: In this mode, the thyristor remains off for the entire period. Thus, the TCSC acts as a pure capacitor, providing maximum capacitive compensation.

   b. **Bypass Mode**: In this mode, the thyristor is turned on for the entire period, essentially bypassing the capacitor. The TCSC provides no compensation in this mode.

   c. **Vernier Mode**: This mode provides a variable compensation. By controlling the firing angle (α) of the thyristor, the effective reactance of the TCSC can be controlled. The TCSC can act as a capacitor, inductor, or any reactance value in between based on the firing angle.

3. **Vernier Mode Explanation**: The vernier mode offers variable compensation. It is named the "vernier" mode because it allows fine adjustments to the compensation level, similar to the fine adjustments made using a vernier scale in measurement instruments.

4. **Impedance Calculation**: The impedance of the TCSC can be given by:
   
   \[ Z_{TCSC} = \frac{jX_C * jX_L}{jX_C + jX_L} \]

   Where:
   - \( X_C \) is the reactance of the capacitor: \( \frac{1}{\omega C} \)
   - \( X_L \) is the reactance of the inductor: \( \omega L \)

   The exact impedance value in each mode depends on the firing angle (α).

5. **XTSC as a function of β (β=π-α)**:
   
   The reactance \( XTSC \) is a function of the firing angle and can be represented graphically with β on the x-axis and reactance on the y-axis. The reactance starts from maximum capacitive value in blocking mode and moves to an inductive value in bypass mode. The exact shape depends on the values of C and L.

6. **Benefits of TCSC over Simple Series Capacitive Compensation**:
   
   a. **Variable Compensation**: Unlike a fixed capacitor, TCSC offers dynamic and variable compensation.
   
   b. **Enhanced System Stability**: Helps in damping power oscillations and improves transient stability.
   
   c. **Improved Voltage Regulation**: Provides better voltage profile during varying load conditions.
   
   d. **Mitigation of Transmission Bottlenecks**: TCSC can increase the power transfer capability of a transmission line.

7. **Subsynchronous Resonance (SSR) Problem with TCSC**:
   
   Yes, TCSC can introduce or exacerbate subsynchronous resonance problems. SSR is a phenomenon where certain components, like turbines, resonate with electrical system frequencies below the system's fundamental frequency. The TCSC can interact with the natural frequencies of a turbine-generator, potentially causing harmful oscillations. Proper design and controls must be in place to mitigate such effects.