Proof of Concept SwiftGen Build Rule
====================================

![Build Rule](https://raw.githubusercontent.com/gredman/SwiftGenBuildRule/main/images/rule.png)

A custom build rule takes two files as input:

- the swiftgen.yml config
- an accompanying asset catalog

and produces generated code in the derived sources. This is similar to how CoreData model objects are generated for example.

The results of this approach are:

- generated code is kept out of project folder
- code always generated at the start of the build process, i.e. new assets can be referenced immediately

Unfortunately we still need to build first before code completion picks up the new asset references.
