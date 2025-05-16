# T-FLIPFLOP-POSEDGE

**AIM:**

To implement  T flipflop using verilog and validating their functionality using their functional tables

**SOFTWARE REQUIRED:**

Quartus prime

**THEORY**

**T Flip-Flop**

T flip-flop is the simplified version of JK flip-flop. It is obtained by connecting the same input ‘T’ to both inputs of JK flip-flop. It operates with only positive clock transitions or negative clock transitions. The circuit diagram of T flip-flop is shown in the following figure.

![image](https://github.com/naavaneetha/T-FLIPFLOP-POSEDGE/assets/154305477/458a68fe-2d08-4a9d-ac4f-7ae0480ce0bd)

 
This circuit has single input T and two outputs Qtt & Qtt’. The operation of T flip-flop is same as that of JK flip-flop. Here, we considered the inputs of JK flip-flop as J = T and K = T in order to utilize the modified JK flip-flop for 2 combinations of inputs. So, we eliminated the other two combinations of J & K, for which those two values are complement to each other in T flip-flop. The following table shows the state table of T flip-flop.

Here, Qtt & Qt+1t+1 are present state & next state respectively. So, T flip-flop can be used for one of these two functions such as Hold, & Complement of present state based on the input conditions, when positive transition of clock signal is applied. The following table shows the characteristic table of T flip-flop. Inputs Present State Next State

![image](https://github.com/naavaneetha/T-FLIPFLOP-POSEDGE/assets/154305477/cdd7fb32-539f-4b66-bb8d-f305a153c886)

 
From the above characteristic table, we can directly write the next state equation as Q(t+1)=T′Q(t)+TQ(t)′ ⇒Q(t+1)=T⊕Q(t)

**Procedure**

1: Type the program in Quartus software.

2: Compile and run the program.

3: Generate the RTL schematic and save the logic diagram.

4: Create nodes for inputs and outputs to generate the timing diagram.

5: For different input combinations generate the timing diagram.

**PROGRAM**

Developed by: Gokul Nath R RegisterNumber: 212224230077
```
module exp9(T,clk,Q,Qbar);
input T,clk;
output reg Q;
output reg Qbar;
initial Q=0;
initial Qbar=1;
always @(posedge clk)
begin
Q=(T&(~Q))|((~T)&Q);
Qbar=~Q;
end
endmodule
```

**RTL LOGIC FOR FLIPFLOPS**

![444245399-dce2a99a-6532-4ecf-b74b-7716a8b48081](https://github.com/user-attachments/assets/75612868-3cd8-4e28-93ed-792dd9390f1b)

**TIMING DIGRAMS FOR FLIP FLOPS**

![444245532-ab6d1682-c90c-439d-92ec-9aeb47d413be](https://github.com/user-attachments/assets/9a942fbc-fec0-429f-9f63-9806ef37c2b6)

**RESULTS**

Thus T flipflop using verilog and validating their functionality using their functional tables is verified.
