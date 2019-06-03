<img src="./doc-base/neo.png" align="right" height="70"/>

# NEO Specification

## Document format
In order to facilitate the contributions to the document, we decided to adopt pandoc format, which allows hybrid LaTeX + Markdown syntax.

### Base structure
The structure of the document consists of five files:
- specification.md : main document in Mardown + LaTeX (this file is automatically generated by `merge_sections.sh`)
- [metadata.yaml](doc-base/metadata.yaml) : document metadata (authors, abstract, ...)
- [style.pandoc](doc-base/style.pandoc) : document style (LaTeX headings)
- [eisvogel.latex](doc-base/eisvogel.latex) : base LaTeX template (Eisvogel template with small changes)
- [references.bib](doc-base/references.bib) : bibliography in BibTeX format

The sections are separated on `sections/` folder (these are used as source to generate `specification.md` file).

Current draft proposal includes 6 sections + references (this may be changed by community, as anything else!):
- [Introduction.md](sections/Introduction.md) : expected release date -> Q2+ 2019
- [Network.md](sections/Network.md) : expected release date -> Q4+ 2019
- [Numbers.md](sections/Numbers.md) : expected release date -> Q3+ 2019
- [Cryptography.md](sections/Cryptography.md) : expected release date -> Q4+ 2019
- [NeoVM.md](sections/NeoVM.md) : expected release date -> Q3+ 2019
- [NeoContract.md](sections/NeoContract.md) : expected release date -> Q4+ 2019
- [Consensus.md](sections/Consensus.md) : first released 14 March, 2019.
- References (automatically generated from [references.bib](doc-base/references.bib)): expected release date -> Q2+ 2019


## Build instructions (manual build)
Install pandoc and LaTeX base (try [pandoc](https://pandoc.org/try)). On debian-based linux, you can simply run `make install`, and all dependencies will be installed.

After pandoc and LaTeX base are available, you can simply run `make`, which will generate the specification paper pdf.

### Building specific section
Any section can be build using command `make section` and passing `SECTION` parameter.
For example: `make section SECTION=Consensus` will build section 08 (it will be stored on `build/Consensus.pdf`).

## Automatically building using docker
The easiest way to build is by using docker.

* Build the docker image using `docker_build.sh`

* Compile the specification paper using `docker_run.sh`

* Output will be generated as `build/neo-specification.pdf`

## How to contribute
If you know Neo technology and want to contribute, feel free to directly submit a Pull Request with the desired changes.
Initially, the idea is to create a broad and complete initial version of the document, which will be polished in the future.

## License

This repository is Free Culture license Creative Commons 4.0 International (CC BY 4.0) for all figures and externally copyrighted material.
As usual, every author shall keep the copyright of its own contribution and agree with the CC BY 4.0 license for the combined work.

Please, when contributing, be careful to only add figures covered by Creative Commons licenses, and give proper references to original sources.
When adding new original material to this project, contributor agrees that it will be covered by Free Culture license Creative Commons [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/).

The beautiful Pandoc/LaTeX template [Eisvogel](https://github.com/Wandmalfarbe/pandoc-latex-template/) is licensed by BSD 3-Clause License.