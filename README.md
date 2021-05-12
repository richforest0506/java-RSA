RSA Encryption
===

Java implementation of RSA encryption.

Introduction
------------
This program aims to provide the means to encrypt and decrypt files 
using the RSA algorithm.  
	
How to Use
---------- 
1. Create an instance of `RSAKeyGenerator`.
2. Call it's `makeKey()` method, passing in a constant to specify which kind of key should be returned.
   * `RSAKey.PUBLIC_KEY` for encrypting
   * `RSAKey.PRIVATE_KEY` for decrypting
   * `RSAKey.COMPLETE_KEY` for efficient decryption using the Chinese Remainder Theorum
3. Cast the `RSAKey` returned to the appropriate type of `RSAKey`.
   * `RSAPublicKey`
   * `RSAPrivateKey`
   * `RSACompleteKey`
4. Call the key's `use()` method, passing in the source and destination file paths.
   * the key will perform it's operation on the file specified by `source`
   * the key will write the result of it's operation to the file specified by `destination`

Additionally, `RSATest` now contains a main method for testing.  Useage is as follows:

   java com.ws.rsa.RSATest plaintext destination
   
where `plaintext` is the path to a readable file, and `destination` is the prefix to use for storage of files created during the tests.
