\documentclass{article}
\usepackage{amsmath}

\begin{document}

\section*{Huffman Coding Algorithm}

\textbf{Description:} Huffman Coding is a lossless data compression algorithm that uses variable-length codes for encoding symbols based on their frequencies. Frequently occurring symbols are assigned shorter codes, while less frequent symbols are given longer codes. This method ensures efficient data compression by reducing the overall file size.

\textbf{Algorithm:}
\begin{enumerate}
    \item \textbf{Frequency Analysis:}
    \begin{itemize}
        \item Calculate the frequency of each symbol (character) in the input data.
    \end{itemize}

    \item \textbf{Build a Priority Queue:}
    \begin{itemize}
        \item Create a priority queue (or min-heap) where each node is a symbol and its frequency. The node with the lowest frequency has the highest priority.
    \end{itemize}

    \item \textbf{Build the Huffman Tree:}
    \begin{itemize}
        \item While there is more than one node in the queue:
        \begin{itemize}
            \item Extract the two nodes with the lowest frequency.
            \item Create a new internal node with these two nodes as children and with a frequency equal to the sum of the two nodes' frequencies.
            \item Insert this new node back into the priority queue.
        \end{itemize}
    \end{itemize}

    \item \textbf{Generate Codes:}
    \begin{itemize}
        \item Traverse the Huffman tree from the root to each leaf node. Assign a binary code to each symbol by following the path from the root: `0` for left edges and `1` for right edges.
    \end{itemize}

    \item \textbf{Encode Data:}
    \begin{itemize}
        \item Replace each symbol in the input data with its corresponding Huffman code to produce the compressed data.
    \end{itemize}

    \item \textbf{Decode Data (optional):}
    \begin{itemize}
        \item To decode, use the Huffman tree to convert the encoded binary data back into the original symbols.
    \end{itemize}
\end{enumerate}

\textbf{Time Complexity:}
\begin{itemize}
    \item Building the Huffman tree: $O(n \log n)$
    \item Encoding/Decoding: $O(n)$, where $n$ is the length of the input data.
\end{itemize}

Huffman Coding is widely used in various data compression applications, including file compression formats and data transmission protocols.

\end{document}
