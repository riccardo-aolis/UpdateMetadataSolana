# UpdateMetadataSolana
Tutorial on how to update the metadata of an NFT collection on Solana. It includes the script to format the data for the "metaboss update data-all" command. Following the steps you will update the metadata of every nft in your collection, while keeping the same name property for each mint id.  
  
**IMPORTANT**  
Test on devnet first. Use this method only if you know exactly what you are doing. 

**Steps:**  
1- Generate the new images/metadata  
2- Run "sugar upload" using the config file of the existing candy machine and the new images/metadata  
3- Run "metaboss snapshot mints" to fetch the mint ids  
4- Run "metaboss decode" using the output of the "metaboss snapshot mints" command  
5- Move the "metaboss decode" output inside a folder called mints_data, move mints_data in the same folder as format_script.py  
6- Move the new cache file generated using the "sugar upload" command in the same folder as format_script.py  
7- Create an "output" folder in the same folder as format_script.py  
8- Run the script from the main folder using "py format_script.py", you'll find the formatted data in the "output" folder  
9- Run "metaboss update data-all" using as --data-dir the path to the output folder  
  
**Contacts:** @riccardoaolis on Twitter
