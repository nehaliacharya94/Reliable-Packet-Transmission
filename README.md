# Reliable Packet Transmission
_(Spring: January 2016 - May 2016)_

The aim of this project was to develop a simple network application program and to implement a simple end-to-end encryption and decryption application. I used Java and basic socket API programming for this assignment. The project was divided into three parts. 
>
* The first part was about writing a client/server program just to send and read the files. For example the client wants to send a confidential file to the server over an open network. 
>
<img width="405" alt="capture" src="https://user-images.githubusercontent.com/29523536/28008478-b86c24f2-6525-11e7-82e2-a6190c07c212.PNG">

* The second part of this project required me to implement the Advanced Encryption Standard (AES-128) encryption/decryption algorithm in the program. Now the file that the client wants to send will be first encrypted by the AES algorithm and the encrypted file will then be sent to the server as a binary file. When this encrypted file is received by the server, it will be decrypted and stored in a fixed directory in the server’s machine.
>
* The final part was about using another algorithm called the Diffie Hellman Key Exchange to exchange the keys between the client and server. For this key exchange to take place, when the client first makes request for connection, each side will use BBS to generate its own pseudo random numbers and then use Diffie-Hellman to obtain a common secret key between the client and the server. There was a condition that if the secret key is less than 128 bits, then we had to use Diffie-Hellman algorithm again to obtain another secret key and concatenate it to the previous key. This process kept repeating until we obtained a key of at least 128 bits and if the key length was greater than 128 bits then I discarded the few prefix bits to chunk it to 128 bits. 
>
<img width="407" alt="capture1" src="https://user-images.githubusercontent.com/29523536/28008556-0309f7aa-6526-11e7-8dee-86b76aa94e1e.PNG">
