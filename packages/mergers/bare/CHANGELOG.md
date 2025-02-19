# @graphql-mesh/merger-bare

## 0.15.0

### Minor Changes

- bcd9355ee: Breaking change in merger API;

  Before a merger should return a `GraphQLSchema`, not it needs to return `SubschemaConfig` from `@graphql-tools/delegate` package.
  The idea is to prevent the schema from being wrap to reduce the execution complexity.
  Now if merger returns an executor, it will be used directly as an executor inside Envelop's pipeline.
  Also it can return `transforms` which will be applied during execution while schema transforms are applied on build time without any modification in the resolvers.

  If there are some root transforms, those are applied together with the source transforms on the execution level in case of a single source.

### Patch Changes

- Updated dependencies [6e6fd4ab7]
- Updated dependencies [bcd9355ee]
  - @graphql-mesh/utils@0.37.1
  - @graphql-mesh/types@0.78.0

## 0.14.2

### Patch Changes

- Updated dependencies [66f5d0189]
- Updated dependencies [0401c7617]
  - @graphql-mesh/types@0.77.1
  - @graphql-mesh/utils@0.37.0

## 0.14.1

### Patch Changes

- Updated dependencies [12e1e5d72]
- Updated dependencies [12e1e5d72]
  - @graphql-mesh/types@0.77.0
  - @graphql-mesh/utils@0.36.1

## 0.14.0

### Minor Changes

- a0950ac6f: Breaking Change:

  - Now you can set a global `customFetch` instead of setting `customFetch` individually for each handler. `customFetch` configuration field for each handler will no longer work. And also `customFetch` needs to be the path of the code file that exports the function as `default`. `moduleName#exportName` is not supported for now.

  - While programmatically creating the handlers, now you also need `fetchFn` to be passed to the constructor;

  ```ts
  new GraphQLHandler({
    ...,
    fetchFn: myFetchFn,
  })
  ```

  - `readFileOrUrl`'s second `config` parameter is now required. Also this second parameter should take an object with `cwd`, `importFn`, `fetch` and `logger`. You can see the diff of handler's codes as an example.

### Patch Changes

- Updated dependencies [19d06f6c9]
- Updated dependencies [19d06f6c9]
- Updated dependencies [a0950ac6f]
  - @graphql-mesh/utils@0.36.0
  - @graphql-mesh/types@0.76.0

## 0.13.55

### Patch Changes

- Updated dependencies [d4754ad08]
- Updated dependencies [2df026e90]
  - @graphql-mesh/types@0.75.0
  - @graphql-mesh/utils@0.35.7

## 0.13.54

### Patch Changes

- Updated dependencies [ed9ba7f48]
  - @graphql-mesh/types@0.74.2
  - @graphql-mesh/utils@0.35.6

## 0.13.53

### Patch Changes

- Updated dependencies [41cfb46b4]
  - @graphql-mesh/utils@0.35.5
  - @graphql-mesh/types@0.74.1

## 0.13.52

### Patch Changes

- Updated dependencies [13b9b30f7]
  - @graphql-mesh/types@0.74.0
  - @graphql-mesh/utils@0.35.4

## 0.13.51

### Patch Changes

- Updated dependencies [9733f490c]
  - @graphql-mesh/utils@0.35.3
  - @graphql-mesh/types@0.73.3

## 0.13.50

### Patch Changes

- Updated dependencies [3c0366d2c]
- Updated dependencies [3c0366d2c]
  - @graphql-mesh/utils@0.35.2
  - @graphql-mesh/types@0.73.2

## 0.13.49

### Patch Changes

- Updated dependencies [abe9fcc41]
  - @graphql-mesh/utils@0.35.1
  - @graphql-mesh/types@0.73.1

## 0.13.48

### Patch Changes

- 974e703e2: Cleanup dependencies
- Updated dependencies [974e703e2]
- Updated dependencies [19a99c055]
- Updated dependencies [974e703e2]
- Updated dependencies [974e703e2]
- Updated dependencies [893d526ab]
- Updated dependencies [974e703e2]
  - @graphql-mesh/types@0.73.0
  - @graphql-mesh/utils@0.35.0

## 0.13.47

### Patch Changes

- Updated dependencies [43eb3d2c2]
  - @graphql-mesh/utils@0.34.10
  - @graphql-mesh/types@0.72.5

## 0.13.46

### Patch Changes

