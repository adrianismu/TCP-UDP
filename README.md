# Nama
Nama  : Adrian Ismu Arifianto

NRP   : 5025211116

# TCP

## No.1
### Soal
What is the IP address and TCP port number used by the client computer (source) that is transferring the file to gaia.cs.umass.edu?
### Jawab

![Screenshot 2023-10-16 220346](https://github.com/adrianismu/TCP-UDP/assets/71255346/3a4f0d6f-7a1b-4c8c-bcf1-16598432725c)

IP address: `192.168.86.68`

Port: `55639`

## No.2
### Soal
What is the IP address of gaia.cs.umass.edu? On what port number is it sending and receiving TCP segments for this connection?
### Jawab

![Screenshot 2023-10-16 220356](https://github.com/adrianismu/TCP-UDP/assets/71255346/2ad46cd4-be93-4e4b-b1bc-0c35fd9a13c0)

Port: `80`

## No.3
### Soal
What is the sequence number of the TCP SYN segment that is used to initiate the TCP connection between the client computer and gaia.cs.umass.edu? What is it in this TCP segment that identifies the segment as a SYN segment? Will the TCP receiver in this session be able to use Selective Acknowledgments?
### Jawab

![Screenshot 2023-10-16 220356](https://github.com/adrianismu/TCP-UDP/assets/71255346/ff0b045a-5823-4c4b-a346-2ebad482894c)

sequence number (raw) = `1068969752`


## No.4
### Soal
What is the sequence number of the SYNACK segment sent by gaia.cs.umass.edu to the client computer in reply to the SYN? What is it in the segment that identifies the segment as a SYNACK segment? What is the value of the Acknowledgement field in the SYNACK segment? How did gaia.cs.umass.edu determine that value?
### Jawab

![Screenshot 2023-10-16 220554](https://github.com/adrianismu/TCP-UDP/assets/71255346/cd6c3dc0-6ccc-44cd-8d2d-48d4dd1d5a4c)


## No.5
### Soal
What is the sequence number of the TCP segment containing the header of the HTTP POST command? How many bytes of data are contained in the payload (data) field of this TCP segment? Did all of the data in the transferred file alice.txt fit into this single segment?

### Jawab
![Screenshot 2023-10-16 220811](https://github.com/adrianismu/TCP-UDP/assets/71255346/e46c89de-5a26-4cff-ae5e-d871f2c24143)

Sequence Number: `152041 (relative sequence number)` 

Sequence Number (raw): `4236801228`

TCP payload: `(1385 bytes)`

## No.6
### Soal
### Jawab

## No.7
### Soal
Consider the TCP segment containing the HTTP “POST” as the first segment in the data transfer part of the TCP connection.

### Jawab

![Screenshot 2023-10-16 220935](https://github.com/adrianismu/TCP-UDP/assets/71255346/372efa48-cee5-4930-b818-1cb5e629cf02)

frame: 4 : length = 32 + 1448 = `1480 bytes`

frame: 5 : length = 32 + 1448 = `1480 bytes`

frame: 6 : length = 32 + 1448 = `1480 bytes`

frame: 9 : length = 32 + 1448 = `1480 bytes`

Total length 1480 * 4 = `5920 bytes`


