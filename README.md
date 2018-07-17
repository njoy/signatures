# signatures
A collection of signature files for NJOY projects. A signature file is a JSON file that gives the specific commit of the repository as well as the commits for each of the dependencies. This signature file can be used to accurately reproduce a repository and each of its dependencies at a given point in time.

## Generating Signatures
Signatures are created using [metaconfigure](https://github.com/njoy/metaconfigure):

    metaconfigure/signatures.py <filename>

Metaconfigure is a package used by all of NJOY projects that will generate the files necessary to build the project.

## License
This software is distributed according to the terms specified in the [LICENSE](LICENSE) file.
