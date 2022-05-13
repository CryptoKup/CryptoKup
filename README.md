Transactions-<BR>
A transaction contains the following fields:<BR>
Field Description<BR>
Version Protocol version number<BR>
Arbitrary Data Used for metadata or otherwise<BR>
Inputs Incoming funds<BR>
Outputs Outgoing funds (blk)<BR>
File Contract See: File Contracts (blk)<BR>
Storage Proof See: Proof of Storage (blk)<BR>
Signatures Signatures from each input<BR>
CRYPTOKUP-BTC-EGLD-ADA-SYSTEM P2P<BR>

 Inputs and Outputs<BR>
An output comprises a volume of coins. Each output<BR>
has an associated identifier, which is derived from the<BR>
transaction that the output appeared in. The ID of<BR>
output i in transaction t is defined as:<BR>
H(t||“output”||i)<BR>
where H is a cryptographic hashing function, and<BR>
“output” is a string literal. The block reward and<BR>
miner fees have special output IDs, given by:<BR>
H(H(Block Header)||“blockreward”)<BR>
Every input must come from a prior output, so an
input is simply an output ID.
Inputs and outputs are also paired with a set of
spend conditions. Inputs contain the spend conditions
themselves, while outputs contain their Merkle root
hash [2].
<b>KUP -System v2-by-anonimus-prt-bitcoin</b>Cryptokup.com
H(transaction||“contract”||i)
where i is the index of the contract within the transaction. The output ID of the proof can then be determined from:
H(contract ID||outcome||Wi)
Where Wi
is the window index, i.e. the number of
windows that have elapsed since the contract
<H3>CRYPTOKUP-VALIDA-COIN-H(contract ID||H(Bi−1))BLOCKCHAIN/explorer.cryptokup.com/H(t||“output”||i)</H3> reinvested (1,80%) 
Algorithm
Hosts prove their storage by providing a segment of
the original file and a list of hashes from the file’s
Merkle tree. This information is sufficient to prove
that the segment came from the original file. Because
proofs are submitted to the blockchain, anyone can
verify their validity or invalidity. Each storage proof
uses a randomly selected segment. The random seed
for challenge window W




