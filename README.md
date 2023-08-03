# python-paillier 
![GitHub Workflow Status (with event)](https://img.shields.io/github/actions/workflow/status/sylvainpelissier/python-paillier/build.yml) ![GitHub Workflow Status (with event)](https://img.shields.io/github/actions/workflow/status/sylvainpelissier/python-paillier/test.yml?label=Unit%20Test)



A Python 3 library implementing the Paillier Partially Homomorphic Encryption.

The homomorphic properties of the paillier crypto system are:

-  Encrypted numbers can be multiplied by a non encrypted scalar.
-  Encrypted numbers can be added together.
-  Encrypted numbers can be added to non encrypted scalars.

Citing
======

`python-paillier` is designed, developed and supported by `CSIRO's Data61 <https://www.data61.csiro.au/>`__. If
you use any part of this library in your research, please cite it using the following BibTex entry::

    @misc{PythonPaillier,
      author = {CSIRO's Data61},
      title = {Python Paillier Library},
      year = {2013},
      publisher = {GitHub},
      journal = {GitHub Repository},
      howpublished = {\url{https://github.com/data61/python-paillier}},
    }


Running unit tests
------------------

::

   python setup.py test

Or use nose::

   nosetests


Note related to gmpy2
---------------------

`gmpy2` is not required to use the library, but is preferred. A pure Python implementation is available but 
`gmpy2` drastically improves performances. As indication on a laptop not dedicated to benchmarking, running the example
`examples/federated_learning_with_encryption.py` provided in the library took:
- 4.5s with `gmpy2` installed
- 35.7s without `gmpy2` installed

However, `gmpy2` is a requirement to run the tests.

Code History
------------

Developed at `Data61 | CSIRO <http://data61.csiro.au>`_.

Parts derived from the Apache licensed Google project:
https://code.google.com/p/encrypted-bigquery-client/
