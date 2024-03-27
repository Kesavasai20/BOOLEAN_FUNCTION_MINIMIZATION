# BOOLEAN_FUNCTION_MINIMIZATION

**AIM:**

To implement the given logic function verify its operation in Quartus using Verilog programming.

F1= A’B’C’D’+AC’D’+B’CD’+A’BCD+BC’D 

F2=xy’z+x’y’z+w’xy+wx’y+wxy

**Equipment Required:**

Hardware – PCs, Cyclone II , USB flasher

**Software – Quartus prime**

**Theory**

**Logic Diagram**

**Procedure**

1.	Type the program in Quartus software.

2.	Compile and run the program.

3.	Generate the RTL schematic and save the logic diagram.

4.	Create nodes for inputs and outputs to generate the timing diagram.

5.	For different input combinations generate the timing diagram.


**Program:**

**Program to implement the given logic function and to verify its operations in quartus using Verilog programming.**

**Developed by:  K KESAVA SAI**

**RegisterNumber: 212223230105**

```
module experiment(
    input a, b, c, d, w, x, y, z,
    output f1, f2
);

wire adash, bdash, cdash, ddash, ydash, zdash, wdash;
not(adash, a);
not(bdash, b);
not(cdash, c);
not(ddash, d);
not(ydash, y);
not(zdash, z);
not(wdash, w);

wire p, q, r, s, t, u, term1, term2, term3;

and(p, bdash, ddash);
and(q, adash, b, d);
and(r, a, b, cdash);
and(term1, ydash, z);
and(term2, x, y);
and(term3, w, y);

or(f1, p, q, r);
or(f2, term1, term2, term3);

endmodule
```

![image](https://github.com/Kesavasai20/BOOLEAN_FUNCTION_MINIMIZATION/assets/138849303/a2467947-0fec-4cf4-99d7-86f4e56ac2c9)


**RTL realization**
![DE-2 2](https://github.com/Kesavasai20/BOOLEAN_FUNCTION_MINIMIZATION/assets/138849303/6f9f20eb-ee9c-4961-8ba8-3269fb978b5f)


**Output:**

![image](https://github.com/Kesavasai20/BOOLEAN_FUNCTION_MINIMIZATION/assets/138849303/b89694a0-bd52-48ea-b805-576176d54758)

**TRUTH TABLE**

![image](https://github.com/Kesavasai20/BOOLEAN_FUNCTION_MINIMIZATION/assets/138849303/89ebe1fc-7ad8-4777-a09f-73b4923a7ce7)

**Result:**

Thus the given logic functions are implemented using and their operations are verified using Verilog programming.

