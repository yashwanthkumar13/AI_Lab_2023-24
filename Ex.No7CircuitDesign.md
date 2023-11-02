# Ex.No: 7  Logic Programming –  Logic Circuit Design
### DATE:                                                                            
### REGISTER NUMBER : 212221040185
### AIM: 
To write a logic program to design a circuit like half adder and half subtractor.
###  Algorithm:
1. Start the Program
2. Design a AND gate logic if both inputs are 1 then output is 1.
3. Design a OR gate logic if any one of input is 1 then output is 1.
4. Design a XOR gate logic if both inputs are different then output is 1.
5. Design a NOT gate logic if input is 0 then output is 1.
6. Design a half adder and half subtractor using the rules.
7. Test the logic.
8. Stop the program.

### Program:

    and_gate(1, 1, 1).
    and_gate(_, _, 0).
    
    or_gate(0, 0, 0).
    or_gate(_, _, 1).
    
    xor_gate(0, 0, 0).
    xor_gate(1, 1, 0).
    xor_gate(_, _, 1).
    
    not_gate(0, 1).
    not_gate(1, 0).
    
    half_adder(A, B, Sum, Carry) :-
        xor_gate(A, B, Sum),
        and_gate(A, B, Carry).
    
    half_subtractor(A, B, Diff, Borrow) :-
        xor_gate(A, B, Diff),
        not_gate(A, NotA),
        and_gate(NotA, B, Borrow).
    
    test_logic :-
        write('AND gate:'), nl,
        and_gate(0, 0, X1), write('0 AND 0 = '), write(X1), nl,
        and_gate(0, 1, X2), write('0 AND 1 = '), write(X2), nl,
        and_gate(1, 0, X3), write('1 AND 0 = '), write(X3), nl,
        and_gate(1, 1, X4), write('1 AND 1 = '), write(X4), nl,

        write('OR gate:'), nl,
        or_gate(0, 0, X5), write('0 OR 0 = '), write(X5), nl,
        or_gate(0, 1, X6), write('0 OR 1 = '), write(X6), nl,
        or_gate(1, 0, X7), write('1 OR 0 = '), write(X7), nl,
        or_gate(1, 1, X8), write('1 OR 1 = '), write(X8), nl,
    
        write('XOR gate:'), nl,
        xor_gate(0, 0, X9), write('0 XOR 0 = '), write(X9), nl,
        xor_gate(0, 1, X10), write('0 XOR 1 = '), write(X10), nl,
        xor_gate(1, 0, X11), write('1 XOR 0 = '), write(X11), nl,
        xor_gate(1, 1, X12), write('1 XOR 1 = '), write(X12), nl,
    
        write('NOT gate:'), nl,
        not_gate(0, X13), write('NOT 0 = '), write(X13), nl,
        not_gate(1, X14), write('NOT 1 = '), write(X14), nl,
    
        write('Half Adder:'), nl,
        half_adder(0, 0, S1, C1), write('0 + 0 = '), write(S1), write(' with carry '), write(C1), nl,
        half_adder(0, 1, S2, C2), write('0 + 1 = '), write(S2), write(' with carry '), write(C2), nl,
        half_adder(1, 0, S3, C3), write('1 + 0 = '), write(S3), write(' with carry '), write(C3), nl,
        half_adder(1, 1, S4, C4), write('1 + 1 = '), write(S4), write(' with carry '), write(C4), nl,
    
        write('Half Subtractor:'), nl,
        half_subtractor(0, 0, D1, B1), write('0 - 0 = '), write(D1), write(' with borrow '), write(B1), nl,
        half_subtractor(0, 1, D2, B2), write('0 - 1 = '), write(D2), write(' with borrow '), write(B2), nl,
        half_subtractor(1, 0, D3, B3), write('1 - 0 = '), write(D3), write(' with borrow '), write(B3), nl,
        half_subtractor(1, 1, D4, B4), write('1 - 1 = '), write(D4), write(' with borrow '), write(B4), nl.


### Output:

![image](https://github.com/yashwanthkumar13/AI_Lab_2023-24/assets/116741234/d6e73ad7-46b1-43d1-a18e-01e54f83e6e2)


### Result:
Thus the truth table of circuit verified sucessfully.
