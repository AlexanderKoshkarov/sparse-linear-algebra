# sparse-linear-algebra

Sparse linear algebra datastructures and algorithms in Haskell

TravisCI : [![Build Status](https://travis-ci.org/ocramz/sparse-linear-algebra.png)](https://travis-ci.org/ocramz/sparse-linear-algebra)

This library provides common numerical analysis functionality, without requiring any external bindings. It is not optimized for performance (yet), but it serves as an experimental platform for scientific computation in a purely functional setting.

Algorithms :

* Iterative linear solvers

    * Conjugate Gradient Squared (CGS)

    * BiConjugate Gradient Stabilized (BiCGSTAB) (non-Hermitian systems)

* Matrix decompositions

    * QR factorization

* Utilities : Vector and matrix norms, matrix condition number, Givens rotation, Householder reflection

* Predicates : Matrix orthogonality test (A^T A ~= I)



----------

This is also an experiment in principled scientific programming :

* set the stage by declaring typeclasses and some useful generic operations (normed linear vector spaces, i.e. finite-dimensional spaces equipped with an inner product that induces a distance function),

* define appropriate data structures, and how they relate to those properties (sparse vectors and matrices, defined internally via `Data.IntMap`, are made instances of the VectorSpace and AdditiveGroup classes respectively). This allows to decouple the algorithms from the actual implementation of the backend,

* implement the algorithms, following 1:1 the textbook [1] 


## License

GPL3, see LICENSE

## Credits

Inspired by

* `linear` : https://hackage.haskell.org/package/linear
* `sparse-lin-alg` : https://github.com/laughedelic/sparse-lin-alg

## References

[1] : Y. Saad, Iterative Methods for Sparse Linear Systems, 2nd ed., 2000