# Generic Multi-Way Tree ADT (Java)

A generic N-ary (multi-way) tree data structure implemented in Java (`MyTree<T>`), supporting unbounded branching factors, recursive sub-tree mutations, topological relation queries, and unique element semantics.

## Core Features & Operations
- Generic Nodes & Unbounded Children: Accommodates arbitrary data types `T` assuming element uniqueness per node, with zero capacity limits on child branches.
- Node Insertion (`add`): Attaches child elements directly under an existing parent node, validating parent presence.
- Recursive Sub-Tree Pruning (`remove`): Removes target nodes along with their complete descendant subtrees, throwing `IllegalArgumentException` upon invalid root removal attempts.
- Topological Ancestry Queries: Efficiently evaluates hierarchical paths via `isSuccessorOf` (descendant check) and `isPredecessorOf` (ancestor check).
- Search & Subtree Retrieval: Provides existence lookups (`exists`) and sub-tree references (`get`) returning full sub-tree structures.
- Structural Metrics: Dynamic tree size calculations (`size`) initializing at 1 upon root instantiation.

## Method Signatures
- MyTree(T rootValue)
- boolean add(T parent, T child)
- boolean remove(T element) throws IllegalArgumentException
- boolean exists(T element)
- boolean isSuccessorOf(T descendant, T ancestor)
- boolean isPredecessorOf(T ancestor, T descendant)
- int size()
- MyTree<T> get(T element)
- T getData()

## Requirements
- Java Development Kit (JDK 8 or higher).

## Build & Run
Compile Java source files:
javac *.java

Run main execution driver or unit tests:
java Main
