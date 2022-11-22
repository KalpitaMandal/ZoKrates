## Getting started

The "Hello World" example:
```
def main(private field a, field b) {
    assert(a * a == b);
    return;
}
```

The main function is similar to that in java, this is the only function that runs and all other things need to be called within this function. 
`field` represents the basic data type in circuits. `private` signals that we do not want to reveal this input, but still prove that we know its value. All variables are immutable by default and to specify mutability `mut` is the keyword used. The functions have an exclusive scope. 

### compilation commands

```
# compile
zokrates compile -i root.zok
# perform the setup phase
zokrates setup
# execute the program
zokrates compute-witness -a 337 113569
# generate a proof of computation
zokrates generate-proof
# export a solidity verifier
zokrates export-verifier
# or verify natively
zokrates verify
```

### Variable types
Functions defined as the follows:
```
def main -> feild {...}
```
Indicate that the funtion returns a value of type field. `Field` types can range from value between [1 - 21888242871839275222246405745257275088548364400416034343698204186575808495617] (this is a very large prime number). Anything stored in the field type outside the range will overflow.

`bool` type is used for storing 0 or 1 values.

`u8/u16/u32/u64` type implies an unsigned integer that stores values in the range of [0 - 2 ** bitwidth]. For eg, u8 will range from [0 - 2 ** 8].


