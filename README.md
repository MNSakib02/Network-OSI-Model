# 7 layers of the OSI Model?

The 7 layers of the OSI model can be defined as follows, from top to bottom:
1. The application layer
The Application Layer: content requested and returned in required format
![osi_model_application_layer_7](https://github.com/MNSakib02/Network-OSI-Model/assets/58394125/f5b5b418-6e52-4038-b8f6-ac846d9b3d90)


This is the only layer that directly interacts with data from the user. Software applications like web browsers and email clients rely on the application layer to initiate communications. But it should be made clear that client software applications are not part of the application layer; rather the application layer is responsible for the protocols and data manipulation that the software relies on to present meaningful data to the user.

Application layer protocols include HTTP as well as SMTP (Simple Mail Transfer Protocol is one of the protocols that enables email communications).

2. The presentation layer
The Presentation Layer: encryption, compression, translation
![osi_model_presentation_layer_6](https://github.com/MNSakib02/Network-OSI-Model/assets/58394125/f12bd106-ff01-4686-8334-9152ee2c866d)


This layer is primarily responsible for preparing data so that it can be used by the application layer; in other words, layer 6 makes the data presentable for applications to consume. The presentation layer is responsible for translation, encryption, and compression of data.

Two communicating devices communicating may be using different encoding methods, so layer 6 is responsible for translating incoming data into a syntax that the application layer of the receiving device can understand.

If the devices are communicating over an encrypted connection, layer 6 is responsible for adding the encryption on the sender’s end as well as decoding the encryption on the receiver's end so that it can present the application layer with unencrypted, readable data.

Finally the presentation layer is also responsible for compressing data it receives from the application layer before delivering it to layer 5. This helps improve the speed and efficiency of communication by minimizing the amount of data that will be transferred.

3. The session layer
The Session Layer: session of communication
![osi_model_session_layer_5](https://github.com/MNSakib02/Network-OSI-Model/assets/58394125/e1efe61e-f34e-432c-bb72-3d9a42b324b4)


This is the layer responsible for opening and closing communication between the two devices. The time between when the communication is opened and closed is known as the session. The session layer ensures that the session stays open long enough to transfer all the data being exchanged, and then promptly closes the session in order to avoid wasting resources.

The session layer also synchronizes data transfer with checkpoints. For example, if a 100 megabyte file is being transferred, the session layer could set a checkpoint every 5 megabytes. In the case of a disconnect or a crash after 52 megabytes have been transferred, the session could be resumed from the last checkpoint, meaning only 50 more megabytes of data need to be transferred. Without the checkpoints, the entire transfer would have to begin again from scratch.

 
4. The transport layer
The Transport Layer: segment, transport, reassembly
![osi_model_transport_layer_4](https://github.com/MNSakib02/Network-OSI-Model/assets/58394125/01b3a4e2-782f-45f3-bb9c-e00ab6aa4170)

The transport Layer is responsible for end-to-end communication between the two devices. This includes taking data from the session layer and breaking it up into chunks called segments before sending it to layer 3. The transport layer on the receiving device is responsible for reassembling the segments into data the session layer can consume.

The transport layer is also responsible for flow control and error control. Flow control determines an optimal speed of transmission to ensure that a sender with a fast connection does not overwhelm a receiver with a slow connection. The transport layer performs error control on the receiving end by ensuring that the data received is complete, and requesting a retransmission if it isn’t.

Transport layer protocols include the Transmission Control Protocol (TCP) and the User Datagram Protocol (UDP).

5. The network layer
The Network Layer: packets creation, transport, packets assembly
![osi_model_network_layer_3](https://github.com/MNSakib02/Network-OSI-Model/assets/58394125/45c49bd0-d251-4823-b5de-50e30c017f06)


The network layer is responsible for facilitating data transfer between two different networks. If the two devices communicating are on the same network, then the network layer is unnecessary. The network layer breaks up segments from the transport layer into smaller units, called packets, on the sender’s device, and reassembling these packets on the receiving device. The network layer also finds the best physical path for the data to reach its destination; this is known as routing.

Network layer protocols include IP, the Internet Control Message Protocol (ICMP), the Internet Group Message Protocol (IGMP), and the IPsec suite.

6. The data link layer
The Data Link Layer: frame creation, frames sent between networks
![data_link_layer_osi_model](https://github.com/MNSakib02/Network-OSI-Model/assets/58394125/f92d5c78-53be-46ed-a6b9-6dbba3d1389b)

The data link layer is very similar to the network layer, except the data link layer facilitates data transfer between two devices on the same network. The data link layer takes packets from the network layer and breaks them into smaller pieces called frames. Like the network layer, the data link layer is also responsible for flow control and error control in intra-network communication (The transport layer only does flow control and error control for inter-network communications).

7. The physical layer
The Physical Layer: sending cable, bitstream, receiving cable
![osi_model_physical_layer_1](https://github.com/MNSakib02/Network-OSI-Model/assets/58394125/e99bb812-42d8-49a6-8ad0-5ec51ef6f5f9)

This layer includes the physical equipment involved in the data transfer, such as the cables and switches. This is also the layer where the data gets converted into a bit stream, which is a string of 1s and 0s. The physical layer of both devices must also agree on a signal convention so that the 1s can be distinguished from the 0s on both devices.
