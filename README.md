
| **Documentation**                                                               | **PackageEvaluator**                                                                            | **Build Status**                                                                                |
|:-------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------:|
| [![][docs-stable-img]][docs-stable-url] [![][docs-latest-img]][docs-latest-url] |[![][license-img]][license-url]   | [![][travis-img]][travis-url] |

[docs-stable-img]: https://img.shields.io/badge/docs-latest-blue.svg
[docs-stable-url]: https://weecology.github.io/Retriever.jl/latest/
[docs-latest-img]: https://readthedocs.org/projects/retrieverjl/badge/?version=latest
[docs-latest-url]: https://weecology.github.io/Retriever.jl/latest/
[travis-img]: https://travis-ci.org/weecology/Retriever.jl.svg?branch=master
[travis-url]: https://travis-ci.org/weecology/Retriever.jl
[license-img]: http://img.shields.io/badge/license-MIT-blue.svg
[license-url]: https://raw.githubusercontent.com/weecology/Retriever.jl/master/LICENSE


# Retriever
Julia wrapper for the Data Retriever software.

Data Retriever automates the tasks of finding, downloading, 
and cleaning up publicly available data, and then stores them in a local database or as .csv files. 
Simply put, it's a package manager for data. 
This allows data analysts to spend a majority of their time in analysing rather than in cleaning up or managing data.

## Installation

To use Retriever, you first need to [install Retriever](http://www.data-retriever.org), a core python package.

### Database Management Systems

Depending on the database management systems you wish to use, follow the `Setting up servers` [documentation of the retriever](https://github.com/weecology/retriever). You can change the credentials to suit your server settings.

The Retriever Julia package depends on a few Julia packages that will be installed automatically.

Ensure that Pycall is using the same Python path where the retriever Python package is installed.

You can change that path to a desired path as below.

```julia

julia> ENV["PYTHON"]="Python path where the retriever python package is installed"
# Build Pycall to enable the use of the new path
Pkg.build("PyCall")

```

To install Retriever Julia package


```julia

julia> Pkg.add("Retriever")

```

To install from Source, download or checkout the source from the [github page](https://github.com/weecology/Retriever.jl.git).

Go to `Retriever.jl/src`. Run Julia.

```Julia

julia> include("Retriever.jl")

```

To create docs

```Shell

julia --color=yes make.jl

```

or simply

```Shell

julia make.jl

```

(Note: If you want help in installing Julia you can follow this [tutorial](https://medium.com/@shivamnegi2019/julia-beginners-guide-part-1-a9c369128c78)

Acknowledgments
---------------

Development of this software is funded by [the Gordon and Betty Moore
Foundation's Data-Driven Discovery
Initiative](http://www.moore.org/programs/science/data-driven-discovery) through
[Grant GBMF4563](http://www.moore.org/grants/list/GBMF4563) to Ethan White and
started as [Shivam Negi](https://www.linkedin.com/in/shivam-negi-64a227103/)'s [Google Summer of Code](https://summerofcode.withgoogle.com/)
