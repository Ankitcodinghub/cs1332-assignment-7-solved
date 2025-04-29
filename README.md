# cs1332-assignment-7-solved
**TO GET THIS SOLUTION VISIT:** [CS1332 Assignment 7 Solved](https://www.ankitcodinghub.com/product/cs1332-important-solved-7/)


---

📩 **If you need this solution or have special requests:** **Email:** ankitcoding@gmail.com  
📱 **WhatsApp:** +1 419 877 7882  
📄 **Get a quote instantly using this form:** [Ask Homework Questions](https://www.ankitcodinghub.com/services/ask-homework-questions/)

*We deliver fast, professional, and affordable academic help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;109379&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;1&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;5&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;5\/5 - (1 vote)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;CS1332 Assignment 7 Solved&quot;,&quot;width&quot;:&quot;138&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

<div class="kksr-stars">

<div class="kksr-stars-inactive">
            <div class="kksr-star" data-star="1" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="2" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="3" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="4" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="5" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>

<div class="kksr-stars-active" style="width: 138px;">
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>
</div>


<div class="kksr-legend" style="font-size: 19.2px;">
            5/5 - (1 vote)    </div>
    </div>
1. All submitted code must compile under JDK 8. This includes unused code, so don’t submit extra files that don’t compile. Any compile errors will result in a 0.

2. Do not include any package declarations in your classes.

3. Do not change any existing class headers, constructors, instance/global variables, or method signatures. For example, do not add throws to the method headers since they are not necessary.

4. Do not add additional public methods.

5. Do not use anything that would trivialize the assignment. (e.g. don’t import/use java.util.ArrayList for an ArrayList assignment. Ask if you are unsure.)

6. Always be very conscious of efficiency. Even if your method is to be O(n), traversing the structure multiple times is considered inefficient unless that is absolutely required (and that case is extremely rare).

7. You must submit your source code, the .java files, not the compiled .class files.

8. Only the last submission will be graded. Make sure your last submission has all required files. Resubmitting will void all previous submissions.

9. After you submit your files, redownload them and run them to make sure they are what you intended to submit. You are responsible if you submit the wrong files.

Pattern Matching

For all of the algorithms, make sure you check the simple failure cases as soon as possible. For example, if the pattern is longer than the text, don’t do any preprocessing on the pattern/text and just return an empty list since there cannot be any occurrences of the pattern in the text.

CharacterComparator

CharacterComparator is a comparator that takes in two characters and compares them. This allows you to see how many times you have called compare(); besides this functionality, its return values are what you’d expect a properly implemented compare() method to return. You must use this comparator as the number of times you call compare() with it will be used when testing your assignment.

If you do not use the passed in comparator, this will cause tests to fail and will significantly lower your grade on this assignment.

You must implement the algorithms as they were taught in class. We are expecting exact comparison counts for this homework. If you are getting fewer comparison counts than expected, it means one of two things, either you implemented the algorithm wrong (most likely) or you are using an optimization not taught in the class (unlikely).

Knuth-Morris-Pratt

Failure Table

The Knuth-Morris-Pratt (KMP) algorithm relies on using the prefix of the pattern to determine how much to shift the pattern by. The algorithm itself uses what is known as the failure table (also called failure function). This is an array of length m where each index will correspond to the character at that index in the pattern. Each index i of the failure table should contain the length of the longest proper prefix that matches a proper suffix of pattern[0, …, i]. A proper prefix/suffix does not equal the string itself. There are different ways of calculating the failure table, but we are expecting the specific format described below.

For any string pattern, have a pointer i starting at the first letter, a pointer j starting at the second letter, and an array called table that is the length of the pattern. First, set index 0 of table to 0. Then, while j is still a valid index within pattern:

• If the characters pointed to by i and j match, then write i + 1 to index j of the table and increment i and j.

• If the characters pointed to by i and j do not match:

– If i is not at 0, then change i to table[i – 1]. Do not increment j or write any value to the table.

– If i is at 0, then write i to index j of the table. Increment only j.

For example, for the string abacab, the failure table will be:

a b a c a b

0 0 1 0 1 2

For the string ababac, the failure table will be:

a b a b a c

0 0 1 2 3 0

For the string abaababa, the failure table will be:

a b a a b a b a

0 0 1 1 2 3 2 3

For the string aaaaaa, the failure table will be:

a a a a a a

0 1 2 3 4 5

Searching Algorithm

For the main searching algorithm, the search acts like a standard brute-force search for the most part, but in the case of a mismatch:

• If the mismatch occurs at index 0 of the pattern, then shift the pattern by 1.

• If the mismatch occurs at index j of the pattern and index i of the text, then shift the pattern such that index failure[j-1] of the pattern lines up with index i of the text, where failure is the failure table. Then, continue the comparisons at index i of the text (or index failure[j-1] of the pattern). Do not restart at index 0 of the pattern.

In addition, if the whole pattern is ever matched, instead of shifting the pattern over by 1 to continue searching for more matches, the pattern should be shifted so that the pattern at index failure[j-1], where j is at pattern.length, aligns with the index after the match in the text. KMP treats a match as a “mismatch” on the character immediately following the match.

Boyer-Moore

Last Occurrence Table

Key properties of Boyer-Moore include matching characters starting at the end of the pattern, rather than the beginning and skipping along the text in jumps of multiple characters rather than searching every single character in the text.

The shifting rule considers the character in the text at which the comparison process failed (assuming that a failure occurred). If the last occurrence of that character is to the left in the pattern, shift so that the pattern occurrence aligns with the mismatched text occurrence. If the last occurrence of the mismatched character does not occur to the left in the pattern, shift the pattern over by one (to prevent the pattern from moving backwards). In addition, if the mismatched character does not exist in the pattern at all (no value in last table) then pattern shifts completely past this point in the text.

For finding multiple occurrences, if you find a match, shift the pattern over by one and continue searching.

Rabin-Karp

Note: You must use the exact rolling hash function specified in the javadocs. You are not allowed to use Math.pow() for the intial hash calculation, nor are you allowed to use it for updating the text hash. This is because exponentiating a number is not an O(1) operation, so creating your own custom power method is also inefficient.

Grading

Here is the grading breakdown for the assignment. There are various deductions not listed that are incurred when breaking the rules listed in this PDF, and in other various circumstances.

Methods:

kmp 15pts

buildFailureTable 10pts

boyerMoore 15pts

buildLastTable 10pts

rabinKarp 25pts

Other:

Checkstyle 10pts

Efficiency 15pts

Total: 100pts

JUnits

If you need help on running JUnits, there is a guide, available on Canvas under Files, to help you run JUnits on the command line or in IntelliJ.

Style and Formatting

Javadocs

Vulgar/Obscene Language

Any submission that contains profanity, vulgar, or obscene language will receive an automatic zero on the assignment. This policy applies not only to comments/javadocs, but also things like variable names. Exceptions

When throwing exceptions, you must include a message by passing in a String as a parameter. The message must be useful and tell the user what went wrong. “Error”, “BAD THING HAPPENED”, and “fail” are not good messages. The name of the exception itself is not a good message. For example:

Bad: throw new IndexOutOfBoundsException(‘‘Index is out of bounds.’’);

Good: throw new IllegalArgumentException(‘‘Cannot insert null data into data structure.’’);

Generics

If available, use the generic type of the class; do not use the raw type of the class. For example, use new LinkedList&lt;Integer&gt;() instead of new LinkedList(). Using the raw type of the class will result in a penalty.

Forbidden Statements

• package

• System.arraycopy()

• clone()

• assert()

• Arrays class

• Array class

• Thread class

• Collections class

• Collection.toArray()

• Reflection APIs

• Inner or nested classes

• Lambda Expressions

• Method References (using the :: operator to obtain a reference to a method)

• Math.pow() (for this homework only)

If you’re not sure on whether you can use something, and it’s not mentioned here or anywhere else in the homework files, just ask.

Debug print statements are fine, but nothing should be printed when we run your code. We expect clean runs – printing to the console when we’re grading will result in a penalty. If you submit these, we will take off points.

Provided

The following file(s) have been provided to you. There are several, but we’ve noted the ones to edit.

1. PatternMatching.java

This is the class in which you will implement the different pattern matching algorithms. Feel free to add private static helper methods but do not add any new public methods, new classes, instance variables, or static variables.

2. CharacterComparator.java

This is a comparator that will be used to count the number of comparisons used. You must use this comparator. Do not modify this file.

3. PatternMatchingStudentTests.java

This is the test class that contains a set of tests covering the basic algorithms in the PatternMatching class. It is not intended to be exhaustive and does not guarantee any type of grade. Write your own tests to ensure you cover all edge cases.

Deliverables

You must submit all of the following file(s). Make sure all file(s) listed below are in each submission, as only the last submission will be graded. Make sure the filename(s) matches the filename(s) below, and that only the following file(s) are present. The only exception is that Canvas will automatically append a -n depending on the submission number to the file name(s). This is expected and will be handled by the TAs when grading as long as the file name(s) before this add-on matches what is shown below. If you resubmit, be sure only one copy of each file is present in the submission. If there are multiple files, do not zip up the files before submitting; submit them all as separate files.

Once submitted, double check that it has uploaded properly on Canvas. To do this, download your uploaded file(s) to a new folder, copy over the support file(s), recompile, and run. It is your sole responsibility to re-test your submission and discover editing oddities, upload issues, etc.

1. PatternMatching.java
