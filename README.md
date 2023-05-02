Download Link: https://assignmentchef.com/product/solved-cosc310-assignment-7-binary-search-trees
<br>
The objectives of this assignment are to:

<ul>

 <li>Gain further experience with using interfaces.</li>

 <li>Gain further experience with recursion.</li>

 <li>Gain understanding and experience with implementations of a binary search tree.</li>

 <li>Gain experience with dictionary applications.</li>

 <li>Continue to practice good programming techniques.</li>

</ul>

<h3>Task:</h3>

<strong>Step 1:</strong>

Create a binary search tree implementation of a Dictionary.   The class must be named BSTDictionary where Dictionary is defined as:




/**

* An abstract data type for a Dictionary that maps a set of keys to values.

*

* <strong>@author</strong> <u>dtsmith</u>

*

* <strong>@param</strong> &lt;K&gt; Data type for the keys

* <strong>@param</strong> &lt;V&gt; Data type for the values

*/

<strong>interface</strong> Dictionary&lt;K, V&gt; {

/**

* Put a key together with its associated value into the dictionary.

* If the key already exists then the new value replaces the current

* value associated with the key. Values can be retrieved using the

* get method.

*

* <strong>@param</strong> key the key

* <strong>@param</strong> value the new value

* <strong>@return</strong> the original value if the key already exists in the

*         dictionary, otherwise null.

*/

<strong>public</strong> V put(K key, V value);




/**

* Get the current value associated with a given key.

*

* <strong>@param</strong> key the key

* <strong>@return</strong> the current value associated with the key in the dictionary

*         if found, otherwise null.

*/

<strong>public</strong> V get(K key);




/**

* Remove the key and its associated value associated from the

* dictionary. The value associated with the key is returned.  If the

* key does not exist in the dictionary then null is returned.

*

* <strong>@param</strong> key the key

* <strong>@return</strong> the value associated with the removed key in the dictionary.

*         If the key did not exist then null.

*/

<strong>public</strong> V remove(K key);




/**

* Create an Iterator to iterate over the keys of the dictionary.

*

* <strong>@return</strong> an Iterator to iterator over the keys.

*/

<strong>public</strong> Iterator&lt;K&gt; keys();




/**

* Test if the dictionary is empty

*

* <strong>@return</strong> true if the dictionary is empty, otherwise false

*/

<strong>public</strong> <strong>boolean</strong> isEmpty();




/**

* Get the number of keys in the dictionary

*

* <strong>@return</strong> the number of keys in the dictionary

*/

<strong>public</strong> <strong>int</strong> noKeys();

}

<strong>Your implementation of BSTDictionary must not use an inner/nested class of Nodes.</strong>  Instead define your BSTDictionary to have a left and right instance variables that are each a BSTDictionary.  This approach is going to be analogous to the Ls implementation of a linked list.  When a BSTDictionary is created, it will be empty and its left and right instance variables must be null.  The empty BSTDictionary is similar in purpose to the empty Ls at the end of an Ls list.  On adding a key and value to an empty BSTDictionary, set the key and value instance variables accordingly and create an empty BSTDictionary for the left and create an empty BSTDictionary for the right.  Note that each BSTDictionary must keep track of the number of keys in the given BSTDictionary including all descendants.  Given this an empty BSTDictionary will have zero for the number of keys.

Note that keys() returns a Java Iterator, however you only need to implement the hasNext() and next() methods.

<strong>Step 3:</strong>

Create a jUnit test program to thoroughly test your BSTDictionary.




<strong>Step 4: </strong>

Create a word count program (<strong>not in edu.iup.cosc310.util</strong>).  The word count program must open a text file passed to it on the command line.  Your program must process the text file identifying the set of unique words in the file and the number of occurrences of each word.  Separate words on spaces, commas, tabs, newlines, carriage returns, and other not alphanumeric characters (i.e. split on “\W+”).




After processing all the words in the input text file, your word count program must print a list of all the found words, in sorted order, together with the number of times each word was found within the file.  The output is to be is sorted word order.

<h3>Deliverables:</h3>




<ul>

 <li>zip file of your project. It will contain the sources and class files of your implementation, test, and word count program.  The .zip file must be named [Your name]Asmt7.zip.</li>

 <li>Printouts of source files for your interface, binary search implementation, test program, and word count program.</li>

 <li>Screen shot of your captured output from executing your jUnit test program.</li>

 <li>Text frle your captured output from executing your word count program against:</li>

</ul>

supplied sylabus.txt.

<h3>Other requirements:</h3>

<ul>

 <li>The iterator must return the keys in an in order traversal. The iterator implementation must not copy keys into a data structure holding all keys.</li>

 <li>The Dictionary and BSTDictionary must be defined in package edu.iup.cosc310.util.</li>

 <li>The word count program must be defined in package edu.iup.cosc310.wordcount</li>

 <li><strong>Must provide JavaDoc</strong></li>

</ul>


