# Bearer Authorization

## Provided Reading Material

### [JWTs Explained](https://www.youtube.com/watch?v=926mknSW9Lo)

### [Intro to JWT](https://jwt.io/introduction/)

### [Are JWTs Secure?](https://stackoverflow.com/questions/27301557/if-you-can-decode-jwt-how-are-they-secure)

## My Notes:

### What is JWT?

- JSON Web Token is an open security standard
- It allows securely sending information between parties
- It is digitally signed to ensure the integrity of the information
- JWT's can be encrypted to provide secrecy between parties.
- Encrypted vs Signed
  - Encryption prevents the contents of a token from being read at all.
  - Signing prevents token forgery. The use of a signature ensures the delivered contents come from an authentic source.
- JWTs can be used for both secure information exchange and authorization.

### Public-Private key pairs

This is a concept I saw in the "Intro to JWT" reading which I researched and will try to explain.

- Public-Private key pairs are a part of a system known as [public-key cryptography](https://en.wikipedia.org/wiki/Public-key_cryptography).
  - It consists of sending data which is encoded using "one-way" mathematical computations and a "private key" as an input.
  - Then, someone can use a "public key" (mathematically related to the private key) to decoded the data and verify the identity of the creator.
  - This system prevents acceptance and generation of fake data by way of verifying the identity of the source, and obfuscating the private key by the one-way computations done with it.
  - If the wrong private key is used to sign data, it can't be decoded by the public key.
  - Data can be signed with the public key as well, but it can only be decoded by the private key.

### JWT Structure

JWT's consist of 3 parts, separated by dots: **Header** + **Payload** + **Signature**: `xxxx.yyyy.zzzz`

- The header consists of the signing algorithm and the token type (which will be `JWT` for a jwt), encoded in Base64
- The payload consists of claims, which are statements about the sender. There are 3 types of claims
  - Registered claims: claims with predefined definitions per the JWT docs
  - Public claims: Basically any data can be but into a public claim, but the [IANA JSON Web Token Registry](https://www.iana.org/assignments/jwt/jwt.xhtml) should be used to prevent namespace collision (two claims using the same key)
  - Private claims: Claims created to share information between the sender and final recipient which is not registered or public
  - The payload with whatever claims is encoded in Base64.
- The Signature is created from a totally unexplained combination of the encoded header, encoded payload and a secret.

### JWT Advantages

JWT has advantages in that JWTs take up less space, has less security holes that other methods, and JSON parsers are common in most programming languages.
