## Riecoin Vanitybech
Vanitybech is a tool that creates Riecoin Segwit addresses that start with a specific pattern. For example using the patern "test" the following address and it's corresponding private key can be generated.
```
Private Key:   40b7719b937872996271310242577b867cfe08f3e791f0f41fa80a24ce64795e
Address:       ric1qtest3y6wcqd4j9nvkrnc4s9c4zgvash8n50g46
```

Since Riecoin addresses are not reversable the only way to do this is to generate as many random private keys as possible, and check if their address matches the pattern. This is done repeatedly until a matching pattern is found.

## Estimated Time
Guessing a private key with the chosen prefix has an element of luck to it. The following table depicts a rough estimate on what should  be expected on a Ryzen 3600 desktop processor using all of it's 12 threads. Your results may vary.

| Prefix      | Eta (Ryzen 3600)|
| ------------- | ---------- |
|ric1q0        	  | 20 ms           |
|ric1q00           | 20 ms           |
|ric1q000          | 150 ms          |
|ric1q0000         | 10 s            |
|ric1q00000        | 5 min           |
|ric1q000000       | 3 hours         |
|ric1q0000000      | 3 days          |
|ric1q00000000     | 100 days        |
|ric1q000000000    | 10 years        |
|ric1q0000000000   | 350 years       |
|ric1q00000000000  | 10000 years     |


## Compilation (Ubuntu 20.10)
```
sudo apt install build-essential libgmp-dev libssl-dev autoconf libtool
make
```

## Example Usage
```
$ ./vanitygen -p ric1q0000
Pattern: ric1q0000
Generating BTC Address
[00:00:00:00][7 Kkey/s][Total 1][Eta 3 min]
[00:00:00:05][23 Kkey/s][Total 103638][Eta 51 sec]
[00:00:00:10][20 Kkey/s][Total 205645][Eta 57 sec]
[00:00:00:15][14 Kkey/s][Total 301861][Eta 81 sec]
[00:00:00:20][21 Kkey/s][Total 397760][Eta 55 sec]
[00:00:00:25][21 Kkey/s][Total 497344][Eta 56 sec]
[00:00:00:30][21 Kkey/s][Total 598619][Eta 55 sec]
[00:00:00:35][21 Kkey/s][Total 698003][Eta 56 sec]
[00:00:00:40][21 Kkey/s][Total 794843][Eta 56 sec]

Private Key:   ae2dc7320a6abb3cfeecb8ece453deb5d15a063e6d3cd830ae2644d1245c94f7
Address:       ric1q0000fayt6xl63wsa53flzshalf25d650kjqfwe
```

## Important Notes
When using this software double check the generated addresses using other implementations to make sure that everyting is working correctly. Do NOT send mainnet coins to generated addresses unless you make sure that the address matches the coresponding private key. Also, please do not use the addresses shown in this readme file as you will (probably) get robbed.
