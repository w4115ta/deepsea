
In thinking about various contract systems and writing specifications for a few of them, I've noticed that almost all sensible contracts can be modelled as some kind of simple transition system. Contract programmers should be able to express these systems declaratively, without dealing with the messy details of the EVM.

The central idea is to express contract methods as the product of exactly four components:

-   a guard (or conditional)
-   a list of storage mutations
-   a list of effects (external calls and event logs)
-   a return value

The contract interface is determined exactly by its type signature.

Some existing contract programming languages that (to some degree) share this approach:

-   [scilla](https://scilla.readthedocs.io/en/latest/)
-   [pact](https://github.com/kadena-io/pact)

See the example programs in this directory.

