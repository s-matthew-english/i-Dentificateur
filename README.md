# i-Dentificateur

*a simple programme to identify the human language of a document or text fragment*


![id_2](https://cloud.githubusercontent.com/assets/9053984/7790715/1b59cad2-02c3-11e5-8ad4-417db2d6c2f6.jpg)



The methodoligies used herein were selected on the basis of:

> Garg, Archana, Vishal Gupta, and Manish Jindal. "*A Survey of Language Identification Techniques and Applications*." Journal of Emerging Technologies in Web Intelligence 6.4 (2014): 388-400.

### How Does It Work?
  - The programme stores a dictionary of each language for which it is operable in the form of a [Bloom filter](http://billmill.org/bloomfilter-tutorial/)
  - For an input text we search through the Bloom filters for each language incrementing an associated count whenever a word in the text corresponds to a word in one of our dictionaries. 
  - Finally, the language of the dictionary with the highest valued representive count variable is determined the winner. 

This method is surprisingly effective, able to correctly identify such potentially perplexing text fragments as "*Schwarzenegger in Kindergarten Cop*". 


### Version

&beta;

### Tech

To work properly:

* You should be running Java 7 or higher.

### Installation

Download the project zip file. 

```sh
$ wget https://github.com/h1395010/i-Dentificateur/archive/master.zip
```
Navigate to the directory and unzip it. 
```sh
$ unzip master.zip
```
'*cd* ' into the directory with the source files.
```sh
$ cd i-Dentificateur-master/
```
Compile with the command
```sh
$ javac *.java
```
Run with the command 
```sh
$ java iDentificateur
```


### Usage

Execution of the above commands will invoke the User Interface:

![ui](http://i.stack.imgur.com/aiEUV.png)

**Text Fragment**

Click the radio button adjacent to the word '*Text*', in the corresponding box input a fragment or sentence to assess the language in which it is written. 

**Document**

Indicate the radio button beside the word '*File*', this action will prompt an local explorer window, navigate to the file of interest and make the selection, this will initiate the evaluation process.


### Development

Want to contribute? Great!

Pull-requests are quite welcome.

Alternatively if you want to see a new feature let me know!

### TODO

> "a software is never done, you just stop working on it"

 - Handle exceptions at a higher level in the program and exit if an unusable state is detected
 - Add support for Chinese (Pinyin) and Russian
 - Programatically enforce specific encoding of stored lists and input text
 - Optimize size of Bloom filters
 - Unify input UI and output UI

 
### Currently Supported Languages

 * Italiano
 * Français
 * English
 * Deutsch
 * Español
 * Nederlandse
 * Português

### References

 - Word lists employed were downloaded from the [WinEdt Dictionaries](http://www.winedt.org/Dict/).
 - The concept of utilizing Bloom filters for this project was inspired, in addition to the above mentioned paper, by [Daniel Spiewak](http://www.codecommit.com/blog/scala/bloom-filters-in-scala).
 - This Bloom filter implementation draws on the work of [Magnus Skjegstad](https://github.com/magnuss/java-bloomfilter).


License
----

MIT



**Note**: Regarding *placement of braces* this code follows a symetrical style in lieu of the traditional Java convention 

