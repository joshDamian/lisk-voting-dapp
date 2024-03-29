# Pollify

![image](https://github.com/joshDamian/lisk-voting-dapp/assets/67528283/47175fa3-fe2f-4cf1-a81b-4e43c76ea16f)

## About

Pollify is a decentralized voting application using the Lisk SDK, where users can create and participate in various polls and elections.

## Key Features

**User Registration:** Users can create accounts on the DApp using their Lisk account.

**Poll Creation:** Registered users can create polls by specifying the title, description, options, and expiration date. These polls are stored on the sidechain.

**Voting:** Users can participate in polls by casting their votes. Each user's vote is recorded on the sidechain using their Lisk address.

**Results Display:** Real-time poll results are visualized in pie charts.

**Security:** Ensures that the voting process is secure and transparent by leveraging blockchain technology. Prevent double voting and ensure anonymity.

**Expiration and Closing:** Polls automatically close and results are finalized when the specified expiration date is reached.

## Testing Instructions

### Software Requirements

The project requires:

- Node.js: 18.0
- npm: >= 8.1.0

### Cloning the repo

Clone the repository using the following command to include the `dapp-frontend` and `blockchain-client` submodules:

```bash
git clone --recurse-submodules https://github.com/joshDamian/lisk-voting-dapp.git
```

### Running Blockchain Client

- `cd` to the `blockchain-client` folder.
- Run `npm install` and `npm run build` in the `blockchain-client` folder.
- Run `./bin/run start --config=config/custom_config.json` to start the blockchain client.

### Running the Dapp frontend

- `cd` to the `dapp-frontend` folder.
- Run `npm install` to install dependencies.
- Run `npm run dev` to start the application.

PS: The blockchain client should be running before starting the frontend application.

### Funding lisk account

> You need some LSK to create polls and vote on `Pollify`

#### Using the client dashboard

While the blockchain client is running;

- Copy your LSK address from the account tab on `Pollify`

    ![image](https://github.com/joshDamian/lisk-voting-dapp/assets/67528283/df73763e-bd36-4d55-9c0c-98b3c791524e)

- Visit [http://localhost:4005](http://localhost:4005)
- Scroll to the `Invoke command` section and select `token_transfer`

    <img width="1438" alt="Screenshot 2023-09-12 at 04 54 09" src="https://github.com/joshDamian/lisk-voting-dapp/assets/67528283/8a231a7d-fcf6-4a79-bf35-3f6934f65101">

- Enter this passphrase into the passphrase input:

    ```txt
    guitar extend virtual giggle absorb hamster destroy bone sun gap fire penalty document rocket arrive eternal flight diet clarify inflict draw fruit usage mean
    ```

- Enter the request payload as shown in the picture, using your copied LSK address as `recipientAddress` and  `1481248200000000` as the `tokenID`.
Using this payload:

    ```json
    {
        "recipientAddress": "<YOUR LSK address>",
        "tokenID": "1481248200000000",
        "amount": "4000000000",
        "data": ""
    }
    ```

- Submit the request.
