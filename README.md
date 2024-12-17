# T-FLIPFLOP-POSEDGE

**AIM:**

To implement  T flipflop using verilog and validating their functionality using their functional tables

**SOFTWARE REQUIRED:**

Quartus prime

**THEORY**

**T Flip-Flop**

T flip-flop is the simplified version of JK flip-flop. It is obtained by connecting the same input ‘T’ to both inputs of JK flip-flop. It operates with only positive clock transitions or negative clock transitions. The circuit diagram of T flip-flop is shown in the following figure.

![Screenshot 2024-12-17 141841](https://github.com/user-attachments/assets/919d41e8-1862-4a20-9271-2a85cda9db54)

 
This circuit has single input T and two outputs Qtt & Qtt’. The operation of T flip-flop is same as that of JK flip-flop. Here, we considered the inputs of JK flip-flop as J = T and K = T in order to utilize the modified JK flip-flop for 2 combinations of inputs. So, we eliminated the other two combinations of J & K, for which those two values are complement to each other in T flip-flop. The following table shows the state table of T flip-flop.

Here, Qtt & Qt+1t+1 are present state & next state respectively. So, T flip-flop can be used for one of these two functions such as Hold, & Complement of present state based on the input conditions, when positive transition of clock signal is applied. The following table shows the characteristic table of T flip-flop. Inputs Present State Next State

![Screenshot 2024-12-17 142256](https://github.com/user-attachments/assets/93140136-6d71-4d40-af33-02bec05af0d8)

 
From the above characteristic table, we can directly write the next state equation as Q(t+1)=T′Q(t)+TQ(t)′ ⇒Q(t+1)=T⊕Q(t)

**Procedure**

1.Type the program in Quartus software. 

2.Compile and run the program. 

3.Generate the RTL schematic and save the logic diagram. 

4.Create nodes for inputs and outputs to generate the timing diagram. 

5.For different input combinations generate the timing diagram.


**PROGRAM**

/* Program for flipflops and verify its truth table in quartus using Verilog programming. 

Developed by:  Dinesh.V

RegisterNumber: 24010667
```
module tflipflop(t, clk, rst, q);
  input t, clk, rst;
  output reg q;

  always @(posedge clk or posedge rst) 
begin
    if (rst)
      q <= 0; // Reset the flip-flop
    else if (t==0)
      q <= q; 
     else
        q<=~q;
  end
endmodule
```
**RTL LOGIC FOR FLIPFLOPS**

![Screenshot 2024-12-17 142008](https://github.com/user-attachments/assets/c32e4058-3a82-4291-ab97-3fe7b79c5c87)

**TIMING DIGRAMS FOR FLIP FLOPS**

**RESULTS**

Thus the truth table of T-FLIPFLOP in Quartus II using Verilog programming are studied, verified and executed successfully.
