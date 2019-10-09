---
id: diffiehellman
title: Diffie-Hellman
sidebar_label: Diffie-Hellman
---

Bindings for the crypto_scalarmult API. [See the libsodium crypto_scalarmult docs for more information](https://download.libsodium.org/doc/advanced/scalar_multiplication).

``` js
crypto_scalarmult_base(publicKey, secretKey)
```
Create a scalar multiplication public key based on a secret key
* `publicKey` should be a `buffer` of length `crypto_scalarmult_BYTES`
* `secretKey` should be a `buffer` of length `crypto_scalarmult_SCALARBYTES`

The generated public key is stored in `publicKey`.

``` js
crypto_scalarmult(sharedSecret, secretKey, remotePublicKey)
```
Derive a shared secret from a local secret key and a remote public key.
* `sharedSecret` should be a `buffer` of length `crypto_scalarmult_BYTES`
* `secretKey` should be a `buffer` of length `crypto_scalarmult_SCALARBYTES`
* `remotePublicKey` should be a `buffer` of length `crypto_scalarmult_BYTES`

The generated shared secret is stored in `sharedSecret`.