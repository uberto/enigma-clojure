# Enigma Clojure

This is the implementation of the paper enigma clojure machine as part of Steve Freeman and FinancialAgile session at Software Craftsmanship 2012.

Enigma clojure implementes the paper enigma version that can be found at http://mckoss.com/Crypto/Enigma.htm

## How to bootstrap the project
* install leningen https://github.com/technomancy/leiningen/
* type: lein midje to run the tests

## Paper enigma machine usage example

#### Setup
1. Select left/center/right rotors.
2. Position initial wheel positions by sliding the indicated window letter up to the first row.

#### Operation
Start at the input column at right, then work left to reflector, and then back to the right to the output column.

1. If the up arrow appears in the window row, shift that rotor and the rotor to the left up one row (the Right Rotor is always shifted up one row before each letter is encoded/decoded).
2. Select letter to encode/decode in the Input column.
3. Read adjacent letter, X , in right hand column of the Right Rotor; select the letter X in the left hand column of the Rotor.
4. Repeat for Center Rotor.
5. Repeat for Left Rotor.j
6. Read the adjacent letter, R , in the Reflector; select the other letterR intheReflector.
7. Read adjacent letter, Y , in left hand column of the Left Rotor; selecttheletterY intherighthandcolumnoftheRotor.
8. Repeat for Center Rotor.
9. Repeat for Right Rotor.
10. Write down the adjacent letter, Z , in the output column. Repeat for each letter of the message.

#### Example
Initial setting: I-II-III: MCK, Letter E encodes to Q. Sample Message: QMJIDO MZWZJFJR

## License

Copyright (C) 2012 reborg@reborg.net

Distributed under the Eclipse Public License, the same as Clojure.
