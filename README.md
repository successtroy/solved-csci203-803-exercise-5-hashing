Download Link: https://assignmentchef.com/product/solved-csci203-803-exercise-5-hashing
<br>
This exercise is to be completed during your week 8 laboratory class. When you complete the exercise show your work to your lab tutor to have your work marked. The marking is based mainly on correct implementation and code readability. You should implement your code in one file (e.g. ex5.cpp, ex5.c, ex5.java). Make sure your program has a header comment block accontaining the name of the exercise, your name and your student login (e.g. jfk01). You may implement your solution in C, C++, Java or Python.




For this exercise, you are to implement a simple hash table. Your program should prompt for the name of an input file and the read and process the data contained in the file.




The file contains a sequence of integer values. Read them and construct a hash table using chaining. For this exercise, you should use linked lists implemented with dynamic data, as shown below

<img decoding="async" data-recalc-dims="1" data-src="https://i0.wp.com/www.logicprohub.com/wp-content/uploads/2019/09/306.png?w=980&amp;ssl=1" class="aligncenter lazyload" src="data:image/gif;base64,R0lGODlhAQABAAAAACH5BAEKAAEALAAAAAABAAEAAAICTAEAOw==">

 <noscript>

  <img decoding="async" class="aligncenter" src="https://i0.wp.com/www.logicprohub.com/wp-content/uploads/2019/09/306.png?w=980&amp;ssl=1" data-recalc-dims="1">

 </noscript>




Your program should read each integer in turn and calculate its hash value using mod 100 as the hashing function. Thus, if the key is <em>k</em>, the hash value h(<em>k</em>) = <em>k </em>mod 100.




When you have finished calculate and print:

<ol>

 <li>The number of empty entries in the hash table.</li>

 <li>The length of the longest chain.</li>

</ol>




As usual, do not use STL or equivalent. Page 2 has pseudo code of some algorithms you might use.




When you are finished, test your program using the provided text file named “ex5.txt” and show your code and the output to your lab tutor to receive your mark. Also, submit your file via unix (banshee) using the submit command below.




<h1>$ submit -u <em>login </em>-c CSCI203 –a ex5 <em>filename </em></h1>

<strong><em> </em></strong>

where ‘<strong><em>login</em></strong>‘ is your UNIX login ID and ‘<strong><em>filename</em></strong>’ is the name of your file.




If you are unable to attend your lab class and demonstrate your work on time due to circumstances beyond your control (e.g. sickness), contact your lecturer  to request an extension.




1




<strong> </strong>

<h1>Pseudo Code</h1>

<strong> </strong>

<strong>  </strong>

<strong>insert( int key, int value ) </strong>

<strong> </strong>

<strong>   create newNode, assign value to it,     set newNode.next to null    if hashTable[key] is NULL then         hashTable[key] = newNode    else         Node^ currentNode = hashTable[key]         while currentNode.next != NULL             currentNode = currentNode.next         end while         currentNode.next = newNode    end if  end insert() </strong>

<strong> </strong>

<strong>  </strong>

<strong>int hashFunction( int value ) </strong>

<strong> </strong>

<strong>      calculate hashKey from value     return hashKey </strong>

<strong> </strong>

<strong>end hashFunction() </strong>

<strong> </strong>

<strong>  </strong>

<strong>main()     try to open input file,   print error &amp; exit if file not found </strong>

<strong> </strong>

<h2>      initise hash table</h2>

<strong>      while file has more data… </strong>

<strong>            get hash key from hash function         insert value into hashTable at key </strong>

<strong> </strong>

<strong>      end while       print nubmer of empty entries and collisions </strong>

<strong>       </strong>

<h2>end main()</h2>

<strong> </strong>

2


