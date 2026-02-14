stem_test_database
==================

This repository contains an example database for materials and motors from the
[stem](https://stefanmathis.github.io/stem_book/) simulation toolbox for
electric motors. It is usually included as a submodule in other crates of the
framework to provide materials and motors for unit and integration tests.

The individual files purposefully sometimes assign units to values and sometimes
don't. This is done to verify within the test framework that the deserialization
routines can deal with both cases. For example:
` mass_density: 7650.0 kg / m^3` results in the same value as
` mass_density: 7650.0` or ` mass_density: 7.65 to / m^3`.