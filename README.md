# Cache-Timing Attacks on AES

AES, like many cryptographic algorithms, is susceptible to **side-channel attacks** that exploit physical implementations rather than theoretical weaknesses. Among these, **cache-timing attacks** represent a significant threat, as they use the time variations in the execution of cryptographic operations to infer sensitive information about the secret key.

This project is motivated by work from **Daniel J. Bernstein**, who demonstrated the feasibility of extracting AES keys through cache-timing analysis. These attacks exploit the architectural characteristics of some CPUs to observe data access patterns and deduce information about the encryption processes. The vulnerability comes from the fact that hitting or missing the cache can lead to large, measurable differences in execution times. These differences can be analyzed to reveal information on possible encryption keys, thus compromising the encrypted data.

### Project Overview

This project creates a **simulation of the computer’s hardware** in order to emulate the mechanics of cache-timing attacks. This allows a detailed exploration of the attack’s dynamics and offers insight into the differences in execution time which stem from cache hits and misses.

In tandem with replicating cache-timing attacks, this project evaluates simulations of various countermeasures proposed by **Eran Tromer, Dag Arne Osvik, and Adi Shamir**. These countermeasures include:
- **Dynamic table storage**
- **Cache state normalization**
- **Process blocking**
