# Open Head NFT Provenance
At OpenHead we believe in transparancy, that's why we've decided to use a provenance to proof there has been no tampering with the assignment of the NFT artwork. The provenance was assigned on contract deployment, before any token was minted, and can't be modified in any way.

The Open Head NFT provenance is:
```
5c2c415345e46ec68f5f97f895ba6e4e200e7879d3cee9c1966cb24ea1110f33
```

You can check it yourself reading the "provenance" field [in our smart contract](https://etherscan.io/address/0xca6788c8efa6a1c8bc97fa98938fa361d51ef823#readContract) or [in the following file of this repository](hashes/provenance.txt).


## What is a provenance?
We recommend checking [this article](https://medium.com/coinmonks/the-elegance-of-the-nft-provenance-hash-solution-823b39f99473), that explains beautifully what a provenance hash is.

## How was it calculated
For this project we decided to use SHA-256, be aware you'll need to use the same hashing algorithm in order to validate the provenance or any image hash.

* First, we generated the hash of each image - which you can find in the respective hashes/imageId.txt file.
* Then we concatenated all the resulting hashes into a single huge string - which you can see [in this file](hashes/concatenatedHashString.txt).
* Finally, we hashed the contents of the concatenated string, which gave us the resulting hash.

**Disclaimer: We used the resized images to calculate the provenance. You can find the resized image in the metadata of your NFT.**