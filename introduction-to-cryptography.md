# Introduction to Cryptography

<figure><img src=".gitbook/assets/Introduction to cryptography-THM room image.png" alt=""><figcaption></figcaption></figure>



**Task 1 Introduction**

*   You have received the following encrypted message:

    _“Xjnvw lc sluxjmw jsqm wjpmcqbg jg wqcxqmnvw; xjzjmmjd lc wjpm sluxjmw jsqm bqccqm zqy.” Zlwvzjxj Zpcvcol_

    You can guess that it is a quote. Who said it?

Miyamoto Musashi



**Task 2 Symmetric Encryption**

* Decrypt the file `quote01` encrypted (using AES256) with the key `s!kR3T55` using `gpg`. What is the third word in the file?

```
gpg --output original_message01.txt --decrypt quote01.txt.gpg
```

Do not waste time idling or thinking after you have set your goals.

Miyamoto Musashi

* Decrypt the file `quote02` encrypted (using AES256-CBC) with the key `s!kR3T55` using `openssl`. What is the third word in the file?

```
openssl aes-256-cbc -d -in quote02 -out original_message02.txt 
```

The true science of martial arts means practicing them in such a way that they will be useful at any time, and to teach them in such a way that they will be useful in all things. Miyamoto Musashi

* Decrypt the file `quote03` encrypted (using CAMELLIA256) with the key `s!kR3T55` using `gpg`. What is the third word in the file?

```
gpg --output m3.txt --decrypt quote03.txt.gpg
```

You must understand that there is more than one path to the top of the mountain. Miyamoto Musashi
