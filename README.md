fips-log.c
=========

fipsified log.c ( https://github.com/rxi/log.c)

fips build system: https://github.com/floooh/fips

## How to integrate:

Add the dependency to your fips.yml file:

```yaml
imports:
    fips-log.c:
        git: https://github.com/darsausalo/fips-log.c
```

Use log.c as dependency in your targets:

```cmake
fips_begin_*(...)
    ...
    fips_deps(log.c)
fips_end_*(...)
```
