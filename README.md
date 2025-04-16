### Name: V Rakshita
### Reg no: 212224100049

# EXP 7 - JK FLIPFLOP

## **AIM:** 

To implement  JK flipflop using verilog and validating their functionality using their functional tables

## **SOFTWARE REQUIRED:**

Quartus prime

## **THEORY**

### **JK Flip-Flop**

JK flip-flop is the modified version of SR flip-flop. It operates with only positive clock transitions or negative clock transitions. The circuit diagram of JK flip-flop is shown in the following figure.

![image](https://github.com/naavaneetha/JKFLIPFLOP-USING-IF-ELSE/assets/154305477/a649c30b-232b-4558-b188-fd6c09845180)


This circuit has two inputs J & K and two outputs Qtt & Qtt’. The operation of JK flip-flop is similar to SR flip-flop. Here, we considered the inputs of SR flip-flop as S = J Qtt’ and R = KQtt in order to utilize the modified SR flip-flop for 4 combinations of inputs. The following table shows the state table of JK flip-flop.

![image](https://github.com/naavaneetha/JKFLIPFLOP-USING-IF-ELSE/assets/154305477/c4360742-e8a8-4937-b089-c46c0433f9a3)

 
Here, Qtt & Qt+1t+1 are present state & next state respectively. So, JK flip-flop can be used for one of these four functions such as Hold, Reset, Set & Complement of present state based on the input conditions, when positive transition of clock signal is applied. The following table shows the characteristic table of JK flip-flop. Present Inputs Present State Next State
 
![image](https://github.com/naavaneetha/JKFLIPFLOP-USING-IF-ELSE/assets/154305477/6c275261-a6d5-4c37-a3a7-1e88ca11c4cd)

By using three variable K-Map, we can get the simplified expression for next state, Qt+1t+1. Three variable K-Map for next state, Qt+1t+1 is shown in the following figure.
 
![image](https://github.com/naavaneetha/JKFLIPFLOP-USING-IF-ELSE/assets/154305477/5174f41b-0ce0-4329-a372-6d1943ea6673)

The maximum possible groupings of adjacent ones are already shown in the figure. Therefore, the simplified expression for next state Qt+1t+1 is Q(t+1)=JQ(t)′+K′Q(t)Q(t+1)=JQ(t)′+K′Q(t)

## **PROCEDURE**

1.	Open Quartus and go to File -> New Project Wizard to create a new project. 

2.	Then, Go to File -> New -> Verilog HDL File and type the program. Compile and run the program.

3.	Then go to Tools -> NetList Viewers -> RTL Viewer and generate the RTL schematic and save the logic diagram.

4.	Then go to File -> New -> University program VWF. Create nodes for inputs and outputs to generate the timing diagram.

5.	Give different input combinations and go to Run Functional Simulation to generate the timing diagram.

## **PROGRAM**
```
module JKFLIPFLOP(j,k,q,qb,clock);
input j,k,clock;
output reg q;
output qb;
always @ (posedge(clock))
begin
	q<=(j &(~q)) | ((~k) & q);
end
assign qb = ~q;
endmodule
```

## **EXCITATION TABLE AND LOGIC DIAGRAM:**

![Screenshot (250)](https://github.com/user-attachments/assets/1c1a4633-bebd-47ce-bd01-b218d796a4a8)

![Screenshot (245)](https://github.com/user-attachments/assets/4b3fc9e8-00d6-4f5f-a280-4be85c992115)

## **WAVEFORM**

![Screenshot (248)](https://github.com/user-attachments/assets/6763616c-ae70-4e67-8c8f-0bfc7e850bb6)

## **RESULT**

JK flipflop has been implemented and their functionality has been validated using verilog.
