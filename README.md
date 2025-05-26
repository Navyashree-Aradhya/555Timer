# 555Timer
### 1. AIM
### Aim for Monostable Multivibrator Using 555 Timer IC:

To design and implement a monostable multivibrator circuit using a 555 Timer IC, and to observe the generation of a single output pulse of a specified duration in response to a trigger input.
### 2. THEORY
A monostable multivibrator is a circuit that has one stable state and one quasi-stable (temporary) state. When triggered externally, it temporarily switches to the quasi-stable state for a predetermined time and then returns to the stable state automatically.
The 555 Timer IC can be configured in monostable mode to produce a single output pulse in response to a trigger input.
The output pulse duration (T) is given by the formula:

*T = 1.1 x R x C*

Where:
- R = Resistance in ohms
- C = Capacitance in farads
- ### <ins>Key Features
- Accurate pulse generation (0.5ms) on each trigger.
- Ignores further triggers during pulse duration (non-retriggerable).
- Triggered externally using digital signals or another 555 timer in astable mode.
- Can be used in digital timing, pulse generation, and signal shaping applications
- ### 3. CIRCUIT DESIGN AND CALCULATION
![1](https://github.com/user-attachments/assets/bad65a9b-f731-4336-a1b5-0cd4d842c246)
#### Target pulse width:

*T = 0.5 ms*
Using the monostable formula:
*T = 1.1 x R x C*
Assuming:
- C = 1 µF
Then:
*R = T/1.1 x C = 454.54 Ω*
Selected values:
- R = 454.54 Ω
- C = 1 µF

These values yield a pulse duration of approximately 0.5 ms.
### 4. SIMULATION ANALYSIS
### <ins>Transient Analysis
Used to verify timing behaviour of the output signal in response to various trigger signals

### <ins>Procedure 
1. Open LTspice and create a new schematic.Set up the circuit as per the circuit diagram.
2. Select the Resistor (R) and Capacitor(C) as per the given specifcation.
3. Simulation Command
   - Go to **Simulate** -> *Edit Simulation Cmd*
   - Choose **Transient**, and set thime as needed per case.
   - ### 5. OUTPUT WAVEFORMS AND RESULTS
### <ins>Case 1: Properly Spaced Triggers
- Trigger Pulse Source:
  VTrig PULSE(5 0 0.05m 0 0 0.01m 2m)
  - This generates a falling edge every 2 ms (well spaced).

- Run the simulation for 10 ms
- ![Screenshot (117)](https://github.com/user-attachments/assets/d6000acf-b342-40b2-8b99-d3b3cd85ba6a)


