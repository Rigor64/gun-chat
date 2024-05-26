<a name="readme-top"></a>

## Matteo Leopizzi 326110

<!-- LOGO -->
<br />
<div align="center">
    <img src="https://github.com/Rigor64/gun-chat/blob/main/public/favicon2.png" alt="Logo" width="100" height="100">

  <h1 align="center">JogTalk</h1>
  <h2 align="center">A decentralized chat app for your journey</h2>

</div>

<!-- Content tabel -->
<details>
  <summary>Content</summary>
  <ol>
    <li>
      <a href="#overview">Overview</a>
    </li>
    <li>
      <a href="#project-specifications">Project specifications</a>
      <ul>
        <li><a href="#decentralized-database">Decentralized Database</a></li>
        <li><a href="#message-transmission-and-encryption">Message Transmission and Encryption</a></li>
        <li><a href="#user-interface">User interface</a></li>
          <li><a href="#accessibility-and-usage">Accessibility and Usage</a></li>
      </ul>
    </li>
    <li>
      <a href="#protocol-description">Protocol description</a>
    </li>
    <li>
      <a href="#installation">Installation</a>
    </li>
  </ol>
</details>

<!-- OVERVIEW -->
## Overview
JogTalk is a unique chat app designed to help you to connect with others while you're out jogging or walking. Simply scan one of our specially designed QR codes with your device, that you can find around the entrances of parks, open fields, or at the beginning of a trail, and you'll be directed to our web service where the app runs seamlessly. Once logged in, you can join a global chat where users can share experiences, give feedback, and motivate each other. The goal of JogTalk is to promote outdoor activities and encourage people to engage with others nearby who are in the same location. Whether you're looking for a jogging partner, seeking motivation, or just want to share your journey, JogTalk makes your outdoor experience more interactive and enjoyable. Get moving and start chatting with JogTalk!

<p align="right">(<a href="#readme-top">Back on top</a>)</p>

<!-- PROJECT specifications -->
## Project specifications
<!-- DECENTRALIZED DATABASE -->
1. **Decentralized Database:**
   - JogTalk utilizes a decentralized database architecture to store user messages. This ensures that no single device holds the entire database, enhancing data security and redundancy.
   - Each user maintains a portion of the database on their device. The database is continuously synchronized, allowing for real-time updates and seamless communication.
   - Whenever the user turns off the application, all of the data stored in its device are eliminated.
   - The decentralized nature of the database reduces the risk of data breaches and provides resilience against server outages.

<!-- MESSAGE TRANSTISSION AND ENCRYPTION -->
2. **Message Transmission and Encryption:**
   - The app employs the GUN protocol, a decentralized networking protocol written in JavaScript, for both message transmission and encryption.
   - GUN ensures secure and efficient data distribution across all users, maintaining data integrity and privacy.
   - Messages are encrypted end-to-end, ensuring that user communication remains private and secure.
   - When create a new user account, the system generate a public/private key pair.
   - The login to the account is secured by hashing the password and a salt with PBKDF2. This produces a proof of work that is used to encrypt and decrypt the private key with AES.
   - With the private key, every user can read and write their own personal data using the private key as an AES encryption key.
   - With the public key, every user can sign their published content, to ensure the integrity.

<!-- USER INTERFACE -->
3. **User Interface:**
   - The graphical user interface (GUI) is developed using HTML and CSS, ensuring cross-device compatibility. This allows the application to be accessed through any device equipped with a web browser.
   - The interface is designed to be user-friendly and responsive, providing an optimal user experience regardless of the device used.

<!-- ACCESSIBILITY AND USAGE -->
4. **Accessibility and Usage:**
   - Users can join a global chat upon logging in, where they can share experiences, provide feedback, and encourage each other.
   - The QR code system simplifies access to the app, making it easy for users to connect and interact without the need for complex setup procedures.

<p align="right">(<a href="#readme-top">Back on top</a>)</p>

<!-- PROTOCOL DESCRIPTION -->
## Protocol description

[GUN](https://gun.eco/) is a small, easy, and fast protocol for syncing data. GUN is a database engine that runs every­where JavaScript does browsers, mo­bile de­vices and servers, al­low­ing you to build ex­act­ly the data sys­tem you want. GUN.JS aka GunDB is more than just a graph database. GUN is fully decentralized (peer-to-peer or multi-master), changes are not controlled by a centralized server. A server can be just another peer (node or vertices) in the network, one that may have more reliable resources than a browser. You save data on one machine, and it will sync it to other peers without needing a complex consensus protocol. GUN allows for data synchronization to happen seamlessly between all connected nodes by default. It’s offline first capabilities mean that if connectivity is lost to other nodes due to a network error or no availability, the application will store all changes locally and automatically synchronize as soon there is a connection. The gun graph database is stored across all peers participating in the network. Most data distribution scenarios that one could think of are possible to occur: Every peer might possess the complete graph, or only a subset of the complete graph and may possess data that does not exist on any other node (yet). The whole database is considered to be the union of all peers’ graphs.

[GitHub on the project](https://github.com/amark/gun)

<p align="right">(<a href="#readme-top">Back on top</a>)</p>

<!-- INSTALLATION -->
## Installation
If you want to try the local version of the project, you just need to open a PowerShell prompt and type:

```
git clone https://github.com/Rigor64/gun-chat
npm install
npm run dev
```

<p align="right">(<a href="#readme-top">Back on top</a>)</p>

