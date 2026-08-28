# 3D Tiles Validation with WFF Semantics

This guide explains how to validate a 3D Tiles dataset using the [Cesium 3D Tiles Validator](https://github.com/CesiumGS/3d-tiles-validator), along with a semantic schema derived from the [Well-Formed Format (WFF) 1.9.0 metadata schema](../WFF1.9.0.metadata.schema.json).

The process ensures that custom semantic fields defined in WFF are correctly interpreted and validated by the 3D Tiles Validator.

## Prerequisites

- Node.js (v16 or later recommended)
- The [3D Tiles Validator](https://github.com/CesiumGS/3d-tiles-validator)

## Installation

In order to install the validator locally into a directory, run
```sh
npm install 3d-tiles-validator
```

## Usage

Use the Cesium 3D Tiles Validator to validate your tileset, passing the `--optionsFile` flag with your options file:

```sh
npx 3d-tiles-validator --optionsFile wff19_options.json -t path/to/tileset.json
```

When the validator is not installed as a package from NPM, but supposed to be used directly in a cloned repository, then the command line usage is as follows:
```sh
npx ts-node src/main.ts --optionsFile wff19_options.json -t path/to/tileset.json
```
