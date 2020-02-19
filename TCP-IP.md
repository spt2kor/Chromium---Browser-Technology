
# Building Blocks of TCP
  NETWORKING 101, CHAPTER 2
  https://hpbn.co/building-blocks-of-tcp/

  TCP provides an effective abstraction of a reliable network running over an unreliable channel,
  hiding most of the complexity of network communication from our applications: 
  retransmission of lost data, in-order delivery, congestion control and avoidance, data integrity, 
  and more. When you work with a TCP stream, you are guaranteed that all bytes sent will be identical
  with bytes received and that they will arrive in the same order to the client. As such, TCP is 
  optimized for accurate delivery, rather than a timely one. This, as it turns out, also creates
  some challenges when it comes to optimizing for web performance in the browser.

  The HTTP standard does not mandate TCP as the only transport protocol. If we wanted, we could 
  deliver HTTP via a datagram socket (User Datagram Protocol or UDP), or any other transport protocol of our choice,



# Building Blocks of UDP
https://hpbn.co/building-blocks-of-udp/
  UDP is colloquially referred to as a null protocol, and RFC 768, which describes its operation, could indeed fit on a napkin.

  The words datagram and packet are often used interchangeably, but there are some nuances. 
  While the term "packet" applies to any formatted block of data, the term "datagram" is often 
  reserved for packets delivered via an unreliable service—no delivery guarantees, no failure notifications.

  UDP acronym, to form "Unreliable Datagram Protocol." That is also why UDP packets are generally,
  and more correctly, referred to as datagrams.

DNS
  Perhaps the most well-known use of UDP, and one that every browser and Internet application depends on, 
  is the Domain Name System (DNS): given a human-friendly computer hostname, we need to discover its 
  IP address before any data exchange can occur.

Web Real-Time Communication (WebRTC) standards
voice and video calling and other forms of peer-to-peer (P2P)  communication,
  The new Web Real-Time Communication (WebRTC) standards, jointly developed by the IETF and W3C working groups,
  are enabling real-time communication, such as voice and video calling and other forms of peer-to-peer (P2P) 
  communication, natively within the browser via UDP. With WebRTC, UDP is now a first-class browser transport 
  with a client-side API! We will investigate WebRTC in-depth in WebRTC, 


IP 
  To understand UDP and why it is commonly referred to as a "null protocol," we first need to 
  look at the Internet Protocol (IP), which is located one layer below both TCP and UDP protocols.
  The IP layer has the primary task of delivering datagrams from the source to the destination host based on their addresses.

IP- Unreliable
  Once again, the word "datagram" is an important distinction: 
  the IP layer provides no guarantees about message delivery or notifications of failure and hence 
  directly exposes the unreliability of the underlying network to the layers above it.
  If a routing node along the way drops the IP packet due to congestion, high load, or for
  other reasons, then it is the responsibility of a protocol above IP to detect it, 
  recover, and retransmit the data—that is, if that is the desired behavior!

UDP packet add Port No 
  The UDP protocol encapsulates user messages into its own packet structure (Figure 3-2),
  which adds only four additional fields: source port, destination port, length of packet, 
  and checksum. Thus, when IP delivers the packet to the destination host, the host is able 
  to unwrap the UDP packet, identify the target application by the destination port, and
  deliver the message. Nothing more, nothing less.

UDP is NULL Protocol 
- drops source port,checksum, and connection mgmt responsibility to Application layer
  both the source port and the checksum fields are optional fields in UDP datagrams.
  The IP packet contains its own header checksum, and the application can choose to omit 
  the UDP checksum, which means that all the error detection and error correction can be delegated
  to the applications above them. At its core, UDP simply provides "application multiplexing" on top 
  of IP by embedding the source and the target application ports of the communicating hosts. With that
  in mind, we can now summarize all the UDP non-services:

  No guarantee of message delivery
  No acknowledgments, retransmissions, or timeouts

  No guarantee of order of delivery
  No packet sequence numbers, no reordering, no head-of-line blocking

  No connection state tracking
  No connection establishment or teardown state machines

  No congestion control
  No built-in client or network feedback mechanisms

TCP VS UDP
  TCP is a byte-stream oriented protocol capable of transmitting 
  application messages spread across multiple packets 
  without any explicit message boundaries within the packets themselves. To achieve this, 
  connection state is allocated on both ends of the connection, and 
  each packet is sequenced,
  retransmitted when lost, and 
  delivered in order. 
  
  UDP datagrams, on the other hand, have definitive boundaries: 
  each datagram is carried in a single IP packet, and 
  each application read yields the full message; 
  datagrams cannot be fragmented.
  
  UDP is a simple, stateless protocol, suitable for bootstrapping other application protocols on top: 
  virtually all of the protocol design decisions are left to the application above it.  
  
  Connection-State Timeouts
  
the primary feature of UDP is all the features it omits: no connection state, handshakes, retransmissions, reassembly, reordering, congestion control, congestion avoidance, flow control, or even optional error checking. 
  
  
  
  
  
  
  
  


