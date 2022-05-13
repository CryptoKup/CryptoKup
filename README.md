Transactions
A transaction contains the following fields:
Field Description
Version Protocol version number
Arbitrary Data Used for metadata or otherwise
Inputs Incoming funds
Outputs Outgoing funds (optional)
File Contract See: File Contracts (optional)
Storage Proof See: Proof of Storage (optional)
Signatures Signatures from each input
KupFIXFee Reward giventoUS REZERVE
Inputs and Outputs
An output comprises a volume of coins. Each output
has an associated identifier, which is derived from the
transaction that the output appeared in. The ID of
output i in transaction t is defined as:
H(t||“output”||i)
where H is a cryptographic hashing function, and
“output” is a string literal. The block reward and
miner fees have special output IDs, given by:
<h3>https://explorer.cryptokup.com/H(H(Block Header)||“blockreward”)email wallet</h3>
H(transaction||“contract”||i)
where i is the index of the contract within the transaction. The output ID of the proof can then be determined from:
H(contract ID||outcome||Wi)
<b>Valid-blockchain-KUP -System v2-by-anonimus-prt-bitcoin</b>
Algorithm
Hosts prove their storage by providing a segment of
the original file and a list of hashes from the file’s
Merkle tree. This information is sufficient to prove
that the segment came from the original file. Because
proofs are submitted to the blockchain, anyone can
verify their validity or invalidity. Each storage proof
uses a randomly selected segment. The random seed
for challenge window Wi
is given by:
H(contract ID||H(Bi−1))
Introduced several improvements such as views which give smart contracts the ability to read the storage state of other smart contracts, timelock encryption to serve as a countermeasure against Block Producer Extractable Value, caching to provide faster access at lower gas costs to data that is accessed regularly, and a global table of constants to facilitate development of more complex smart contracts.
<!---
CryptoKup/CryptoKup is a ✨ special ✨.
You can click the Preview link to take a look at your changes.
--->
