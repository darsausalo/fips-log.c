fips-logc
=========

fipsified logc ( https://github.com/rxi/logc)

fips build system: https://github.com/floooh/fips

## How to integrate:

Add the dependency to your fips.yml file:

```yaml
imports:
    fips-logc:
        git: https://github.com/darsausalo/fips-logc
```

Use logc as dependency in your targets:

```cmake
fips_begin_*(...)
    ...
    fips_deps(logc)
fips_end_*(...)
```
