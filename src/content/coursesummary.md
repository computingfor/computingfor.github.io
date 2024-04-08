+++
date = "07 Apr 2024"
draft = true
title = "Course Summary"
author = "David Evans"
slug = "summary"
+++

## Information

[**Class 1: Introduction**](/post/class1) [[Slides](https://www.dropbox.com/scl/fi/v1wetuahawmcf2a7q0h62/cs1010-class1.pdf?rlkey=10axy9myeli2jhlgru02ylgaq&dl=0)]  
[**Class 2: The Digital Abstraction**](/post/class2) [[Slides](https://www.dropbox.com/scl/fi/sz3pgkdg1ghqvr5vednpu/cs1010-class2.pdf?rlkey=ye1qcpmferifq2ktoq20axzc1&dl=0)]


**Information is an abstract mathematical notion.** To store, transmit, and manipulate information, though, it has to be represented in some **physical way**. At some level, everything in the physical world is continuous.

**Analog vs. Digital Data.** We can interpret a physical repesentation of information as either _analog_ or _digitial_ data. Analog data is _continuous_, with no limit on the number of different values (one way to think of this is that between any two values, there is another value). Digital data is _discrete_, where there is a fixed and finite set of possible values. There are gaps between the values.

**Interpretation of Physical Representations as Analog or Digital.** Although some physical representations are more naturally interpreted as analog or digital, what really matters is if the _interpretation_ of the state of the physical representation is continuous (analog) or discrete (digital). As a concrete example, a clock that ticks is digital, even if it looks like a traditional analog clock. Each tick advances the time by one second, and the physical representation (at least what we can see on the clock face, not the internal state of the springs and gears within the clock) is more naturally interpreted as one of a fixed set of discrete states (for a 12-hour clock, its a large set, but still a fixed and finite one with 60 &times; 60 &times; 12 different possible values).

**Why digital?** Although many early computers operated on analog data representations, nearly all data storage and computing today is doing using digital representations. The advantage of digital data representations is that they enable _reliable_ transmission, storage, and manipulation. With an analog represention, whenever data is copied there is some loss (known as _generation loss_) and this accumulates over time. After a few generations, is it likely that some errors have been introduced. With digital data, we can make _exact_ copies (of course, even with digital copies, there can sometimes be errors, but if there are no errors the copy is exact). We can make copies over and over again and expect to get exactly the same value we started with. Small errors that mean the physical representation is not an exact copy can be automatically corrected when the representation is interpreted as a digital value. This reliability applies not just to copying, but to operating on the data, allowing us to to computations that involve billions of steps without accumulating any errors.

[**Class 3: Apple is Lossy, but Microsoft has bigger Megabytes**](/post/class3) [[Slides](https://www.dropbox.com/scl/fi/7yl99l26ghhdvd8n06poz/cs1010-class3.pdf?rlkey=9nstxoa3nyec9l46km1wabrpk&dl=0)]  
[**Class 4: Continuous Binary Representations**](/post/class4) [[Slides](https://www.dropbox.com/scl/fi/n5byzf2nofdr38nejh7ru/cs1010-class4.pdf?rlkey=4b4w7fvkepwtqx00v92obb59a&dl=0)]


**Measuring information.** The fundamental unit of information is a _bit_ (binary digit). One bit is the amount of information needed to distinguish between two equally likely possibilities. We can represent a bit using a set of two options such as `{0, 1}` or `{off, on}` or `{red, blue}` or `{heads, tails}`. To distinguished between more than two possibilities, we need more than one bit. With two bits, we can distinguish four things: `{00, 01, 10, 11}`. Each additional bit doubles the number of possible values, so if there are _k_ bits we can distinguish 2<sup>_k_</sup> different values. 

**Bytes, MB, and more.** A _nibble_ is four bits, so can represent 2<sup>4</sup> = 16 different values (e.g., `{0000, 0001, 0010, 0011, 
 0100, 0101, 0110, 0111,
 1000, 1001, 1010, 1011,
 1100, 1101, 1110, 1111}`). A _byte_ is the name given to eight bits, which can represent 2<sup>8</sup> = 256 different values (we won't try to list them all, but you can follow the pattern of the 16 above, and combine each nibble with every nibble, getting 16 &times; 16 = 256 different 8-bit bitstrings). We can use the SI (metric) prefixes to represent larger numbers of bits, but they sometimes are used to mean powers of 2 (kilobyte = 1 kB = 2<sup>10</sup> bytes = 1024 bytes) and sometimes to mean powers of 10 (kilobyte = 1 KB = 10<sup>3</sup> bytes = 1000 bytes). A _megabyte_ is commonly used to mean either 2<sup>20</sup> = 2<sup>10</sup> &times; 2<sup>10</sup> = 1024 &times; 1024 = 1,048,576 bytes and 10<sup>6</sup> = 10<sup>3</sup> &times; 10<sup>3</sup> = 1000 &times; 1000 = 1,000,000 bytes. (Apple uses MB = 10<sup>6</sup> and Microsoft uses MB = 2<sup>20</sup>.) Similarly, a _gigabyte_ (GB) is either 2<sup>30</sup> bytes or 10<sup>9</sup> bytes (a Billion bytes), and a _terabyte_ (TB) is either 2<sup>40</sup> or 10<sup>12</sup> bytes (a Trillion bytes).

**Data Compression.** Modern computers can store enormous amounts of data (trillions of bytes are common) and our wired and wireless networks can transmit billions of bits per second, but we still want to store and send more information using those bits. We do this by _compressing_ data to make it smaller. Compression involves two functions: _compress_ and _uncompress_. A _function_ is a mathematical abstraction that maps an _input_ to and _output_. For a given input, the same output is always produced. The _compress_ function taks as its input a sequence of bits (_x_), and outputs a compressed representation of the input, _y_. If the compression is successful, the size of _y_ is much smaller than the size of _x_. Compression is possible because most data is redundant, and because not all values are equally likely we can find ways to compress most data. 

**Lossless vs. Lossy Compression.** Compression is _lossless_ if there is a way to get back exactly the original bits from the compressed representation: for any input _x_, _uncompress_(_compress_(_x_)) = _x_.  We would use lossless compression when the data being compressed is text, numbers, code, or some other type of data where exact values are important.  For many kinds of data, obtaining the exact value is not necessary. This is the case for data like images and audio files, where the value of the data is for humans to observe it, and because of the limits of human perception most humans will not be able to tell the difference between many different values. To enable more compression, for these types of data we often use _lossy_ compression. With lossy compression, _uncompress_(_compress_(_x_)) &thickapprox; _x_. The result of compressing and uncompression is not an exact match to the original data, but is close enough to be good enough for most human uses. Examples of lossy compression are the audio formats used to send data to bluetooth headphones (at least on Apple devices), the `jpg` image formats, and `mp3` audio. The _compression ratio_ is the original (uncompressed) size of the data divided by the size of the compressed data. For typical images we can have a compression ratio around 10 before it starts to look bad to most people; for audio files, the amount of compression that can be tolerated depends on the type of audio and the listener, but compression ratios over 10 are common.

**Why binary?** (Make sure you understand _Why Digital?_ above first &mdash; that explains what data representations should be interpreted as discrete sets, but not why there should only be two values.) Some phyiscal data representations naturally have two clear states, such as magnetic charge (positive or negative), punch cards (either unpunched or punched), but many physical representations are continuous such as amount of electical charge (which is discrete if we can count individual electrons, but is noromally measured in a continuous way). The reason why we use binary interpretations even when the physical representation is continuous is to minimize the size of error regions. If a continuous representation is mapped to two discrete values, there is one error region (that surrounds the point where the value is interpreted as `0` and where it is interpreted as `1`). If we instead represented three discrete values there would be two error regions, and in general, if there are _n_ discrete values we would have _n_ - 1 error regions. Since our goal is to use the continuous storage efficiently, the best solution will be to have only two discrete values and to reduce the amount of contiuous charge needed as much as possible to have an acceptably low error rate.  The other reason to prefer binary representations is because it is easier to compute on binary data than on date with more than two values.

**Algorithms.** An _algorithm_ that solves a problem is a method that 



- Project 1 Questions
- Continuous Binary Representations
- Encryption
- Leaking DRAM (Cold Boot Attacks)

 [**Class 5: Computing on Binary Data**](/post/class5) [[Slides](https://www.dropbox.com/scl/fi/x904tmp7136f9nj33fy1z/cs1010-class5.pdf?rlkey=kfpdstldfmoubw725tqutuow8&dl=0)]

- Addition Algorithms
- What is an _algorithm_?
- Binary Addition Algorithms
- Multiplcation
- 0.010101010101010...
