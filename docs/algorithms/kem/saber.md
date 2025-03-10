# SABER

- **Algorithm type**: Key encapsulation mechanism.
- **Main cryptographic assumption**: Module learning with rounding.
- **Principal submitters**: Jan-Pieter D'Anvers, Angshuman Karmakar, Sujoy Sinha Roy, Frederik Vercauteren.
- **Authors' website**: https://www.esat.kuleuven.be/cosic/pqcrypto/saber/
- **Specification version**: NIST Round 3 submission.
- **Implementation source**: https://github.com/PQClean/PQClean/commit/5b8ef3baea3ffdfbf688a3a1bb8f02de44a67ec0, which takes it from:
  - https://github.com/jschanck/package-pqclean/tree/1ae84c3c/saber, which takes it from:
  - https://github.com/KULeuven-COSIC/SABER/tree/509cc5ec3a7e12a751ccdd2ef5bd6e54e00bd350
- **Implementation license (SPDX-Identifier)**: Public domain.

## Parameter set summary

|  Parameter set  | Security model   |   Claimed NIST Level |   Public key size (bytes) |   Secret key size (bytes) |   Ciphertext size (bytes) |   Shared secret size (bytes) |
|:---------------:|:-----------------|---------------------:|--------------------------:|--------------------------:|--------------------------:|-----------------------------:|
| LightSaber-KEM  | IND-CCA2         |                    1 |                       672 |                      1568 |                       736 |                           32 |
|    Saber-KEM    | IND-CCA2         |                    3 |                       992 |                      2304 |                      1088 |                           32 |
|  FireSaber-KEM  | IND-CCA2         |                    5 |                      1312 |                      3040 |                      1472 |                           32 |

## LightSaber-KEM implementation characteristics

|  Identifier in upstream  | Supported architecture(s)   | Supported operating system(s)   | CPU extension(s) used   | No branching-on-secrets claimed?   | No branching-on-secrets checked by valgrind?   | Large stack usage?‡   |
|:------------------------:|:----------------------------|:--------------------------------|:------------------------|:-----------------------------------|:-----------------------------------------------|:----------------------|
|          clean           | All                         | All                             | None                    | True                               | True                                           | False                 |
|           avx2           | x86\_64                     | Linux,Darwin                    | AVX2                    | False                              | True                                           | False                 |

Are implementations chosen based on runtime CPU feature detection? **Yes**.

 ‡For an explanation of what this denotes, consult the [Explanation of Terms](#explanation-of-terms) section at the end of this file.

## Saber-KEM implementation characteristics

|  Identifier in upstream  | Supported architecture(s)   | Supported operating system(s)   | CPU extension(s) used   | No branching-on-secrets claimed?   | No branching-on-secrets checked by valgrind?   | Large stack usage?   |
|:------------------------:|:----------------------------|:--------------------------------|:------------------------|:-----------------------------------|:-----------------------------------------------|:---------------------|
|          clean           | All                         | All                             | None                    | True                               | True                                           | False                |
|           avx2           | x86\_64                     | Linux,Darwin                    | AVX2                    | False                              | True                                           | False                |

Are implementations chosen based on runtime CPU feature detection? **Yes**.

## FireSaber-KEM implementation characteristics

|  Identifier in upstream  | Supported architecture(s)   | Supported operating system(s)   | CPU extension(s) used   | No branching-on-secrets claimed?   | No branching-on-secrets checked by valgrind?   | Large stack usage?   |
|:------------------------:|:----------------------------|:--------------------------------|:------------------------|:-----------------------------------|:-----------------------------------------------|:---------------------|
|          clean           | All                         | All                             | None                    | True                               | True                                           | False                |
|           avx2           | x86\_64                     | Linux,Darwin                    | AVX2                    | False                              | True                                           | False                |

Are implementations chosen based on runtime CPU feature detection? **Yes**.

## Explanation of Terms

- **Large Stack Usage**: Implementations identified as having such may cause failures when running in threads or in constrained environments.