| Nama | NRP |
| ------- | ------- |
| Adrian Ismu Arifianto | 5025211116  |

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

- Sequence Number: `0` (relative sequence number) & Sequence Number (raw): `1068969752`,
- Karena flag 0x012 menandakan segmen SYN ACK
- Acknowledgment number (raw): `4236649188`, Acknowledgement number diperoleh dengan menambahkan angka 1 pada sequence number dari segmen SYN (ACK = sequence number + 1).

## No.5
### Soal
What is the sequence number of the TCP segment containing the header of the HTTP POST command? How many bytes of data are contained in the payload (data) field of this TCP segment? Did all of the data in the transferred file alice.txt fit into this single segment?

### Jawab
![Screenshot 2023-10-16 220811](https://github.com/adrianismu/TCP-UDP/assets/71255346/e46c89de-5a26-4cff-ae5e-d871f2c24143)

- Sequence Number: `152041 (relative sequence number)` 
- Sequence Number (raw): `4236801228`
- TCP payload: `(1385 bytes)`
- Tidak
## No.6
### Soal
Consider the TCP segment containing the HTTP “POST” as the first segment in the data transfer part of the TCP connection.

### Jawab

![image](https://github.com/adrianismu/TCP-UDP/assets/71255346/2fd88341-f3f3-438b-a8ba-8bbcfeb2ad1b)


- At what time was the first segment (the one containing the HTTP POST) in the data-transfer part of the TCP connection sent? `0.24047`

- At what time was the ACK for this first data-containing segment received? `0.052671`

- What is the RTT for this first data-containing segment? `0.028624`

- What is the RTT value the second data-carrying TCP segment and its ACK? `0.028628`

## No.7
### Soal
Consider the TCP segment containing the HTTP “POST” as the first segment in the data transfer part of the TCP connection.

### Jawab

![Screenshot 2023-10-16 220935](https://github.com/adrianismu/TCP-UDP/assets/71255346/372efa48-cee5-4930-b818-1cb5e629cf02)

- frame: 4 : length = 32 + 1448 = `1480 bytes`

- frame: 5 : length = 32 + 1448 = `1480 bytes`

- frame: 6 : length = 32 + 1448 = `1480 bytes`

- frame: 9 : length = 32 + 1448 = `1480 bytes`

- Total length 1480 * 4 = `5920 bytes`

## No.8
### Soal
- What is the minimum amount of available buffer space advertised to the client by gaia.cs.umass.edu among these first four data-carrying TCP segments?
- Does the lack of receiver buffer space ever throttle the sender for these first four datacarrying segments?
### Jawab
- `13712`
- `Receiver buffer spacer` tidak pernah membatasi pengirim karena window size value selalu lebih besar dari length

## No.9
### Soal
- Are there any retransmitted segments in the trace file?
- What did you check for (in the trace) in order to answer this question?

### Jawab
- Yes
- Retransmitted segments dapat dideteksi melalui sequence number. Ketika melakukan pengiriman ulang, terdapat paket yang sequence number paket selanjutnya tidak lebih besar dari sequence number paket sebelumnya.


### No.10
### Soal
- How much data does the receiver typically acknowledge in an ACK among the first ten data-carrying segments sent from the client to gaia.cs.umass.edu?
- Can you identify cases where the receiver is ACKing every other received segment among these first ten data-carrying segments?

### Jawab
- `1448 byte`
- Jika data terdouble, segmen acking pada setiap segmen yang diterima, contohnya pada segmen kedua yang datanya terdouble dari `1448` menjadi `2896 byte`


## No.11
### Soal
What is the throughput (bytes transferred per unit time) for the TCP connection?
### Jawab

## No.12
### Soal
Use the Time-Sequence-Graph(Stevens) plotting tool to view the sequence number versus time plot of segments being sent from the client to the gaia.cs.umass.edu server.
### Jawab

## No.13
### Soal
These “fleets” of segments appear to have some periodicity. What can you say about the period?
### Jawab

# UDP

## No.1
### Soal
Select the first UDP segment in your trace.
- What is the packet number of this segment in the trace file?
- What type of application-layer payload or protocol message is being carried in this UDP segment?
- How many fields there are in the UDP header?

### Jawab
![image](https://github.com/adrianismu/TCP-UDP/assets/71255346/0bc9510a-ed9c-4dcc-863e-77c4910801f4)

- Paket 5
- SSDP
- 4 Field (source port, destination port, length, checksum)

## No.2
### Soal
By consulting the displayed information in Wireshark’s packet content field for this packet (or by consulting the textbook), what is the length (in bytes) of each of the UDP header fields?

### Jawab
![image](https://github.com/adrianismu/TCP-UDP/assets/71255346/253569d1-421e-434a-9fad-fb624ff05742)

Setiap field terdiri dari 16 bit (2 byte), karena ada 4 bidang, maka panjang masing-masing field header UDP adalah `8 byte`

## No.3
### Soal
The value in the Length field is the length of what?
### Jawab
![image](https://github.com/adrianismu/TCP-UDP/assets/71255346/253569d1-421e-434a-9fad-fb624ff05742)

Length dari payload 275 byte ditambah header 8 byte adalah `183 byte`

## No.4
### Soal
What is the maximum number of bytes that can be included in a UDP payload?
### Jawab
karena panjang field adalah 16 byte, nilai maksimumnya adalah 65.535, sementara header memiliki panjang 8 byte, maka payload maksimumnya adalah `65.527 byte`

## No.5
### Soal
What is the largest possible source port number?
### Jawab
`65.535`

## No.6
### Soal
What is the protocol number for UDP?
### Jawab
![image](https://github.com/adrianismu/TCP-UDP/assets/71255346/98f3a4c0-3eaa-4a51-98f7-3b1beae4a8cc)
`UDP = (17)`

## No.7
### Soal
Examine the pair of UDP packets in which your host sends the first UDP packet and the second UDP packet is a reply to this first UDP packet.

- What is the packet number of the first of these two UDP segments in the trace file?
- What is the packet number of the second of these two UDP segments in the trace file?
- Describe the relationship between the port numbers in the two packets.
### Jawab

![image](https://github.com/adrianismu/TCP-UDP/assets/71255346/2d323a7e-0122-4ff5-af15-520ac70177d5)


- Paket 15
- Paket 17
- Source port untuk paket 15 adalah port tujuan untuk paket 17 dan dapat sebaliknya
