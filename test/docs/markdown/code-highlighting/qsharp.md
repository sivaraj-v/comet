


# Code Highlighting Visuals for Q#

## [Q#]"(" should not be highlighted
(left paren)
<div class="important alert"><p>Complete</p></div>
```qsharp
newtype AmpAmpReflectionPhases = (Double[], Double[]);
```

## [Q#]Output parameters should be in one color - Complete
<div class="important alert"><p>Complete</p></div>
```qsharp
function H2Terms (idxHamiltonian : Int) : (Int[], Int[])
```

##  [Q#]PauliZ/PauliI should be in one color
<div class="important alert"><p>Couldn't Repro</p></div>
```qsharp
R(PauliZ, theta, qubit);
R(PauliI, -theta, qubit);

```

## [Q#]"Int" is not highlighted correctly in function name - Complete
<div class="important alert"><p>Complete</p></div>
```qsharp
function InterpolatedEvolution (inerpolationTime : Double, evolutionGeneratorStart : EvolutionGenerator, evolutionGeneratorEnd : EvolutionGenerator, timeDependentSimulationAlgorithm : TimeDependentSimulationAlgorithm) : (Qubit[] => () : Adjoint, Controlled)
```

## [Q#]operation name RangeStart/RandEnd/RangeStep should be in one color - Complete
<div class="important alert"><p>Complete</p></div>
```qsharp
operation RangeEnd (r : Range) : Int
operation RangeStart (r : Range) : Int
```

## Old stuff

```qsharp
operation ApplyToEach (singleQubitOperation : ('T => () : ), register : 'T[]) : ()

namespace Microsoft.Quantum.Canon {
    open Microsoft.Quantum.Primitive

    /// Use this to generate an array of couplings
    operation GenerateRandom1DJCoupling(nSites: Int) : Double[] {
        body {
            mutable jCCouplings = new Double[nSites]
            let bitsOfRandomness = 8
            let someBool = true
            for(idx in 0..nSites-1) {
                set jCCouplings[idx] = RandomReal(bitsOfRandomness)
            }
            return jCCouplings
        }
    }
    function jC1DFromArray(data: Double[], schedule: Double, idx: Int): Double {
        return schedule * data[idx]
    }



    /// Ising all-to-all model
    function IsingA2AGeneratorIndex(nSites : Int, hx : Double,  jC: ((Int, Int) -> Double), idxHamiltonian : Int) : GeneratorIndex
    {
        // when idxHamiltonian is in [0, nSites - 1], apply transverse field "hx"
        // when idxHamiltonian is in [nSites, 2 * nSites - 1], apply Ising couplings jC(idxSite)
        mutable idxPauliString = new Int[0]
        mutable idxQubits = new Int[0]
        mutable coeff = ToDouble(0)
        consta hi = Pauli


        if(idxHamiltonian < nSites){
            set idxPauliString = [1]
            set idxQubits = [idxHamiltonian]
            set coeff = - 1.0 * hx
        }

        // test reserved
        mutable abstract as double

        elif(idxHamiltonian < nSites + nSites * nSites){
            let hello = "hi"
            let idx = idxHamiltonian - nSites
            let idxI = idx % nSites
            let idxJ = idx / nSites
            if(idxI < idxJ){
                set coeff = - 1.0 * jC(idxI, idxJ)
                set idxPauliString = [3; 3]
                set idxQubits = [idxI; idxJ]
            }
        }
        let generatorIndex = GeneratorIndex((idxPauliString,[coeff]),idxQubits)
        return generatorIndex
    }
}
```

```qsharp
    function IsingA2AGeneratorIndex(nSites : Int, hx : Double,  jC: ((Int, Int) -> Double), idxHamiltonian : Int) : GeneratorIndex
    {
        // when idxHamiltonian is in [0, nSites - 1], apply transverse field "hx"
        // when idxHamiltonian is in [nSites, 2 * nSites - 1], apply Ising couplings jC(idxSite)
        mutable idxPauliString = new Int[0]
        mutable idxQubits = new Int[0]
        mutable coeff = ToDouble(0)

        if(idxHamiltonian < nSites){
            set idxPauliString = [1]
            set idxQubits = [idxHamiltonian]
            set coeff = - 1.0 * hx
        }
        elif(idxHamiltonian < nSites + nSites * nSites){
            let hello = "hi"
            let idx = idxHamiltonian - nSites
            let idxI = idx % nSites
            let idxJ = idx / nSites
            if(idxI < idxJ){
                set coeff = - 1.0 * jC(idxI, idxJ)
                set idxPauliString = [3; 3]
                set idxQubits = [idxI; idxJ]
            }
        }
        let generatorIndex = GeneratorIndex((idxPauliString,[coeff]),idxQubits)
        return generatorIndex
    }
}
```