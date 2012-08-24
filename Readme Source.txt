
This archive contains the source code of extcv 0.7

Important
=========
You may use the source code contained in this archive only if you accept and
agree to be bound by the license terms contained in the file 'License.txt',
which is included in this archive.

Homepage: https://bitbucket.org/j0s3f/extcv/overview


Contents
========

Building extcv from the source code

A) Requirements for building extcv
B) Instructions for building extcv


Building extcv from the source code
===================================

A) Requirements for building extcv:
-----------------------------------

- Microsoft Visual C++ 2010 (Professional Edition or compatible)
- RSA Security Inc. PKCS #11 Cryptographic Token Interface (Cryptoki) 2.20 header
  files (available at ftp://ftp.rsasecurity.com/pub/pkcs/pkcs-11/v2-20)
- nasm assembler


B) Instructions for building extcv:
-----------------------------------

1) Copy the PKCS #11 header files to a standard include path or create
   an environment variable 'PKCS11_INC' pointing to the directory where
   the PKCS #11 header files are installed.

2) Open the 'extcv.sln' solution in Microsoft Visual Studio 2010.

5) Build the solution (projects 'Crypto' and 'extcv').

Note: The crypto library (Project 'Crypto.vcproj') is an unmodified version
of the TrueCrypt crypto library.

