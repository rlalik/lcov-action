## lcov-action

![Build and Test](https://github.com/danielealbano/lcov-action/workflows/Build%20and%20Test/badge.svg)

This action let you to run lcov with the needed parameters

## Inputs

### `gcov_tool`

**Required** Path to the gcov binary, by default `/usr/bin/gcov`.

It's possible to use `/usr/bin/gcov-7` and `/usr/bin/gcov-8`.

### `remove_patterns`

**Required** Comma separated list of simple name-matching patterns to remove from the build, can be empty.

### `output_lcov_info`

**Required** Output path for the lcov info, by default `coverage.info`

## Outputs

No outputs.

## Example usage

gcov 7 (version 7.5.0)
```yaml
uses: daalbano/lcov-action@v1.0.0
with:
  gcov_tool: /usr/bin/gcov-7
```

gcov 8 (version 8.4.0)
```yaml
uses: daalbano/lcov-action@v1.0.0
with:
  gcov_tool: /usr/bin/gcov-8
```

gcov 9 (version 9.3.0) - default
```yaml
uses: daalbano/lcov-action@v1.0.0
```

Remove the 3rdparties and benchmarks subfolder (and any path that would contain these two) from the code coverage
```yaml
uses: daalbano/lcov-action@v1.0.0
with:
  remove_patterns: 3rdparties,benchmarks
```

## Author

Copyright (C) 2020-2021 Daniele Salvatore Albano

## License 

BSD 2-Clause License
