<!-- Author : Anirban Maitra -->
<div align="center">
<h1> ShrinkIT</h1>
</div>


- This webapp uses Huffman Coding for Text Compression and De Compression.
- Made with JavaScript, HTML5 and CSS3.


## About this application:

* This website performs Lossless data compression and decompression of text(.txt) files using Huffman Algorithm.
* In this algorithm, a variable-length code is assigned to input different characters. The code length is related to how frequently characters are used. Most frequent characters have the smallest codes and longer codes for least frequent characters.
* A Huffman code is a tree, built bottom up, starting with the list of different characters appearing in a text and their frequency. 
* Compression ratio usually improves as the file size increases.
* The website is made responsive (with HTML and CSS ) and interactive (with JavaScript ) .


# Huffman Coding Algorithm

**Description:** Huffman Coding is a lossless data compression algorithm that uses variable-length codes for encoding symbols based on their frequencies. Frequently occurring symbols are assigned shorter codes, while less frequent symbols are given longer codes. This method ensures efficient data compression by reducing the overall file size.

## Algorithm

1. **Frequency Analysis:**
   - Calculate the frequency of each symbol (character) in the input data.

2. **Build a Priority Queue:**
   - Create a priority queue (or min-heap) where each node is a symbol and its frequency. The node with the lowest frequency has the highest priority.

3. **Build the Huffman Tree:**
   - While there is more than one node in the queue:
     - Extract the two nodes with the lowest frequency.
     - Create a new internal node with these two nodes as children and with a frequency equal to the sum of the two nodes' frequencies.
     - Insert this new node back into the priority queue.

4. **Generate Codes:**
   - Traverse the Huffman tree from the root to each leaf node. Assign a binary code to each symbol by following the path from the root: `0` for left edges and `1` for right edges.

5. **Encode Data:**
   - Replace each symbol in the input data with its corresponding Huffman code to produce the compressed data.

6. **Decode Data (optional):**
   - To decode, use the Huffman tree to convert the encoded binary data back into the original symbols.

## Time Complexity

- Building the Huffman tree: `O(n log n)`
- Encoding/Decoding: `O(n)`, where `n` is the length of the input data.

