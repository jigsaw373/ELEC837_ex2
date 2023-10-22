## 1. Thyristor-Controlled Reactor (TCR)

### Waveform for $e = E \sin \omega t$

This is a sinusoidal waveform with a period of $T$. The waveform starts at zero, rises to a positive maximum at $t = T/4$, returns to zero at $t = T/2$, dips to a negative maximum at $t = 3T/4$, and then returns to zero at $t = T$. This cycle repeats.

### Current $i_1$ with delay angle $ \pi/2 < \alpha < \pi $

The current waveform will be delayed with respect to the voltage waveform by the firing angle $ \alpha $. The thyristor will start conducting at the firing angle and will turn off when the current waveform crosses zero. Given $ \pi/2 < \alpha < \pi $, the current will start conducting in the negative half-cycle of the voltage and turn off before the end of the negative half-cycle.

### Analytical expression for $i_1$

$$ i_1(t) = \frac{E \sin(\omega t)}{Z} $$

Where $Z$ is the impedance of the circuit. This expression is valid from $ \alpha $ to $ \pi $.

### Fourier series coefficients

$$ f(t) = a_0 + \sum_{n=1}^{\infty} [a_n \cos(n \omega t) + b_n \sin(n \omega t)] $$

Where:

$$ a_h = \frac{2}{T} \int_{0}^{T} f(t) \cos(h \omega t) dt $$

$$ b_h = \frac{2}{T} \int_{0}^{T} f(t) \sin(h \omega t) dt $$

---

## 2. Quadrature Booster (QB)

### Transferred Power and Reactive Power by QB

$$ P = \frac{V_p V_q}{X} \sin(\delta) $$

Where:
- $ V_p $ and $ V_q $ are the magnitudes of the voltages at the terminals p and q, respectively.
- $ X $ is the reactance between the terminals.
- $ \delta $ is the phase difference between the two terminal voltages.

The reactive power supplied by the QB:

$$ Q_{QB} = V_{pq} \cdot I - \frac{V_p^2}{X} \cos(\delta) $$

---

## 3. Static Var Compensator (SVC)

### Circuit Diagram

```
                              +------+
                              |      |
        +----+ TCR    +----+   | SVC  |   +----+
       -|----|-//////-|----|-  |      |  -|----|-
    AC |    |        |    |   +------+   |    | AC
Supply |    | TSC    |    |               |    | Supply
       +----+        +----+               +----+
```

### TSC Control

The Thyristor-Switched Capacitor (TSC) is controlled by firing the thyristor to connect or disconnect the capacitor to the system.

### TCR Control

The Thyristor-Controlled Reactor (TCR) works by controlling the firing angle of the thyristors, which controls the amount of time the reactor is connected to the system during each cycle.

---

## 4. Thyristor-Controlled Series Capacitor (TCSC)

### Circuit Diagram

```
         +-----||------+------/\/\------+
         |       C            L          |
   -----+-------------------------------+-----
         |                            Thyristor
         +------------------------------+
```

### Three Different Modes of Operation

- **Blocking Mode**: The thyristor remains off for the entire period.
- **Bypass Mode**: The thyristor is turned on for the entire period.
- **Vernier Mode**: By controlling the firing angle ($\alpha$) of the thyristor, the effective reactance of the TCSC can be controlled.

### Impedance Calculation

$$ Z_{TCSC} = \frac{jX_C * jX_L}{jX_C + jX_L} $$

Where:
- $ X_C $ is the reactance of the capacitor: $ \frac{1}{\omega C} $
- $ X_L $ is the reactance of the inductor: $ \omega L $

---

I hope this fits your requirements! If any further modifications are needed, please let me know.