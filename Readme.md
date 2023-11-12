# Serpent_in_CBC_mode_for_microcontrollers

This repository contains code that enables you to easily integrate the Serpent encryption algorithm in CBC mode to your project.


## Compatibility

The code was successfully tested on the following boards:
- STM32F407VET6
- Teensy 4.1
- ESP32
- ESP8266


## Usage


```
  Serial.println("\nEncryption/Decryption Test:");
  String plaintext = "This string is encrypted with Serpent in Cipher Block Chaining mode!"; // String to be encrypted
  int iv[16]; // Initialization vector
  for (int i = 0; i < 16; i++){
    iv[i] = random(256); // Fill iv array with random numbers. I suggest you use a more secure method of random number generation!!!
  }
  encrypt_string_with_serpent_in_cbc(plaintext, iv); // Function for encryption. Takes the plaintext and iv as the input.
  Serial.println("\nCiphertext");
  Serial.println(string_for_data);
  String ciphertext = string_for_data; // Back the ciphertext up
  decrypt_string_with_serpent_in_cbc(ciphertext); // Decrypt data
  Serial.println("Plaintext:");
  Serial.println(string_for_data);
```
![image text](https://github.com/Northstrix/Serpent_in_CBC_mode_for_microcontrollers/blob/master/Pictures/Encryption%20and%20Decryption%20test.png)

## Visual representation of the encryption process
![image text](https://github.com/Northstrix/Serpent_in_CBC_mode_for_microcontrollers/blob/master/Pictures/Serpent%20in%20CBC.png)

## Copyright/Ownership

The library with the implementation of [serpent](https://github.com/peterferrie/serpent) by [peterferrie](https://github.com/peterferrie) is the propert of its rightful owner.

Original License:

Designers         Ross Anderson, Eli Biham, Lars Knudsen
First published   1998
Derived from      Square
Certification     AES finalist
Key sizes         128, 192 or 256 bits
Block sizes       128 bits
Structure         Substitution-permutation network
Rounds            32


  Copyright © 2015 Odzhan, Peter Ferrie. All Rights Reserved.

  Redistribution and use in source and binary forms, with or without
  modification, are permitted provided that the following conditions are
  met:

  1. Redistributions of source code must retain the above copyright
  notice, this list of conditions and the following disclaimer.

  2. Redistributions in binary form must reproduce the above copyright
  notice, this list of conditions and the following disclaimer in the
  documentation and/or other materials provided with the distribution.

  3. The name of the author may not be used to endorse or promote products
  derived from this software without specific prior written permission.

  THIS SOFTWARE IS PROVIDED BY AUTHORS "AS IS" AND ANY EXPRESS OR
  IMPLIED WARRANTIES, INCLUDING, BUT NOT LIMITED TO, THE IMPLIED
  WARRANTIES OF MERCHANTABILITY AND FITNESS FOR A PARTICULAR PURPOSE ARE
  DISCLAIMED. IN NO EVENT SHALL THE AUTHOR BE LIABLE FOR ANY DIRECT,
  INDIRECT, INCIDENTAL, SPECIAL, EXEMPLARY, OR CONSEQUENTIAL DAMAGES
  (INCLUDING, BUT NOT LIMITED TO, PROCUREMENT OF SUBSTITUTE GOODS OR
  SERVICES; LOSS OF USE, DATA, OR PROFITS; OR BUSINESS INTERRUPTION)
  HOWEVER CAUSED AND ON ANY THEORY OF LIABILITY, WHETHER IN CONTRACT,
  STRICT LIABILITY, OR TORT (INCLUDING NEGLIGENCE OR OTHERWISE) ARISING IN
  ANY WAY OUT OF THE USE OF THIS SOFTWARE, EVEN IF ADVISED OF THE
  POSSIBILITY OF SUCH DAMAGE.

Part of the code written by me (Northstrix) is covered by the MIT License:

MIT License

Copyright (c) 2023 Maxim Bortnikov

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
