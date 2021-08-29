In steganography, an innocent-looking image is taken as an example and a message is embedded in the image by changing the number of pixels selected by the encryption algorithm. By embedding a hidden message or file in an image, the number of pixels can be changed.

In short, this means we use the encrypted RGB data to include other data, which significantly impairs the visual representation of the image. The hidden message is transmitted by increasing the bandwidth of the original message or by manipulating the file format. Since steganography is often used in phishing and as a way for malicious software to exfiltrate data, it is very difficult to detect it.

I will build an example to demonstrate the encryption of data into images. The data is represented using its ASCII value. Each letter is represented using 8bits, or 1 byte. Each pixel in the image has three bits, one each for RGB frames. Each pixel can hold 3 bits. I will encode three pixels together, making a place for 9 bits. Out of the 9 bits, I will store 1 letter in the 8 bits and one (End Of File)EOF bit. If the EOF bit is high, then it indicates that the end of the message has been reached. Otherwise, it indicates the program to read more pixels for decoding.

I have a simple encryption technique included in the algorithm above. Instead of encoding 3 letters together, I can encode any other number of letters. Unless anyone knows this number, decrypting the file is going to be tough.
