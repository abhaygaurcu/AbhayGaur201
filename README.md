// create a variable to hold your NFTs
let nfts = [];

// this function will take in some values as parameters, create an
// NFT object using the parameters passed to it for its metadata, 
// and store it in the variable above.
function mintNFT(name, description, owner) {
    const nft = {
        name: name,
        description: description,
        owner: owner,
        timestamp: new Date().toISOString()
    };
    nfts.push(nft);
    console.log(`Minted NFT: ${name}`);
}

// create a "loop" that will go through an "array" of NFTs
// and print their metadata with console.log()
function listNFTs() {
    nfts.forEach((nft, index) => {
        console.log(`NFT #${index + 1}`);
        console.log(`Name: ${nft.name}`);
        console.log(`Description: ${nft.description}`);
        console.log(`Owner: ${nft.owner}`);
        console.log(`Timestamp: ${nft.timestamp}`);
        console.log('---------------------------');
    });
}

// print the total number of NFTs we have minted to the console
function getTotalSupply() {
    console.log(`Total supply of NFTs: ${nfts.length}`);
}

// call your functions below this line

// Mint three NFTs
mintNFT("NFT 1", "Description of NFT 1", "Alice");
mintNFT("NFT 2", "Description of NFT 2", "Bob");
mintNFT("NFT 3", "Description of NFT 3", "Charlie");

// List all NFTs
listNFTs();

// Get total supply of NFTs
getTotalSupply();
