# Pollify
![image](https://github.com/joshDamian/lisk-voting-dapp/assets/67528283/47175fa3-fe2f-4cf1-a81b-4e43c76ea16f)


### About 
Pollify is a decentralized voting application using the Lisk SDK, where users can create and participate in various polls and elections. 

### Key Features:
**User Registration:** Users can create accounts on the DApp using their Lisk account.

**Poll Creation:** Registered users can create polls by specifying the title, description, options, and expiration date. These polls are stored on the sidechain.

**Voting:** Users can participate in polls by casting their votes. Each user's vote is recorded on the sidechain using their Lisk address.

**Results Display:** Real-time poll results are visualized in pie charts.

**Security:** Ensures that the voting process is secure and transparent by leveraging blockchain technology. Prevent double voting and ensure anonymity.

**Expiration and Closing:** Polls automatically close and results are finalized when the specified expiration date is reached.

### Testing Instructions
Clone the repo;

**Running Blockchain Client**
- `cd` to the `blockchain-client` folder.
- Run `npm install` and `npm run build` in the `blockchain-client` folder.
- Run `./bin/run start --config=config/custom_config.json` to start the blockchain client.

**Dapp frontend** 
- `cd` to the `dapp-frontend` folder.
- Run `npm install` to install dependencies.
- Run `npm run dev` to start the application.

PS: The blockchain client should be running before starting the frontend application.