- Updated dependencies [55ad5ea44]
  - @graphql-mesh/utils@0.34.9
  - @graphql-mesh/types@0.72.4

## 0.13.45

### Patch Changes

- Updated dependencies [31efa964e]
  - @graphql-mesh/utils@0.34.8
  - @graphql-mesh/types@0.72.3

## 0.13.44

### Patch Changes

- @graphql-mesh/utils@0.34.7
- @graphql-mesh/types@0.72.2

## 0.13.43

### Patch Changes

- Updated dependencies [b9beacca2]
  - @graphql-mesh/utils@0.34.6
  - @graphql-mesh/types@0.72.1

## 0.13.42

### Patch Changes

- Updated dependencies [fa2542468]
  - @graphql-mesh/types@0.72.0
  - @graphql-mesh/utils@0.34.5

## 0.13.41

### Patch Changes

- Updated dependencies [ddbbec8a8]
  - @graphql-mesh/utils@0.34.4
  - @graphql-mesh/types@0.71.4

## 0.13.40

### Patch Changes

- Updated dependencies [2e9addd80]
  - @graphql-mesh/utils@0.34.3
  - @graphql-mesh/types@0.71.3

## 0.13.39

### Patch Changes

- @graphql-mesh/types@0.71.2
- @graphql-mesh/utils@0.34.2

## 0.13.38

### Patch Changes

- 7856f92d3: Bump all packages
- Updated dependencies [7856f92d3]
  - @graphql-mesh/types@0.71.1
  - @graphql-mesh/utils@0.34.1

## 0.13.37

### Patch Changes

- Updated dependencies [f963b57ce]
- Updated dependencies [0644f31f2]
- Updated dependencies [331b62637]
- Updated dependencies [331b62637]
- Updated dependencies [331b62637]
- Updated dependencies [331b62637]
  - @graphql-mesh/types@0.71.0
  - @graphql-mesh/utils@0.34.0

## 0.13.36

### Patch Changes

- @graphql-mesh/utils@0.33.6
- @graphql-mesh/types@0.70.6

## 0.13.35

### Patch Changes

- @graphql-mesh/types@0.70.5
- @graphql-mesh/utils@0.33.5

## 0.13.34

### Patch Changes

- 35a55e841: Bump GraphQL Tools packages
- Updated dependencies [35a55e841]
  - @graphql-mesh/types@0.70.4
  - @graphql-mesh/utils@0.33.4

## 0.13.33

### Patch Changes

- @graphql-mesh/types@0.70.3
- @graphql-mesh/utils@0.33.3

## 0.13.32

### Patch Changes

- Updated dependencies [b02f5b008]
  - @graphql-mesh/types@0.70.2
  - @graphql-mesh/utils@0.33.2

## 0.13.31

### Patch Changes

- 2d5c6c72a: add Git repository link in package.json
- Updated dependencies [2d5c6c72a]
  - @graphql-mesh/types@0.70.1
  - @graphql-mesh/utils@0.33.1

## 0.13.30

### Patch Changes

- Updated dependencies [d567be7b5]
  - @graphql-mesh/types@0.70.0
  - @graphql-mesh/utils@0.33.0

## 0.13.29

### Patch Changes

- Updated dependencies [f30dba61e]
  - @graphql-mesh/types@0.69.0
  - @graphql-mesh/utils@0.32.2

## 0.13.28

### Patch Changes

- Updated dependencies [be61de529]
  - @graphql-mesh/types@0.68.3
  - @graphql-mesh/utils@0.32.1

## 0.13.27

### Patch Changes

- Updated dependencies [b1a6df928]
- Updated dependencies [67fb11706]
  - @graphql-mesh/types@0.68.2
  - @graphql-mesh/utils@0.32.0

## 0.13.26

### Patch Changes

- Updated dependencies [b2c537c2a]
  - @graphql-mesh/utils@0.31.0
  - @graphql-mesh/types@0.68.1

## 0.13.25

### Patch Changes

- Updated dependencies [6c318b91a]
  - @graphql-mesh/types@0.68.0
  - @graphql-mesh/utils@0.30.2

## 0.13.24

### Patch Changes

- @graphql-mesh/types@0.67.1
- @graphql-mesh/utils@0.30.1

## 0.13.23

### Patch Changes

