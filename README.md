# JKFLIPFLOP USING IF-ELSE

## NAME:- JAIYANTAN S
## REG_NO:- 212224100021

**AIM:** 

To implement  JK flipflop using verilog and validating their functionality using their functional tables

**SOFTWARE REQUIRED:**

Quartus prime

**THEORY**

**JK Flip-Flop**

JK flip-flop is the modified version of SR flip-flop. It operates with only positive clock transitions or negative clock transitions. The circuit diagram of JK flip-flop is shown in the following figure.

![image](https://github.com/naavaneetha/JKFLIPFLOP-USING-IF-ELSE/assets/154305477/a649c30b-232b-4558-b188-fd6c09845180)


This circuit has two inputs J & K and two outputs Qtt & Qtt’. The operation of JK flip-flop is similar to SR flip-flop. Here, we considered the inputs of SR flip-flop as S = J Qtt’ and R = KQtt in order to utilize the modified SR flip-flop for 4 combinations of inputs. The following table shows the state table of JK flip-flop.

![image](https://github.com/naavaneetha/JKFLIPFLOP-USING-IF-ELSE/assets/154305477/c4360742-e8a8-4937-b089-c46c0433f9a3)

 
Here, Qtt & Qt+1t+1 are present state & next state respectively. So, JK flip-flop can be used for one of these four functions such as Hold, Reset, Set & Complement of present state based on the input conditions, when positive transition of clock signal is applied. The following table shows the characteristic table of JK flip-flop. Present Inputs Present State Next State
 
![image](https://github.com/naavaneetha/JKFLIPFLOP-USING-IF-ELSE/assets/154305477/6c275261-a6d5-4c37-a3a7-1e88ca11c4cd)

By using three variable K-Map, we can get the simplified expression for next state, Qt+1t+1. Three variable K-Map for next state, Qt+1t+1 is shown in the following figure.
 
![image](https://github.com/naavaneetha/JKFLIPFLOP-USING-IF-ELSE/assets/154305477/5174f41b-0ce0-4329-a372-6d1943ea6673)

The maximum possible groupings of adjacent ones are already shown in the figure. Therefore, the simplified expression for next state Qt+1t+1 is Q(t+1)=JQ(t)′+K′Q(t)Q(t+1)=JQ(t)′+K′Q(t)

**Procedure**

1. Type the program in Quartus software.

2. Compile and run the program.

3. Generate the RTL schematic and save the logic diagram.

4. Create nodes for inputs and outputs to generate the timing diagram.

5. For different input combinations generate the timing diagram.

**PROGRAM**

## Developed by : Jaiyantan S
## Reg_no: 212224100021

```python
module exp7(q,qb,j,k,clk);
input j,k,clk;
output reg q;
output qb;
always @(posedge(clk))
begin 
    q<=(j&(~q)) | ((~k)&q);
end 
assign qb=(~q);
endmodule
```
**TRUTH TABLE**
![437953472-428a98b4-f32d-4c72-940f-6e9af621e7c7](https://github.com/user-attachments/assets/6903556d-0d3b-4915-b7c7-d0eed401e160)


**RTL LOGIC FOR FLIPFLOPS**

![437953573-b43c883e-5bc7-4810-a01c-729ca24fc214](https://github.com/user-attachments/assets/f1718562-cb34-4c9b-b34f-4d0793eb6381)


**WAVEFORM**
![437953629-a12cc994-9d51-4089-86af-6155f5528840](https://github.com/user-attachments/assets/5ab3d1ea-b255-4e37-b4b0-094517204436)

**RESULTS**

Thus the given JK flipflops are implemented using and their operations are verified using Verilog programming

