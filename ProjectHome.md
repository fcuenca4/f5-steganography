## F5 Steganography in Java ##
**F5 is a steganography algo for hiding information in JPEG images**. Unless other implementations it really hides it inside the image itself (not in metadata/comment fields or appended to the end of the file).

This project hosts the source code for a Java F5 steganography implementation as open source.

Credits for this go to Andreas Westfeld, it's base on his work.

Copy from [original paper](http://f5-steganography.googlecode.com/files/F5%20Steganography.pdf):

_Abstract. Many steganographic systems are weak against visual and statistical attacks. Systems without these weaknesses offer only a relatively small capacity for steganographic messages. The newly developed algorithm F5 withstands visual and statistical attacks, yet it still offers a large steganographic capacity. F5 implements matrix encoding to improve the efficiency of embedding. Thus it reduces the number of nec- essary changes. F5 employs permutative straddling to uniformly spread out the changes over the whole steganogram._

## Example Usage ##
Download the [f5.jar](http://f5-steganography.googlecode.com/files/f5.jar), and start it via Java from the command line. To **embed** a file called _msg.txt_ in a picture called _pic.jpg_ run the following:
```
java -jar f5.jar e -e msg.txt pic.jpg out.jpg
```

To **extract** a message from a picture call you call this:
```
java -jar f5.jar x -e out.txt pic.jpg
```

You can also give a password to protect the data or specify the image quality for the JPEG, e.g.:
```
java -jar f5.jar e -e msg.txt -p mypasswd -q 70 in.jpg out.jpg
java -jar f5.jar x -p mypasswd -e out.txt in.jpg
```

## Online Demos ##
currently there I only know of one [webapp with an online demo](https://www.swissxl.ch/tools/f5-steganography/) running. If you find more, please let me know.