- 01bac6bb5: fix - align graphql-tools versions
- Updated dependencies [01bac6bb5]
- Updated dependencies [01bac6bb5]
  - @graphql-mesh/types@0.67.0
  - @graphql-mesh/utils@0.30.0

## 0.13.22

### Patch Changes

- Updated dependencies [268db0462]
  - @graphql-mesh/utils@0.29.0
  - @graphql-mesh/types@0.66.6

## 0.13.21

### Patch Changes

- Updated dependencies [2ffb1f287]
  - @graphql-mesh/types@0.66.5
  - @graphql-mesh/utils@0.28.5

## 0.13.20

### Patch Changes

- 634363331: fix: bump wrap and url-loader packages
- Updated dependencies [6d2d46480]
  - @graphql-mesh/types@0.66.4
  - @graphql-mesh/utils@0.28.4

## 0.13.19

### Patch Changes

- @graphql-mesh/types@0.66.3
- @graphql-mesh/utils@0.28.3

## 0.13.18

### Patch Changes

- Updated dependencies [fb876e99c]
  - @graphql-mesh/types@0.66.2
  - @graphql-mesh/utils@0.28.2

## 0.13.17

### Patch Changes

- Updated dependencies [98ff961ff]
  - @graphql-mesh/types@0.66.1
  - @graphql-mesh/utils@0.28.1

## 0.13.16

### Patch Changes

- b481fbc39: enhance: add tslib to dependencies to reduce bundle size
- Updated dependencies [6f07de8fe]
- Updated dependencies [6f07de8fe]
- Updated dependencies [b481fbc39]
  - @graphql-mesh/types@0.66.0
  - @graphql-mesh/utils@0.28.0

## 0.13.15

### Patch Changes

- Updated dependencies [21de17a3d]
- Updated dependencies [3f4bb09a9]
  - @graphql-mesh/types@0.65.0
  - @graphql-mesh/utils@0.27.9

## 0.13.14

### Patch Changes

- Updated dependencies [8b8eb5158]
- Updated dependencies [8b8eb5158]
  - @graphql-mesh/types@0.64.2
  - @graphql-mesh/utils@0.27.8

## 0.13.13

### Patch Changes

- Updated dependencies [ca6bb5ff3]
  - @graphql-mesh/utils@0.27.7
  - @graphql-mesh/types@0.64.1

## 0.13.12

### Patch Changes

- Updated dependencies [08b250e04]
  - @graphql-mesh/types@0.64.0
  - @graphql-mesh/utils@0.27.6

## 0.13.11

### Patch Changes

- 1815865c3: fix: bump fixed graphql-tools
- Updated dependencies [1815865c3]
  - @graphql-mesh/types@0.63.1
  - @graphql-mesh/utils@0.27.5

## 0.13.10

### Patch Changes

- f202f53af: fix: bump wrap package and throw better error message in case of missing selectionSet for unmatching return types

## 0.13.9

### Patch Changes

- Updated dependencies [b6eca9baa]
- Updated dependencies [b6eca9baa]
  - @graphql-mesh/types@0.63.0
  - @graphql-mesh/utils@0.27.4

## 0.13.8

### Patch Changes

- Updated dependencies [0d43ecf19]
  - @graphql-mesh/types@0.62.2
  - @graphql-mesh/utils@0.27.3

## 0.13.7

### Patch Changes

- Updated dependencies [c71b29004]
- Updated dependencies [447bc3697]
  - @graphql-mesh/utils@0.27.2
  - @graphql-mesh/types@0.62.1

## 0.13.6

### Patch Changes

- Updated dependencies [240ec7b38]
- Updated dependencies [fcbd12a35]
  - @graphql-mesh/types@0.62.0
  - @graphql-mesh/utils@0.27.1

## 0.13.5

### Patch Changes

- Updated dependencies [900a01355]
  - @graphql-mesh/utils@0.27.0

## 0.13.4

### Patch Changes

- Updated dependencies [66ca1a366]
  - @graphql-mesh/types@0.61.0
  - @graphql-mesh/utils@0.26.4

## 0.13.3

### Patch Changes

- Updated dependencies [a79268b3a]
- Updated dependencies [a79268b3a]
  - @graphql-mesh/types@0.60.0
  - @graphql-mesh/utils@0.26.3

## 0.13.2

### Patch Changes

- Updated dependencies [020431bdc]
- Updated dependencies [020431bdc]
- Updated dependencies [020431bdc]
  - @graphql-mesh/types@0.59.0
  - @graphql-mesh/utils@0.26.2

