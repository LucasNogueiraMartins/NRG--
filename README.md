# NRG--

A class is introduced that contains all the attributes and methods necessary for implementing the Numerical Renormalization Group (NRG). There are two modules: `Kondo.py` and `Coupled-Spins.py`. The first applies NRG to the Kondo Model of magnetic impurities, while the second is a toy model of spins with neighborhood coupling.

## Initiating the class

The module `Kondo.py` is initiated by the parameters

- `lambda`: Parameter that sets the logarithm discretization. 
- `J`: Coupling between the spin impurity and the spins of the electrons. 

The module `coupled-spins.py` is initiated by the parameters

- `lambda`: Base of the exponential decreasing function. 
- `J`: Neighborhood coupling.

## Methods of the Class 

There are three main methods: diagonalization of the Hamiltonian `.diag()`, iteration of the Hamiltonian `.ite()`, and the `.cutoff(S)`.

- `.diag()`: changes the basis of all matrices that are important for the '.ite()', diagonalizing the Hamiltonian
- `.ite()`: applies the numerical renormalization group transformation.
- `.cutoff(S)`: applies the cut-off on the higher excited states, retaining only the first S excited states. (S is an integer)

There are several attributes that work internally in the class. The important ones are the Hamiltonian `.H` (a two-dimensional `numpy.array`) and the energies `.val`(a one-dimensional `numpy.array`).


