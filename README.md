# signatures
A collection of signature files for NJOY projects. A signature file is a JSON file that gives the specific commit of the repository as well as the commits for each of the dependencies. This signature file can be used to accurately reproduce a repository and each of its dependencies at a given point in time.

## Projects
So far, we are automatically generating signatures for these projects whenever a change is made to the master (i.e., production) branch:

- [NJOY21](https://github.com/njoy/NJOY21)
- [NJOY2016](https://github.com/njoy/NJOY2016)
- [ENDFtk](https://github.com/njoy/ENDFtk)
- [ACEtk](https://github.com/njoy/ACEtk)
- [utility](https://github.com/njoy/utility)
- [header-utilities](https://github.com/njoy/header-utilities)
- [njoy_c_bindings](https://github.com/njoy/njoy_c_bindings)


## Generating Signatures
Signatures are created using [metaconfigure](https://github.com/njoy/metaconfigure):

    metaconfigure/signatures.py <filename>

Metaconfigure is a package used by all of NJOY projects that will generate the files necessary to build the project.

## Using a signature
To use a signature to checkout and build a project at a previous point in time, do the following&mdash;after cloning the repository:

```bash
./metaconfigure/fetch_subprojects.py <signature_file.json>

# Configure
cmake -D fetched_subprojects=true </path/to/CMakeLists.txt>
```
After the project has been configured, continue to build/test/install the project as before.

## License
This software is distributed according to the terms specified in the [LICENSE](LICENSE) file.
