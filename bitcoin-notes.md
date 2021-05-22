May 21, 2021 : 
Bro : on my asus laptop, I am hoisting a full node

Q.) What is a full node ? 
+ Bro mostly a node has 4 components, 
Miner, Wallet, Blockchain DB, Router

Q.) How i am booting a node ? 
When a new bitcoin node is booted :  this means i have dowmnloaded 'bitcoin-core' s/w (it is of few MBs)
i run it either in GUI mode or daemon mode
 
At this stage the node is not able to perform any of the above mentioned function,

Blockchain is a P2P protocol, so a node need to be able to connect with multiple nodes. For the first time; a node connects to a 'SEED NODE'. 
it is the first node to which a node connects :  it gets different paths from this node

A full node can independenty verify transactions, mine new blocks : it connnects to n/w to sync and know which node have been added
 

+++++++
{
    .......
  {
    "id": 16,
    "addr": "194.14.246.205:8333",
    "addrbind": "192.168.1.21:35556",     // the port is diff for each peer
    "addrlocal": "112.196.153.224:50950", // the port is diff for each peer
    "network": "ipv4",
    "services": "000000000000040d",
    "servicesnames": [
      "NETWORK",
      "BLOOM",
      "WITNESS",
      "NETWORK_LIMITED"
    ],
    "relaytxes": true,
    "lastsend": 1621578474,
    "lastrecv": 1621578474,
    "last_transaction": 0,
    "last_block": 1621578474,
    "bytessent": 298077,
    "bytesrecv": 2100904,
    "conntime": 1621578407,
    "timeoffset": 0,
    "pingtime": 0.190321,
    "minping": 0.190321,
    "version": 70015,
    "subver": "/Satoshi:0.18.1/",
    "inbound": false,
    "startingheight": 684400,
    "synced_headers": 684400,
    "synced_blocks": 67233,
    "inflight": [
    ],
    "permissions": [
    ],
    "minfeefilter": 0.00001898,
    "bytessent_per_msg": {
      "feefilter": 32,
      "getaddr": 24,
      "getdata": 296664,
      "getheaders": 1053,
      "ping": 32,
      "pong": 32,
      "sendcmpct": 66,
      "sendheaders": 24,
      "verack": 24,
      "version": 126
    },
    "bytesrecv_per_msg": {
      "addr": 30082,
      "block": 2069327,
      "feefilter": 32,
      "getheaders": 1053,
      "headers": 106,
      "ping": 32,
      "pong": 32,
      "sendcmpct": 66,
      "sendheaders": 24,
      "verack": 24,
      "version": 126
    },
    "connection_type": "outbound-full-relay"
  }
]
+++++++

Q.) Bro : i ran my s/w in the night, it 25% blocks downloaded 
quit gui -> then i ran daemon ,   then  quit daemon -> ran GUI again
 it showed only 3 % blocks downloaded


Q.) Interesting Problem to solve 

root@krisalphaPC:/# df -h
Filesystem      Size  Used Avail Use% Mounted on
/dev/sda6       268G  254G  835M 100% /
/dev/sda4       384G  194M  364G   1% /folder


bro : 2 interesting things :
if i run the bitcoin qt s/w in sudo : it installs in /blockchain folder 
if i uses another user it installs in /home/anjali folder



Q.) How a Full node v/s SPV node verify the transaction?
UTXO is the unit that decide generation/transfer of bitcoin 

To verify a transaction the UTXO must belong to the spender and must be un-spent
The full node traces the UTXO right to the genesis block if needed if it has to verify a transaction. 

But a SPV node does not do it. The SPV node just stores the headers so it canot verify the transactin. 
So what happens is this 
for ex. we are on node # 300000 
if it needs to verify that the transaction on the node is legit, it waits for few minutes 
ex it will wait for creation of next 6 block, block # 300001- 300006 ; it will assume because the other nodes have created 6 new blocks 
then the transactions in block # 300000 should be valid.


