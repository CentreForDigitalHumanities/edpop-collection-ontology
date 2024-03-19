# EDPOP collection ontology

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.10838554.svg)](https://doi.org/10.5281/zenodo.10838554)

This repository describes an [OWL ontology](https://en.wikipedia.org/wiki/Web_Ontology_Language) that is used in the [EDPOP VRE](https://github.com/UUDigitalHumanitieslab/EDPOP).

## Introduction

In the EDPOP VRE, users can create collections of resources and annotate them. This ontology describes the vocabulary and relationships that is used to manage collections and annotations.

The collection ontology is agnostic to the type of resources that are being collected and annotated. The EDPOP VRE allows users to collect and annotate records in bibliographical catalogues, you could use this vocabulary to describe collections of any linked data resources.

This means that this ontology does _not_ describe the structure of bibliographical data used in EDPOP - that is described in the [EDPOP record ontology](https://github.com/UUDigitalHumanitieslab/edpop-record-ontology).

## Related vocabularies

The ontology relies heavily on existing vocabularies. It is recommended that you familiarise yourself with these specifications before building implementations on the EDPOP collection ontology.

- [RDF](https://www.w3.org/TR/rdf12-schema/)
- [OWL](https://www.w3.org/TR/owl-features/)
- [Web Annotation Vocabulary](https://www.w3.org/TR/annotation-vocab/)
- [ActivityStreams](https://www.w3.org/ns/activitystreams)
- [FOAF](http://xmlns.com/foaf/)

## Content

### Repository contents

This repository contains:

- [ontology.ttl](/ontology.ttl): A formal, machine-readable description of the ontology
- [guidelines](/documentation/guidelines.md): A lengthy description of how the ontology can be used in a research environment.
- [example.ttl](/documentation/example.ttl): An small graph that implements the ontology.
- [test_validate.py](/tests/test_validate.py): A python test that verifies the turtle files in the repository are valid.

### File formats

The `ontology.ttl` and `example.ttl` are [Turtle files](https://en.wikipedia.org/wiki/Turtle_(syntax)). They describe RDF graphs.

Tests are written as [Python](https://www.python.org/) scripts (more detail below).

### Unit tests

The repository contains tests written in Python. These verify that the turtle files can be parsed without errors, which is useful for detecting typos. The tests do not verify the semantics of the ontology, such as whether it implements OWL correctly.

Tests are implemented in [pytest](https://docs.pytest.org/) and located in the [tests](/tests/) directory.

Python 3.8 or higher is required. You will also need [pip](https://pypi.org/project/pip/) to install packages. You can install packages with

```bash
pip install tests/requirements.txt
```

After that, run tests with

```bash
pytest
```

## Licence

This work is licensed under a [Creative Commons 4.0 Attribution Licence](https://creativecommons.org/licenses/by/4.0/). See [LICENCE](/LICENCE).

## Citation

If you wish to cite this ontology, please use the metadata provided in [CITATION.cff](/CITATION.cff).


