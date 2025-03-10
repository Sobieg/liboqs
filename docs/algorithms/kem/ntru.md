# NTRU

- **Algorithm type**: Key encapsulation mechanism.
- **Main cryptographic assumption**: NTRU in Z[x]/(q, x^n-1) with prime n and power-of-two q.
- **Principal submitters**: John M. Schanck.
- **Auxiliary submitters**: Cong Chen, Oussama Danba, Jeffrey Hoffstein, Andreas Hülsing, Joost Rijneveld, Tsunekazu Saito, Peter Schwabe, William Whyte, Keita Xagawa, Takashi Yamakawa, Zhenfei Zhang.
- **Authors' website**: https://ntru.org/
- **Specification version**: NIST Round 3 submission.
- **Implementation source**: https://github.com/PQClean/PQClean/commit/5b8ef3baea3ffdfbf688a3a1bb8f02de44a67ec0, which takes it from:
  - https://github.com/jschanck/ntru/tree/a43a4457
- **Implementation license (SPDX-Identifier)**: CC0-1.0.

## Parameter set summary

|   Parameter set   | Security model   |   Claimed NIST Level |   Public key size (bytes) |   Secret key size (bytes) |   Ciphertext size (bytes) |   Shared secret size (bytes) |
|:-----------------:|:-----------------|---------------------:|--------------------------:|--------------------------:|--------------------------:|-----------------------------:|
| NTRU-HPS-2048-509 | IND-CCA2         |                    1 |                       699 |                       935 |                       699 |                           32 |
| NTRU-HPS-2048-677 | IND-CCA2         |                    3 |                       930 |                      1234 |                       930 |                           32 |
| NTRU-HPS-4096-821 | IND-CCA2         |                    5 |                      1230 |                      1590 |                      1230 |                           32 |
|   NTRU-HRSS-701   | IND-CCA2         |                    3 |                      1138 |                      1450 |                      1138 |                           32 |

## NTRU-HPS-2048-509 implementation characteristics

|  Identifier in upstream  | Supported architecture(s)   | Supported operating system(s)   | CPU extension(s) used   | No branching-on-secrets claimed?   | No branching-on-secrets checked by valgrind?   | Large stack usage?‡   |
|:------------------------:|:----------------------------|:--------------------------------|:------------------------|:-----------------------------------|:-----------------------------------------------|:----------------------|
|          clean           | All                         | All                             | None                    | True                               | True                                           | False                 |
|           avx2           | x86\_64                     | Linux,Darwin                    | AVX2,BMI2               | True                               | True                                           | False                 |

Are implementations chosen based on runtime CPU feature detection? **Yes**.

 ‡For an explanation of what this denotes, consult the [Explanation of Terms](#explanation-of-terms) section at the end of this file.

## NTRU-HPS-2048-677 implementation characteristics

|  Identifier in upstream  | Supported architecture(s)   | Supported operating system(s)   | CPU extension(s) used   | No branching-on-secrets claimed?   | No branching-on-secrets checked by valgrind?   | Large stack usage?   |
|:------------------------:|:----------------------------|:--------------------------------|:------------------------|:-----------------------------------|:-----------------------------------------------|:---------------------|
|          clean           | All                         | All                             | None                    | True                               | True                                           | False                |
|           avx2           | x86\_64                     | Linux,Darwin                    | AVX2,BMI2               | True                               | True                                           | False                |

Are implementations chosen based on runtime CPU feature detection? **Yes**.

## NTRU-HPS-4096-821 implementation characteristics

|  Identifier in upstream  | Supported architecture(s)   | Supported operating system(s)   | CPU extension(s) used   | No branching-on-secrets claimed?   | No branching-on-secrets checked by valgrind?   | Large stack usage?   |
|:------------------------:|:----------------------------|:--------------------------------|:------------------------|:-----------------------------------|:-----------------------------------------------|:---------------------|
|          clean           | All                         | All                             | None                    | True                               | True                                           | False                |
|           avx2           | x86\_64                     | Linux,Darwin                    | AVX2,BMI2               | True                               | True                                           | False                |

Are implementations chosen based on runtime CPU feature detection? **Yes**.

## NTRU-HRSS-701 implementation characteristics

|  Identifier in upstream  | Supported architecture(s)   | Supported operating system(s)   | CPU extension(s) used   | No branching-on-secrets claimed?   | No branching-on-secrets checked by valgrind?   | Large stack usage?   |
|:------------------------:|:----------------------------|:--------------------------------|:------------------------|:-----------------------------------|:-----------------------------------------------|:---------------------|
|          clean           | All                         | All                             | None                    | True                               | True                                           | False                |
|           avx2           | x86\_64                     | Linux,Darwin                    | AVX2,BMI2               | True                               | True                                           | False                |

Are implementations chosen based on runtime CPU feature detection? **Yes**.

## Explanation of Terms

- **Large Stack Usage**: Implementations identified as having such may cause failures when running in threads or in constrained environments.