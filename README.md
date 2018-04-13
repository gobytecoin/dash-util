# gobyte-util

[![npm version](https://img.shields.io/npm/v/gobyte-util.svg)](https://www.npmjs.com/package/gobyte-util)
[![Build Status](https://travis-ci.org/gobytecoin/gobyte-util.svg?branch=master)](https://travis-ci.org/gobytecoin/gobyte-util)
[![Dependency Status](https://david-dm.org/gobytecoin/gobyte-util.svg)](https://david-dm.org/gobytecoin/gobyte-util)

**Utility functions for GoByte hashes and targets**

## Usage

`npm install gobyte-util`

### Methods

#### `toHash(hex)`

Takes a hex string that contains a GoByte hash as input, and returns a GoByte-protocol-friendly little-endian Buffer. Throws an error if the hex string is not of length 64 (representing a 256-bit hash).

#### `compressTarget(target)`

Converts the difficulty target `target` to its compact representation (used in the "bits" field in block headers). `target` should be a `Buffer` (little-endian, the zeroes should be at the end). Returns a `number`.

#### `expandTarget(bits)`

Converts the compressed target integer `bits` to its target hash representation. Returns a `Buffer`.
