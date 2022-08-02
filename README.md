# Logic_gates_with_cpp

we can simulate logic circuits like below:

![image](https://user-images.githubusercontent.com/57284868/182420143-c0fb9e4a-98c3-41b8-978a-5058051057e4.png)


program reads two files:
– circuit.txt
– input.txt

According to content in circuit.txt, the program dynamically creates necessary objects for a logic circuit
and evaluates the states listed in input.txt.

prints the output to stdout. Each line in input.txt is a state. For each state, there should be
a line of output printed.

circuit.txt
• Each line starts with a keyword. Possible keywords:
INPUT
OUTPUT
AND
OR
NOT
FLIPFLOP
DECODER
• The first line specifies input labels. Labels are separated by spaces. Example:

  INPUT a input2 c3 k

• Here there are 4 inputs are defined. Each has an identifier. a, input2, c3, k.

• The second line specifies output labels. Labels are separated by spaces. Example:

  OUTPUT d1 d2 d3 d4
• Here there are 4 outputs are defined. Each has an identifier. d1, d2, d3, d4.

• AND keyword specifies that there is an and gate defined. AND keyword follows the identifier for its output and
two other identifiers for the inputs. Example:

AND gate_A c3 another_id

• Here the and gate has an output identified by the string gate_A. Its inputs are identified c3 and another_id.
These identifiers can be input identifiers or identifiers for other gates.

• OR keyword specifies that there is an or gate defined. OR keyword follows the identifier for its output and two
other identifiers for the inputs. Example:

OR gate_B ck id3

• Here the or gate has an output identified by the string gate_B. Its inputs are identified ck and id3. These
identifiers can be input identifiers or identifiers for other gates.

• NOT keyword specifies that there is a not gate defined. NOT keyword follows the identifier for its output and
one other identifier for its input. Example:

NOT gate_C c5

• Here the not gate has an output identified by the string gate_C. It has only one input an it is identified by
the string c5.

• FLIPFLOP keyword specifies that there is a flip-flop gate defined. FLIPFLOP keyword follows the identifier
for its output and one other identifier for its input. Example:

FLIPFLOP gate_F c6

• Here the flip-flop gate has an output identified by the string gate_F. Its input is identified by c6.

• DECODER keyword specifies that there is a decoder gate defined. DECODER keyword follows the identifiers for
its outputs(o1, o2, o3, o4) and identifiers for its inputs(a1, a2). Example:

DECODER d1 d2 d3 d4 g1 another_identifier

• Here the decoder gate has outputs identified by strings o1, o2, o3, o4. Its inputs are identified by g1 and
another_identifier.


input.txt

• Each line is a list of 1 and 0. Example:

1 0 1 1

0 1 1 1

0 0 1 0

1 0 0 1
