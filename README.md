#ParallelMT

####A Parallel Pseudo Random Number Generator for Monte Carlo Applications.

The ParallelMT class is an extension to the MT19937 class, both contained within a single MT
namespace. MT19937 is adapted from the original 64-bit pseudo random number generator
(Nishimura and Matsumoto, 2004). Here we have a class constructed with either a single seed or
an array seed. Methods include RandomInteger and RandomReal. The ParallelMT class creates a
family of MT19937 objects seeded independently allowing for simultaneous access and generation
from within a parallel environment.

### Example usage:

```c++
#include <ParallelMT.hh>
#include <vector>

#define threads 4

int main(){

    // std::vector<double> of length two designates `limits`
    double init[] = {1, 6};
    std::vector<double> limits(init, sizeof(init)/sizeof(double));

    // construct using default seed
    ParallelMT pmt1();

    // construct using specified seed
    ParallelMT pmt2(0x1234ULL);

    // generate a random real numbers
    for (int i = 0; i < 1e6; i++)
    
    ...
    return 0;
}
```
