#### In this task, we discuss the \([7,4]\) Hamming code and investigate its reliability. That coding system	can correct single errors in the transmission of \(4\)-bit messages and proceeds as follows:   

* given a message, we first encode it to a 7-bit _codeword_, where G is a 4x7 _generator_ matrix  
* the codeword is transmitted, and we get the received message  
* System is checked for errors by calculating the _syndrome vector_ for a 7x3 _parity-check_ matrix H  
* if a single error has occurred, then the binary identifies show the wrong bit
* if the error was identified, then we flip the corresponding bit to get the corrected result;  
* the decoded message is then formed. 
  
#### The __generator__ matrix \(G\) and the __parity-check__ matrix \(H\) are given by
\[	
	G := 
	\begin{pmatrix}
		1 & 1 & 1 & 0 & 0 & 0 & 0 \\
		1 & 0 & 0 & 1 & 1 & 0 & 0 \\
		0 & 1 & 0 & 1 & 0 & 1 & 0 \\
		1 & 1 & 0 & 1 & 0 & 0 & 1 \\
	\end{pmatrix},
 \qquad 
	H^\top := \begin{pmatrix}
		1 & 0 & 1 & 0 & 1 & 0 & 1 \\
		0 & 1 & 1 & 0 & 0 & 1 & 1 \\
		0 & 0 & 0 & 1 & 1 & 1 & 1
	\end{pmatrix}
\]


#### Assume that each bit in the transmission \(\mathbf{c} \mapsto \mathbf{r}\) gets corrupted independently of the others with probability \(p = \mathtt{id}/100\), where \(\mathtt{id}\) is your team number. Your task is the following one.

1.  Simulate the encoding-transmission-decoding process N times and find the estimate p of the probability of correct transmission of a single message. Comment why, for large N, p is expected to be close to the other value.  
2. By estimating the standard deviation of the corresponding indicator of success by the standard error of your sample and using the CLT, predict the interval (v-E, v+E), in which the estimate  p falls with probability at least 0.95.  
3.  What choice of N guarantees that E < 0.03?  
4.  Draw the histogram of the number k = 0,1,2,3,4 of errors while transmitting a 4-digit binary message. Do you think it is one of the known distributions?
