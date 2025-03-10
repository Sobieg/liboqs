# HQC

- **Algorithm type**: Key encapsulation mechanism.
- **Main cryptographic assumption**: Syndrome decoding of structure codes (Hamming Quasi-Cyclic).
- **Principal submitters**: Carlos Aguilar Melchor, Nicolas Aragon, Slim Bettaieb, Olivier Blazy, Jurjen Bos, Jean-Christophe Deneuville, Philippe Gaborit, Edoardo Persichetti, Jean-Marc Robert, Pascal Véron, Gilles Zémor, Loïc Bidoux.
- **Authors' website**: https://pqc-hqc.org/
- **Specification version**: NIST Round 3 submission.
- **Implementation source**: https://github.com/PQClean/PQClean/commit/5b8ef3baea3ffdfbf688a3a1bb8f02de44a67ec0, which takes it from:
  - https://github.com/jschanck/package-pqclean/tree/29f79e72/hqc, which takes it from:
  - submission 2020-10-01 at https://pqc-hqc.org/implementation.html
- **Implementation license (SPDX-Identifier)**: Public domain.

## Parameter set summary

|  Parameter set  | Security model   |   Claimed NIST Level |   Public key size (bytes) |   Secret key size (bytes) |   Ciphertext size (bytes) |   Shared secret size (bytes) |
|:---------------:|:-----------------|---------------------:|--------------------------:|--------------------------:|--------------------------:|-----------------------------:|
|     HQC-128     | IND-CCA2         |                    1 |                      2249 |                      2289 |                      4481 |                           64 |
|     HQC-192     | IND-CCA2         |                    3 |                      4522 |                      4562 |                      9026 |                           64 |
|     HQC-256     | IND-CCA2         |                    5 |                      7245 |                      7285 |                     14469 |                           64 |

## HQC-128 implementation characteristics

|  Identifier in upstream  | Supported architecture(s)   | Supported operating system(s)   | CPU extension(s) used   | No branching-on-secrets claimed?   | No branching-on-secrets checked by valgrind?   | Large stack usage?‡   |
|:------------------------:|:----------------------------|:--------------------------------|:------------------------|:-----------------------------------|:-----------------------------------------------|:----------------------|
|          clean           | All                         | All                             | None                    | True                               | True                                           | False                 |
|           avx2           | x86\_64                     | Linux,Darwin                    | AVX2,BMI1,PCLMULQDQ     | False                              | True                                           | False                 |

Are implementations chosen based on runtime CPU feature detection? **Yes**.

 ‡For an explanation of what this denotes, consult the [Explanation of Terms](#explanation-of-terms) section at the end of this file.

## HQC-192 implementation characteristics

|  Identifier in upstream  | Supported architecture(s)   | Supported operating system(s)   | CPU extension(s) used   | No branching-on-secrets claimed?   | No branching-on-secrets checked by valgrind?   | Large stack usage?   |
|:------------------------:|:----------------------------|:--------------------------------|:------------------------|:-----------------------------------|:-----------------------------------------------|:---------------------|
|          clean           | All                         | All                             | None                    | True                               | True                                           | False                |
|           avx2           | x86\_64                     | Linux,Darwin                    | AVX2,BMI1,PCLMULQDQ     | False                              | True                                           | False                |

Are implementations chosen based on runtime CPU feature detection? **Yes**.

## HQC-256 implementation characteristics

|  Identifier in upstream  | Supported architecture(s)   | Supported operating system(s)   | CPU extension(s) used   | No branching-on-secrets claimed?   | No branching-on-secrets checked by valgrind?   | Large stack usage?   |
|:------------------------:|:----------------------------|:--------------------------------|:------------------------|:-----------------------------------|:-----------------------------------------------|:---------------------|
|          clean           | All                         | All                             | None                    | True                               | True                                           | False                |
|           avx2           | x86\_64                     | Linux,Darwin                    | AVX2,BMI1,PCLMULQDQ     | False                              | True                                           | True                 |

Are implementations chosen based on runtime CPU feature detection? **Yes**.

## Explanation of Terms

- **Large Stack Usage**: Implementations identified as having such may cause failures when running in threads or in constrained environments.