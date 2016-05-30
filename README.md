
# Repackaged Renjin Dependencies

This repo includes build files for repackaging a number of Renjin's dependency into a private package namespace
to avoid version conflicts.

Renjin depends on a few widely-used Java libraries such as [guava](https://github.com/google/guava) and
[asm](http://asm.ow2.org/). Because these libraries are _so_ widely used, they are especially prone to version
conflict, when, for example, the web server framework uses a different and incompatible version of guava.

Having a repackaged version of guava ensures that the version of guava that Renjin expects can coexist peacefully
with a different version required by Spark, or other platform.

