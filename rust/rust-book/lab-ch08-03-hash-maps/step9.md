# Hashing Functions

By default, `HashMap` uses a hashing function called _SipHash_ that can provide
resistance to denial-of-service (DoS) attacks involving hash tables. This is
not the fastest hashing algorithm available, but the trade-off for better
security that comes with the drop in performance is worth it. If you profile
your code and find that the default hash function is too slow for your
purposes, you can switch to another function by specifying a different hasher.
A _hasher_ is a type that implements the `BuildHasher` trait. We’ll talk about
traits and how to implement them in Chapter 10. You don’t necessarily have to
implement your own hasher from scratch; *https://crates.io* has libraries
shared by other Rust users that provide hashers implementing many common
hashing algorithms.