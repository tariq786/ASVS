# V7: Cryptography Verification Requirements

## Control Objective

Ensure that a verified application satisfies the following high level requirements:

* That all cryptographic modules fail in a secure manner and that errors are handled correctly.
* That a suitable random number generator is used when randomness is required.
* That access to keys is managed in a secure way.

## Security Verification Requirements

| # | Description | L1 | L2 | L3 | Since |
| --- | --- | --- | --- | -- | -- |
| **7.2** | Verify that all cryptographic modules fail securely, and errors are handled in a way that does not enable Padding Oracle attacks. | ✓ | ✓ | ✓ | 1.0 |
| **7.6** | Verify that all random numbers, random file names, random GUIDs, and random strings are generated using the cryptographic module’s approved random number generator when these random values are intended to be not guessable by an attacker. |  | ✓ | ✓ | 1.0 |
| **7.7** | Verify that cryptographic algorithms used by the application have been validated against FIPS 140-2 or an equivalent standard. | ✓ | ✓ | ✓ | 1.0 |
| **7.11** | Verify that consumers of cryptographic services do not have direct access to key material, such as by using key vaults or API based alternatives. |  | ✓ | ✓ | 4.0 |
| **7.12** | Verify that Personally Identifiable Information (PII) and other sensitive data is stored encrypted while at rest. |  | ✓ | ✓ | 4.0 |
| **7.13** | Verify that sensitive passwords or key material maintained in memory is overwritten with zeros as soon as it is no longer required, to mitigate memory dumping attacks. |  | ✓ | ✓ | 4.0 |
| **7.14** | Verify that all keys and passwords are replaceable, and are generated or replaced at installation time. |  | ✓ | ✓ | 3.0 |
| **7.15** | Verify that random numbers are created with proper entropy even when the application is under heavy load, or that the application degrades gracefully in such circumstances. |  |  | ✓ | 3.0 |
| **7.16** | Verify that industry proven cryptographic modules are used instead of custom coded cryptography. | ✓ | ✓ | ✓ | 4.0 |

## References

For more information, see also:

* [OWASP Testing Guide 4.0: Testing for weak Cryptography](https://www.owasp.org/index.php/Testing_for_weak_Cryptography)
* [OWASP Cheat Sheet: Cryptographic Storage](https://www.owasp.org/index.php/Cryptographic_Storage_Cheat_Sheet)
