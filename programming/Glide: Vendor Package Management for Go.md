---
Title: "Glide: Vendor Package Management for Go"
Date: 2018-01-29 11:34:24
Categories: [programming]
Tags: [go, gliden]
Authors: sedlav
---

**Glide** is a package manager for Go that is conceptually similar to package managers for other languages such as Cargo for Rust, NPM for Node.js, Pip for Python, Bundler for Ruby, and so forth.

**Glide** provides the following functionality:

- Records dependency information in a glide.yaml file. This includes a name, version or version range, version control information for - private repos or when the type cannot be detected, and more.
- Tracks the specific revision each package is locked to in a glide.lock file. This enables reproducibly fetching the dependency tree.
- Works with Semantic Versions and Semantic Version ranges.

[Link](https://glide.readthedocs.io/en/latest/)
