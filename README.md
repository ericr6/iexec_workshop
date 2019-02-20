# iexec_workshop

iExec, being blockchain-based, allows you to manage your computing transactions in a secure and decentralized environment.
In order to transact between multiple parties within iExec, an Ethereum wallet is required.
First, you will need to create your Ethereum wallet and credit it with Ethereum tokens (ETH), before running the application.
While iExec is in its development phase, we allow transactions on Ethereum’s Kovan Network. Sometimes referred to as test network, it uses Kovan ETH tokens that hold no real value and are used solely for testing purposes.

 

##Install the SDK 

The iExec SDK and API provide a set of tools that allows all users to easily interact with iExec decentralized marketplace.

```
npm -g install iexec # install the cli
iexec --version
iexec --help

``` 


## What is wallet 
The cryptocurrency wallet is a secure software program to interact with blockchains.
The wallet enables user to send and receive digital currency and monitor their balance and conduct other operations as smart contract.

iExec service runs on ethereum blockchain, the deal between agents (data owner, resources provider, developer and end users) are made using RLC token.

This transaction execution (smart contract) takes some amount of gas in ETH,
this gas is used to calculate the amount of fees that need to be paid to the network in order to execute an operation.


## Setup your wallet and charge your wallet

There is nothing to do!
We realized the job, ask to the instructor where to download all the information   

unzip the file in your working directory 
and check your wallet 

```
   iexec wallet show
```
 to show your wallet balance 
 
```
address:    0xca10fe415a89f75784166ca32cf1384f26f9e479

✔ Wallet kovan balances [42]:
ETH:  0
nRLC: 50000

``` 

iExec is a marketplace, you can view the state of the current orderbook, the list of computing resources available now.
 
```
iexec orderbook show
ℹ using chain [kovan]
✔ orderbook details:
- 
  id:        2050
  price:     10563
  pool:      0x4a02532aBD258929d211A660e155aB747eCa7F46
  category:  5
  timestamp: 2019-02-18T16:02:56.000Z
- 
  id:        2038
  price:     10955
  pool:      0x295732b566B785D24A839e57a4AEea0C849b6A4a
  category:  5
  timestamp: 2019-02-18T10:52:28.000Z
- 
  id:        1989
  price:     14208
  pool:      0x49327538C2f418743E70Ca3495888a62B587A641
  category:  5
  timestamp: 2019-02-07T10:16:44.000Z
- 
  id:        2026
  price:     15243
  pool:      0x295732b566B785D24A839e57a4AEea0C849b6A4a
  category:  5
  timestamp: 2019-02-14T09:15:52.000Z
- 
  id:        1988
  price:     15378
  pool:      0x49327538C2f418743E70Ca3495888a62B587A641
  category:  5
  timestamp: 2019-02-07T10:15:56.000Z

ℹ trade in the browser at https://market.iex.ec

``` 
Your are ready to buy resources to run your applications. The payment will be in RLC, the iExec cryptocurrency.
  
## Install metamask and configure your wallet

https://metamask.io/ 

Copy your private key from wallet.json and import 
Warning: remember we are in testing configuration, in mainnet, manage your wallet information with cautious
keep your private safe, you can loose all your cryptocurrencies without recovery possible.     

Open your metamask extension and select import 
![import in myether wallet](images/mew_import.png)

![import private key](images/mew_newaccount.png)




##The application

### The software: Nilearn 

Nilearn is a Python module for fast and easy statistical learning on NeuroImaging data.

<https://nilearn.github.io/>

It leverages the scikit-learn Python toolbox for multivariate statistics with applications 
such as predictive modelling, classification, decoding, or connectivity analysis.

### The application detail 

the application consists in plotting a statistical maps to measure the brain activity
more details in https://en.wikipedia.org/wiki/Statistical_parametric_mapping

The initial example can be found here
<http://nilearn.github.io/auto_examples/plot_3d_and_4d_niimg.html>

The second plot applies a threeshold to hightlighs the more active area (first plot without threeshold)    


The data are available at www.neurovault.com, a public repository of unthresholded statistical maps, 
parcellations, and atlases of the brain


Nilearn software will download the input data if it is present on the current 


      

## Intro to SGX

iExec provides a full end to end data protection for blockchain-based computation using Intel® SGX.

End-to-end protection means full protection of the application data, user data, embedded data as well as application output data.

Intel® Software Guard Extensions (SGX) is a technology that runs code and data in CPU-hardened “enclaves” or a ‘Trusted Execution Environment’ (TEE).

The enclave is a trusted area of memory where critical aspects of the application functionality are protected, helping keep code and data confidential and unmodified.

Your account must be topped up with RLC in order to trigger the execution of an application.

  
### Prepare the dAPP, 
- dockerize
  iExec supports dockerized application, 
- no gui   
- data input
    
### Run the dApp

```
    cp iexec-rlc.blend ./tee/inputs
```

### Run the dApp with privacy preserving
   -customize the docker
   -encrypt the data
   -custom the execution