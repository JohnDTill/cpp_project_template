# cpp-project-template
This template exists to consolidate my idea of best practice for the kind of C++ project I typically tackle. Components which I want to capture here are:
- [ ] vcpkg external library management
  - [x] QtCreator integration
  - [ ] VSCode integration
- [ ] "test" directory for integration tests
- [ ] "meta" directory for code generation step prior to C++ project build
- [ ] "installer" directory for QtInstaller providing easy Windows installation and registering associated file types
- [ ] ".github/workflows" directory for automated CI tests
  - [x] Unfinished work check
  - [ ] Integration tests
    - [ ] Matrix of various OS and compiler targets
    - [ ] Smoke tests for all commits, extensive tests for MRs against main
  - [ ] Tests of "meta" Python code

vcpkg is preferred instead of conan because of frequent dependence on LGPL-licensed libraries which have less obligations when dynamic linking. conan leaves it up to the package maintainers to specify if a package is shared (dynamically linked), which results in gaps like Windows lacking a shared package for GMP. vcpkg provides the linking option to the package recipient for all packages.

## Since I want the template to include readme images...
here is one of my favourite comics about programming:
![A comic illustrating the danger of "if(x=true)"](doc/readme/assign_instead_of_equality_blunder.jpg?raw=true "Some helpful or witty hovertip")

### Since I'm enjoying this a bit too much...
![How to tell when you're a real professional- man sat at piano thinking: "I don't enjoy this at all anymore"](doc/readme/how_to_tell_when_you're_a_real_professional.png?raw=true "Another helpful or witty hovertip")

# Installation
TEMPLATE: fill in or delete section

## Windows
TEMPLATE: fill in or delete section

## Linux
TEMPLATE: fill in or delete section

# Development Prerequisites
TEMPLATE: fill in or delete section

# License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details. Project dependencies are subject to their own license conditions.

# Contributing
TEMPLATE: fill in or delete section

# CI Status

[![C++ Integration Tests](https://github.com/JohnDTill/cpp_project_template/actions/workflows/cpp_integration_tests.yml/badge.svg)](https://github.com/JohnDTill/cpp_project_template/actions/workflows/cpp_integration_tests.yml)

[![Finished work](https://github.com/JohnDTill/cpp_project_template/actions/workflows/to-do_check.yml/badge.svg)](https://github.com/JohnDTill/cpp_project_template/actions/workflows/to-do_check.yml)
