
CODE EXECUTION:


--> Open our project in Visual Studio or any editor.

--> Install Ganache, a private blockchain simulator for ethereum development and can be downloaded from https://www.trufflesuite.com/ganache.

--> Download Metamask from https://metamask.io/, which is a type of Ethereum wallet that bridges the gap between the user interfaces for Ethereum (e.g. Mist browsers, DApps) and the regular web (e.g. Chrome, Firefox, websites).
    
--> Make sure you have npm installed, go to command prompt & type npm -v, if a version comes out it's installed, else go to https://nodejs.org/en/ and download same.

--> Remix is the most popular IDE for Solidity developers, Go to http://remix.ethereum.org/ to use it or you can download the vscode extension by simply searching Ethereum Remix in the extension tab and download the same.

--> We need 6 accounts namely:- 

    1) one for admin who only can deploy smart contracts.
    2) one for phlebotomist who creates a bloood packet and makes it ready for delivery.
    3) one for transporter who starts delivery and update the delivery status and finally ends the delivery.
    4) one for blood bank admin who makes the blood packet ready for supply
    5) one for distributor who makes a final delivery to hospital
    6) one for hospital to receive the blood packet

--> Start the Ganache and you will get 10 default accounts for your blockchain at a local RPC server HTTP://127.0.0.1:7545.

--> Now Click the Remix extension tab in Visual studio code and perform the below steps:

    1) Click Run & Deploy, then click Activate in the pop-up menu.
    2) Now go back to Ganache, press the brown setting icon in the top-right icon.
    3) In the server tab, find the hostname with the port number and copy it.
    4) Paste this hostname with the port number in the Remix panel in the format of http://<hostname>:<port_number>, for me, it would be http://127.0.0.1:7545.
    5) Make sure our BloodProduction solidity file is active, then press compile in the Remix extension.
    6) After compiling our BloodProduction smart contract, we can deploy your token to the blockchain using your custom configuration ie enter the address of phlebotomist, bloodbank admin, transporter, distributor, hospital and click deploy.

--> Copy the address of deployed contract and paste it in config.js file

--> Open a terminal and enter the following commands
	
     npm install (If you are running it for the first time)
     npm start 

--> It automically opens our platform in the browser with the given address and port. In my case it is localhost:3000.

--> You can now connect to your installed metamask wallet extension and select the network as Ganache. 

--> You can switch your accounts to perform the operation as specified in blood production solidity file.

    1) Firstly, phlebotomist creates a packet, so you must use the phlebotomist metamask account to make a transaction and only then you can see the UI that can be used by Phlebotomist to create a blood packet.
       Phlebotomist creates a blood packet by filling the form with specified details and it will be visible only to phlebotomist and only a phlebotomist can perform that transaction.

    2) Now, the transporter can make start, update and End delivery transactions provided that he is connected to his/her metamask account in order to use the UI and perform transaction.

    3) Now, the blood bank admin can use his metamask account and our UI to perform make it ready for supply transaction.

    4) Now, the distributor using his account and the UI he can do final delivery to hospital transaction.

    5) Finally, hospital receives its blood packet.


------------------------------------------------------------------------------------------------------------END-------------------------------------------------------------------------------------------------------------------

