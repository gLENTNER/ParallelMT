#ParallelMT

####A Parallel Pseudo Random Number Generator for Monte Carlo Applications.

The ParallelMT class is an extension to the MT19937 class, both contained within a single MT
namespace. MT19937 is adapted from the original 64-bit pseudo random number generator
(Nishimura and Matsumoto, 2004). Here we have a class constructed with either a single seed or
an array seed. Methods include RandomInteger and RandomReal. The ParallelMT class creates a
family of MT19937 objects seeded independently allowing for simultaneous access and generation
from within a parallel environment.
