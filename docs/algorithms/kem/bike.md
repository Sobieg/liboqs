# BIKE

- **Algorithm type**: Key encapsulation mechanism.
- **Main cryptographic assumption**: QC-MDPC (Quasi-Cyclic Moderate Density Parity-Check).
- **Principal submitters**: Nicolas Aragon, Paulo Barreto, Slim Bettaieb, Loic Bidoux, Olivier Blazy, Jean-Christophe Deneuville, Phillipe Gaborit, Santosh Gosh, Shay Gueron, Tim Güneysu, Carlos Aguilar Melchor, Rafael Misoczki, Edoardo Persichetti, Nicolas Sendrier, Jean-Pierre Tillich, Valentin Vasseur, Gilles Zémor.
- **Authors' website**: http://bikesuite.org/
- **Specification version**: 4.1.
- **Implementation source**: https://github.com/awslabs/bike-kem, which takes it from:
  - https://bikesuite.org/files/v4.1/Reference_Implementation.2020.10.20.2.zip
- **Implementation license (SPDX-Identifier)**: Apache-2.0.

## Parameter set summary

|  Parameter set  | Security model   |   Claimed NIST Level |   Public key size (bytes) |   Secret key size (bytes) |   Ciphertext size (bytes) |   Shared secret size (bytes) |
|:---------------:|:-----------------|---------------------:|--------------------------:|--------------------------:|--------------------------:|-----------------------------:|
|     BIKE-L1     | IND-CPA          |                    1 |                      1541 |                      5223 |                      1573 |                           32 |
|     BIKE-L3     | IND-CPA          |                    3 |                      3083 |                     10105 |                      3115 |                           32 |

## BIKE-L1 implementation characteristics

|  Identifier in upstream  | Supported architecture(s)   | Supported operating system(s)   | CPU extension(s) used   | No branching-on-secrets claimed?   | No branching-on-secrets checked by valgrind?   | Large stack usage?‡   |
|:------------------------:|:----------------------------|:--------------------------------|:------------------------|:-----------------------------------|:-----------------------------------------------|:----------------------|
|          master          | little endian               | All                             | None                    | True                               | True                                           | False                 |
|          master          | x86\_64                     | Linux,Darwin                    | AVX2,AVX512,PCLMUL,SSE2 | True                               | True                                           | False                 |

Are implementations chosen based on runtime CPU feature detection? **Yes**.

 ‡For an explanation of what this denotes, consult the [Explanation of Terms](#explanation-of-terms) section at the end of this file.

## BIKE-L3 implementation characteristics

|  Identifier in upstream  | Supported architecture(s)   | Supported operating system(s)   | CPU extension(s) used   | No branching-on-secrets claimed?   | No branching-on-secrets checked by valgrind?   | Large stack usage?   |
|:------------------------:|:----------------------------|:--------------------------------|:------------------------|:-----------------------------------|:-----------------------------------------------|:---------------------|
|          master          | little endian               | All                             | None                    | True                               | True                                           | False                |
|          master          | x86\_64                     | Linux,Darwin                    | AVX2,AVX512,PCLMUL,SSE2 | True                               | True                                           | False                |

Are implementations chosen based on runtime CPU feature detection? **Yes**.

## Explanation of Terms

- **Large Stack Usage**: Implementations identified as having such may cause failures when running in threads or in constrained environments.