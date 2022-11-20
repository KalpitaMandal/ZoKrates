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