## 0.13.1

### Patch Changes

- Updated dependencies [113091148]
- Updated dependencies [6bb4cf673]
  - @graphql-mesh/utils@0.26.1
  - @graphql-mesh/types@0.58.0

## 0.13.0

### Minor Changes

- 56e2257fa: feat: use JIT in all execution phases

### Patch Changes

- f60bcb083: fix(core): update wrap to fix #3424
- 56e2257fa: fix(merger-bare): handle single source transforms correctly
- Updated dependencies [1ab0aebbc]
- Updated dependencies [56e2257fa]
- Updated dependencies [56e2257fa]
  - @graphql-mesh/types@0.57.2
  - @graphql-mesh/utils@0.26.0

## 0.12.9

### Patch Changes

- Updated dependencies [2b876f2b8]
  - @graphql-mesh/utils@0.25.0

## 0.12.8

### Patch Changes

- Updated dependencies [d907351c5]
  - @graphql-mesh/types@0.57.1
  - @graphql-mesh/utils@0.24.2

## 0.12.7

### Patch Changes

- Updated dependencies [26d685f2a]
  - @graphql-mesh/utils@0.24.1

## 0.12.6

### Patch Changes

- Updated dependencies [cfca98d34]
  - @graphql-mesh/types@0.57.0
  - @graphql-mesh/utils@0.24.0

## 0.12.5

### Patch Changes

- Updated dependencies [5666484d6]
  - @graphql-mesh/utils@0.23.0

## 0.12.4

### Patch Changes

- Updated dependencies [6c216c309]
  - @graphql-mesh/utils@0.22.2

## 0.12.3

### Patch Changes

- Updated dependencies [c22eb1b5e]
  - @graphql-mesh/utils@0.22.1

## 0.12.2

### Patch Changes

- Updated dependencies [ec0d1d639]
- Updated dependencies [1cc0acb9a]
  - @graphql-mesh/types@0.56.0
  - @graphql-mesh/utils@0.22.0

## 0.12.1

### Patch Changes

- Updated dependencies [1b332487c]
  - @graphql-mesh/types@0.55.0
  - @graphql-mesh/utils@0.21.1

## 0.12.0

### Minor Changes

- 875d0e48d: enhance: small improvements

### Patch Changes

- Updated dependencies [875d0e48d]
  - @graphql-mesh/utils@0.21.0

## 0.11.1

### Patch Changes

- Updated dependencies [761b16ed9]
  - @graphql-mesh/types@0.54.1
  - @graphql-mesh/utils@0.20.1

## 0.11.0

### Minor Changes

- 09f81dd74: GraphQL v16 compatibility
- 09f81dd74: GraphQL v16 compability

### Patch Changes

- Updated dependencies [09f81dd74]
- Updated dependencies [09f81dd74]
  - @graphql-mesh/types@0.54.0
  - @graphql-mesh/utils@0.20.0

## 0.10.2

### Patch Changes

- Updated dependencies [0dc08e5cc]
  - @graphql-mesh/utils@0.19.0

## 0.10.1

### Patch Changes

- Updated dependencies [6f57be0c1]
  - @graphql-mesh/types@0.53.0
  - @graphql-mesh/utils@0.18.1

## 0.10.0

### Minor Changes

- 811960cdc: feat(runtime): use factory functions for debug messages

### Patch Changes

- Updated dependencies [4ec7a14ba]
- Updated dependencies [811960cdc]
- Updated dependencies [6f5ffe766]
  - @graphql-mesh/utils@0.18.0
  - @graphql-mesh/types@0.52.0

## 0.9.27

### Patch Changes

- Updated dependencies [256abf5f7]
  - @graphql-mesh/types@0.51.0
  - @graphql-mesh/utils@0.17.2

## 0.9.26

### Patch Changes

- Updated dependencies [8c9b709ae]
  - @graphql-mesh/types@0.50.0
  - @graphql-mesh/utils@0.17.1

## 0.9.25

### Patch Changes

- Updated dependencies [7bd145769]
  - @graphql-mesh/utils@0.17.0

## 0.9.24

### Patch Changes

- Updated dependencies [472c5887b]
  - @graphql-mesh/utils@0.16.3

## 0.9.23

### Patch Changes

- Updated dependencies [6ce43ddac]
  - @graphql-mesh/types@0.49.0
  - @graphql-mesh/utils@0.16.2

