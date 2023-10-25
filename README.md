STEPS TO DEPLOY DEPLOY VRF DIRECT REQUEST  
  
STEP 1:
Have the XDC pay with mainnet connected to Remix

STEP 2:  
Git clone the repo : https://github.com/GoPlugin/vrf_client_contract_direct_request.git  
Copy the folder to Remix/ Connect the remix to local folder  where the contracts exist
Commands to Connet Remix to local folder:  
npm install -g @remix-project/remixd  
remixd -s folder_path -u https://remix.xinfin.network/  

STEP 3:
Request for co-ordinator address, wrapper_address and its subscription_id to Plugin Team, and update the below file:  
File : VRFV2DirectFunding.sol, line 47 : uint32 callbackGasLimit = appropriate_gas_limit;  
File : VRFV2DirectFunding.sol, line 54 : uint32 numWords = Minimum 1 and Maximum 10;  
File : VRFV2DirectFunding.sol, line 60 : address wrapperAddress = WRAPPER_ADDRESS;  
  
STEP 4:  
Fund the subscription_id  with a minimum of 10 PLI using below widget, follow the readme section for instructions  
https://github.com/GoPlugin/VRF-fund-widget.git  
  
STEP 5:  
Deploy the contract VRFV2DirectFunding.sol  
  
STEP 6:  
Fund the VRFV2DirectFunding contract with minimum of 10 PLI  
  
STEP 7:  
Trigger requestRandomWords method    
  
STEP 8:  
After the above transaction is complete trigger "lastRequestId", to fetch the latest request ID  
  
STEP 9:  
After few seconds, pass the above request ID as parameter and trigger "getRequestStatus" method to get the random numbers  
