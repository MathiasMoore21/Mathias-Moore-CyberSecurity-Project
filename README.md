Secure File Transmission Using OTP and Extended Vigenère Cipher


This project demonstrates a secure sender–receiver communication system implemented in Python using socket programming and cryptographic techniques. A confidential file is encrypted using a One-Time Pad (OTP), and the OTP key itself is secured using an Extended Vigenère Cipher that supports the full 256-character ASCII set.

The system simulates how sensitive data can be securely transmitted across a network using layered encryption.

 How the System Works:

 Encryption (Sender – Program A):
1. Reads a plaintext file containing a simple message.
2. Generates a truly random One-Time Pad (OTP) key of equal length.
3. Encrypts the message using XOR with the OTP key.
4. Encrypts the OTP key using an Extended Vigenère Cipher with a pre-shared secret.
5. Sends:
   - The encrypted OTP key over Port 3500
   - The encrypted message over Port 3501

 Decryption (Receiver – Program B):
1. Listens on the designated ports for incoming data.
2. Receives and stores the encrypted OTP key and encrypted message.
3. Decrypts the OTP key using the Extended Vigenère Cipher.
4. Uses the decrypted OTP key to restore the original message using XOR.
5. Saves the decrypted file and prints the final decoded message to the screen.





Cryptographic Techniques Used

One-Time Pad (OTP)
  Provides perfect secrecy by XOR-ing the plaintext with a truly random key of equal length.

Extended Vigenère Cipher
  An enhanced version of the classical Vigenère Cipher that operates over the full 256-character ASCII range, allowing secure encryption of binary data.

How to Run:

1.	Make sure Python 3 is installed.
2.	Place Sender_A.py, Receiver_B.py, and Zelenskyy1.dat in the same directory.
3.	Open two terminal windows.
4.	In the first terminal, run: python Receiver_B.py
5.	In the second terminal, run: python Sender_A.py
6.	The decrypted message will be printed by the receiver and saved as Zelenskyy2.dat.