## 0.9.22

### Patch Changes

- Updated dependencies [46a4f7b73]
- Updated dependencies [aa804d043]
- Updated dependencies [67552c8f8]
  - @graphql-mesh/utils@0.16.1
  - @graphql-mesh/types@0.48.0

## 0.9.21

### Patch Changes

- Updated dependencies [9eff8a396]
  - @graphql-mesh/types@0.47.0
  - @graphql-mesh/utils@0.16.0

## 0.9.20

### Patch Changes

- Updated dependencies [f4f30741d]
  - @graphql-mesh/utils@0.15.0

## 0.9.19

### Patch Changes

- Updated dependencies [4545fe72d]
- Updated dependencies [d189b4034]
- Updated dependencies [f23820ed0]
- Updated dependencies [06d688e70]
  - @graphql-mesh/types@0.46.0
  - @graphql-mesh/utils@0.14.0

## 0.9.18

### Patch Changes

- fc51c574d: Dependency updates
- Updated dependencies [fc51c574d]
  - @graphql-mesh/types@0.45.2
  - @graphql-mesh/utils@0.13.7

## 0.9.17

### Patch Changes

- Updated dependencies [1c2667489]
  - @graphql-mesh/types@0.45.1
  - @graphql-mesh/utils@0.13.6

## 0.9.16

### Patch Changes

- Updated dependencies [7080a2f1d]
  - @graphql-mesh/utils@0.13.5

## 0.9.15

### Patch Changes

- cb70939cc: fix(transforms): handle non nullable input variables correctly
- Updated dependencies [6266d1774]
- Updated dependencies [94606e7b9]
- Updated dependencies [2b8dae1cb]
- Updated dependencies [0c97b4b75]
  - @graphql-mesh/types@0.45.0
  - @graphql-mesh/utils@0.13.4

## 0.9.14

### Patch Changes

- Updated dependencies [25d10cc23]
  - @graphql-mesh/types@0.44.2
  - @graphql-mesh/utils@0.13.3

## 0.9.13

### Patch Changes

- 49c8ceb38: fix(core): bump packages to fix variables issue
- Updated dependencies [49c8ceb38]
  - @graphql-mesh/types@0.44.1
  - @graphql-mesh/utils@0.13.2

## 0.9.12

### Patch Changes

- Updated dependencies [1ee417e3d]
  - @graphql-mesh/types@0.44.0
  - @graphql-mesh/utils@0.13.1

## 0.9.11

### Patch Changes

- Updated dependencies [885ea439a]
- Updated dependencies [d8051f87d]
- Updated dependencies [d8051f87d]
  - @graphql-mesh/types@0.43.0
  - @graphql-mesh/utils@0.13.0

## 0.9.10

### Patch Changes

- Updated dependencies [bdb58dfec]
  - @graphql-mesh/utils@0.12.0

## 0.9.9

### Patch Changes

- Updated dependencies [7d0e33660]
  - @graphql-mesh/utils@0.11.4

## 0.9.8

### Patch Changes

- Updated dependencies [cfb517b3d]
  - @graphql-mesh/types@0.42.0

## 0.9.7

### Patch Changes

- 3c4c51100: enhance(runtime): skip validation on schema delegation
- Updated dependencies [3c4c51100]
  - @graphql-mesh/utils@0.11.3

## 0.9.6

### Patch Changes

- e6acdbd7d: enhance(runtime): do not compose unnecessary resolvers
- Updated dependencies [e6acdbd7d]
  - @graphql-mesh/types@0.41.1
  - @graphql-mesh/utils@0.11.2

## 0.9.5

### Patch Changes

- Updated dependencies [69c89666d]
  - @graphql-mesh/utils@0.11.1

## 0.9.4

### Patch Changes

- Updated dependencies [214b7a23c]
  - @graphql-mesh/types@0.41.0

## 0.9.3

### Patch Changes

- Updated dependencies [0d2f7bfcd]
  - @graphql-mesh/types@0.40.0

## 0.9.2

### Patch Changes

- Updated dependencies [1caa8ffd3]
  - @graphql-mesh/utils@0.11.0

## 0.9.1

### Patch Changes

- Updated dependencies [6c90e0e39]
  - @graphql-mesh/types@0.39.0

## 0.9.0

### Minor Changes

- 346fe9c61: Performance improvements and OData fixes

### Patch Changes

