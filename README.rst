OpenIBAN - Python IBAN library
===============================

.. image:: https://travis-ci.org/nathanIL/openiban.svg
    :target: https://travis-ci.org/nathanIL/openiban

OpenIBAN is a generic library for interacting with various (currently only `openiban.com <https://openiban.com/>`_) IBAN
providers.

save open line IBAN validation

.. code-block:: python

    from openibanlib import openiban
    # By trying to initialize an IBAN object
    >>> try:
            openiban.IBAN('TR51 0006 2000 1780 0006 6240 13')
        except IBANFormatValidationException:
            print("Invalid IBAN provided")
    # Or using a static method
    >>> openiban.IBAN.format_validate('TR51 0006 2000 1780 0006 6240 13')
    True
    ...

On line (using an IBAN provider) validation

.. code-block:: python

    from openibanlib.providers.OpenIBAN import OpenIBAN
    ...
    
Installation
------------

To install simply (coming soon):

.. code-block:: bash

    $ pip install openiban-lib
