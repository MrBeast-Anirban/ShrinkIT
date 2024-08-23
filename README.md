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

Huffman Coding is widely used in various data compression applications, including file compression formats and data transmission protocols.
