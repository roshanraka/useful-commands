Step 1: 

Create a skeleton business network using Yeoman. This command will require a business network name, description, author name, author email address, license selection and namespace.

Command: yo hyperledger-composer:businessnetwork

Enter property-sale for the network name, and desired information for description, author name, and author email.

Select Apache-2.0 as the license.

Select org.example.mynetwork as the namespace.

Select No when asked whether to generate an empty network or not.

Step 3:

Run the command in the project directory


Command: composer archive create -t dir -n .

Step 4: Deploying business network

To install the business network, from the property-sale directory, run the following command:


Command: composer network install --card PeerAdmin@hlfv1 --archiveFile property-sale@0.0.1.bna

The composer network install command requires a PeerAdmin business network card (in this case one has been created and imported in advance), and the the file path of the .bna which defines the business network.

To start the business network, run the following command:


Command: 
composer network start --networkName property-sales --networkVersion 0.0.1 --networkAdmin admin --networkAdminEnrollSecret adminpw --card PeerAdmin@hlfv1 --file networkadmin.card

The composer network start command requires a business network card, as well as the name of the admin identity for the business network, the name and version of the business network and the name of the file to be created ready to import as a business network card.

To import the network administrator identity as a usable business network card, run the following command:


Command: 
composer card import --file networkadmin.card

The composer card import command requires the filename specified in composer network start to create a card.

To check that the business network has been deployed successfully, run the following command to ping the network:


Command: 
composer network ping --card admin@property-sale

The composer network ping command requires a business network card to identify the network to ping.

Step 5: Rest Server

Command: composer-rest-server

composer-rest-server -c admin@property-sale -n never -w true

Step 6: Angular App

Command: yo hyperledger-composer:angular





