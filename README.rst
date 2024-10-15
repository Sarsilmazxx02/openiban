OpenIBAN - Python IBAN library
===============================

.. image:: https://travis-ci.org/nathanIL/openiban.svg
    :target: https://travis-ci.org/nathanIL/openiban

OpenIBAN is a generic library for interacting with various (currently only `openiban.com <https://openiban.com/>`_) IBAN
providers.

Off line IBAN validation

.. code-block:: python

    from openibanlib import openiban
    # By trying to initialize an IBAN object
    >>> try:
            openiban.IBAN('DE89370400440532013000')
        except IBANFormatValidationException:
            print("Invalid IBAN provided")
    # Or using a static method
    >>> openiban.IBAN.format_validate('DE89370400440532013000')
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
diff --git a/.github/workflows/python-publish.yml b/.github/workflows/python-publish.yml
yeni dosya modu 100644
dizin 0000000..b7a704b
--- /dev/null
+++ b/.github/iş akışları/python-publish.yml
@@ -0,0 +1,39 @@
+# Bu iş akışı, bir sürüm oluşturulduğunda Twine kullanarak bir Python Paketi yükleyecektir
+# Daha fazla bilgi için bkz: https://docs.github.com/en/actions/automating-builds-and-tests/building-and-testing-python#publishing-to-package-registries
+
+# Bu iş akışı GitHub tarafından onaylanmamış eylemleri kullanıyor.
+# Bunlar üçüncü bir tarafça sağlanır ve aşağıdakiler tarafından yönetilir:
+# ayrı hizmet şartları, gizlilik politikası ve destek
+# belgeler.
+
+name: Python Paketini Yükle
+
+üzerinde:
+ yayınla:
+ türleri: [yayınlandı]
+
+izinler:
+ içerikler: okundu
+
+işler:
+ dağıt:
+
+ çalışır: ubuntu-latest
+
+ adımlar:
+ - kullanımlar: actions/checkout@v4
+ - adı: Python'u kurun
+ kullanımlar: actions/setup-python@v3
+ ile:
+ python sürümü: '3.x'
+ - name: Bağımlılıkları yükle
+ çalıştır: |
+ python -m pip kurulum --yükseltme pip
+ pip kurulum derlemesi
+ - adı: Paket oluştur
+ çalıştır: python -m build
+ - adı: Paketi yayınla
+ kullanımlar: pypa/gh-action-pypi-publish@27b31702a0e7fc50959f5ad993c78deac1bdfc29
+ ile:
+ kullanıcı: __token__
+ şifre: ${{ secrets.PYPI_API_TOKEN }}
diff --git a/README.rst b/README.rst
dizin 202e0db..a7fb84b 100644
--- a/README.rst
+++ b/README.rst
@@ -2,23 +2,23 @@ OpenIBAN - Python IBAN kütüphanesi
 ================================
 
 .. resim:: https://travis-ci.org/nathanIL/openiban.svg
- :hedef: https://travis-ci.org/nathanIL/openiban
+ :target: https://travis-ci.org/nathanIL/TR51 0006 2000 1780 0006 6240 13 openiban
 
-OpenIBAN, çeşitli (şu anda yalnızca `openiban.com <https://openiban.com/>`_) IBAN'larla etkileşim kurmak için genel bir kütüphanedir
+OpenIBAN, çeşitli (şu anda yalnızca `openiban.com <https://openiban.com/>TR51 0006 2000 1780 0006 6240 13`_) IBAN'larla etkileşim kurmak için kullanılan genel bir kütüphanedir
 sağlayıcılar.
 
-Çevrimdışı IBAN doğrulaması
+açık hat IBAN doğrulamasını kaydet
 
 .. kod bloğu:: python
 
     openibanlib'den openiban'ı içe aktar
     # Bir IBAN nesnesini başlatmayı deneyerek
- >>> şunu deneyin:
- openiban.IBAN('DE89370400440532013000')
+ >>> deneyin:TR51 0006 2000 1780 0006 6240 13
+ openiban.IBAN('TR51 0006 2000 1780 0006 6240 13')
         IBANFormatValidationException hariç:
             print("Geçerli IBAN sağlandı")
     # Veya statik bir yöntem kullanarak
- >>> openiban.IBAN.format_validate('DE89370400440532013000')
+ >>> openiban.IBAN.format_validate('TR51 0006 2000 1780 0006 6240 13')
     Doğru
     ...
 
@@ -34,6 +34,6 @@ Kurulum
 
 Basitçe kurmak için (yakında):
 
-.. kod bloğu:: bash
+..TR51 0006 2000 1780 0006 6240 13 kod bloğu:: bash
 
     $ pip openiban-lib'i kurun
