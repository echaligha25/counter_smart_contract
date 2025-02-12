
git clone https://github.com/starknet-edu/basecamp11-app.git
cd basecamp11-app


starkli signer keystore new keystore.json
starkli account oz init account.json --keystore keystore.json

starkli account deploy account.json --keystore keystore.json


starkli declare target/dev/sn_workshop_Counter.contract_class.json --account account.json --keystore keystore.json

//to deploy use the below command
starkli deploy Contract-Class-Hash InitialNumber DestinationAccount

eg 
starkli deploy 0x059008e773455069448845ec2a7557f8c8fe9dc94afaff13fd90865f1aaa17c4 4 0x045f9be2a7c7c8e2af0db69305fa175d9f37ed2be5356d63897b670bf0e04a3a --account account.json --keystore keystore.json

resoureces links
https://book.cairo-lang.org/ch101-03-contract-events.html
https://docs.starknet.io
https://starknet-by-example.voyager.online/applications/simple_vault
https://docs.openzeppelin.com/contracts-cairo/0.20.0/access
https://book.starkli.rs/accounts
https://foundry-rs.github.io/starknet-foundry/
