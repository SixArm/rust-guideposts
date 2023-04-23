# Eq, PartialEq, Ord, PartialOrd traits

In Rust, traits are used to define shared behavior for types. The following are commonly used traits for comparing types:

* Eq trait: This trait defines the equality relation between two values of a given type. The Eq trait requires that the type implements the PartialEq trait, which defines the partial equality relation. If two values of a type are equal according to the Eq trait, they must be considered indistinguishable in every way.

* PartialEq trait: This trait defines the partial equality relation between two values of a given type. The PartialEq trait requires that the type implements an eq method that takes another value of the same type as an argument, and returns a bool indicating whether the two values are equal. If two values of a type are equal according to the PartialEq trait, they must be considered indistinguishable for the purposes of the Eq trait as well.

* Ord trait: This trait defines the total order relation between two values of a given type. The Ord trait requires that the type implements the PartialOrd trait, which defines the partial order relation. If two values of a type are compared using the Ord trait, they must be completely ordered in a consistent way.

* PartialOrd trait: This trait defines the partial order relation between two values of a given type. The PartialOrd trait requires that the type implements a partial_cmp method that takes another value of the same type as an argument, and returns an Option<Ordering> indicating the ordering relationship between the two values. If two values of a type are compared using the PartialOrd trait, they must be partially ordered in a consistent way.

These traits are important for comparing types in Rust, and are used extensively in Rust's standard library.