- Updated dependencies [346fe9c61]
  - @graphql-mesh/types@0.38.0
  - @graphql-mesh/utils@0.10.0

## 0.8.27

### Patch Changes

- Updated dependencies [4b57f7496]
- Updated dependencies [4b57f7496]
  - @graphql-mesh/types@0.37.0

## 0.8.26

### Patch Changes

- b77148a04: fix(npm-publish): bump all versions to publish again
- Updated dependencies [b77148a04]
  - @graphql-mesh/types@0.36.1
  - @graphql-mesh/utils@0.9.2

## 0.8.25

### Patch Changes

- Updated dependencies [634a8a134]
- Updated dependencies [6b8b23a4e]
- Updated dependencies [2c3312f1a]
- Updated dependencies [d12c7d978]
  - @graphql-mesh/types@0.36.0
  - @graphql-mesh/utils@0.9.1

## 0.8.24

### Patch Changes

- Updated dependencies [191a663a]
  - @graphql-mesh/types@0.35.1

## 0.8.23

### Patch Changes

- Updated dependencies [b9ca0c30]
  - @graphql-mesh/types@0.35.0
  - @graphql-mesh/utils@0.9.0

## 0.8.22

### Patch Changes

- Updated dependencies [ec89a923]
  - @graphql-mesh/utils@0.8.8

## 0.8.21

### Patch Changes

- Updated dependencies [55327fd6]
  - @graphql-mesh/types@0.34.1

## 0.8.20

### Patch Changes

- Updated dependencies [76051dd7]
  - @graphql-mesh/types@0.34.0

## 0.8.19

### Patch Changes

- Updated dependencies [646d6bdb]
  - @graphql-mesh/types@0.33.0

## 0.8.18

### Patch Changes

- Updated dependencies [68d6b117]
  - @graphql-mesh/types@0.32.0

## 0.8.17

### Patch Changes

- Updated dependencies [212f2d66]
  - @graphql-mesh/types@0.31.1

## 0.8.16

### Patch Changes

- Updated dependencies [77327988]
  - @graphql-mesh/types@0.31.0

## 0.8.15

### Patch Changes

- Updated dependencies [48f38a4a]
  - @graphql-mesh/types@0.30.1

## 0.8.14

### Patch Changes

- Updated dependencies [938cca26]
  - @graphql-mesh/types@0.30.0

## 0.8.13

### Patch Changes

- Updated dependencies [8ef29de1]
  - @graphql-mesh/types@0.29.4

## 0.8.12

### Patch Changes

- Updated dependencies [a02d86c3]
- Updated dependencies [a02d86c3]
- Updated dependencies [a02d86c3]
  - @graphql-mesh/types@0.29.3

## 0.8.11

### Patch Changes

- Updated dependencies [69d2198d]
  - @graphql-mesh/utils@0.8.7

## 0.8.10

### Patch Changes

- Updated dependencies [8e8848e1]
  - @graphql-mesh/types@0.29.2

## 0.8.9

### Patch Changes

- Updated dependencies [7e970f09]
  - @graphql-mesh/utils@0.8.6

## 0.8.8

### Patch Changes

- Updated dependencies [e8994875]
  - @graphql-mesh/types@0.29.1

## 0.8.7

### Patch Changes

- Updated dependencies [8d345721]
  - @graphql-mesh/utils@0.8.5

## 0.8.6

### Patch Changes

- Updated dependencies [c767df01]
- Updated dependencies [183cfa96]
- Updated dependencies [b3d7ecbf]
  - @graphql-mesh/types@0.29.0
  - @graphql-mesh/utils@0.8.4

## 0.8.5

### Patch Changes

- Updated dependencies [a22fc6f3]
  - @graphql-mesh/types@0.28.0

## 0.8.4

### Patch Changes

- Updated dependencies [c1de3e43]
  - @graphql-mesh/types@0.27.0

## 0.8.3

### Patch Changes

- Updated dependencies [75f6dff9]
- Updated dependencies [c4f207a7]
  - @graphql-mesh/types@0.26.0

## 0.8.2

### Patch Changes

- Updated dependencies [0df817d0]
  - @graphql-mesh/types@0.25.0

## 0.8.1

### Patch Changes

- Updated dependencies [08c2966e]
  - @graphql-mesh/utils@0.8.3

## 0.8.0

### Minor Changes

- 44348de0: Introduce merger-bare
