# Tag-Checker
A console application that receives a string containing tags (similar to HTML tags) as input, and outputs a string describing if the tags are correctly formatted.

## Task: 
```
Write a program to check that all the tags in a given piece of text (a paragraph) are correctly nested, and
that there are no missing or extra tags. An opening tag for this problem is enclosed by angle brackets,
and contains exactly one upper case letter, for example <T>, <X>, <S>. The corresponding closing tag will
be the same letter preceded by the symbol /; for the examples above these would be </T>, </X>, </S>.

If the paragraph is correctly tagged then output the line “Correctly tagged paragraph”, otherwise output
a line of the form “Expected <expected> found <unexpected>” where <expected> is the closing tag
matching the most recent unmatched tag and <unexpected> is the closing tag encountered. If either of
these is the end of paragraph, i.e. there is either an unmatched opening tag or no matching closing tag at
the end of the paragraph, then replace the tag or closing tag with #. 
  
These points are illustrated in the examples below which should be followed exactly as far as spacing is concerned
```

## Example:

### Sample Input
```
- The following text<C><B>is centred and in boldface</B></C>
- <B>This <\g>is <B>boldface</B> in <<*> a</B> <\6> <<d>sentence
- <B><C> This should be centred and in boldface, but the tags are wrongly nested </B></C>
- <B>This should be in boldface, but there is an extra closing tag</B></C>
- <B><C>This should be centred and in boldface, but there is a missing closing tag</C>
``` 
### Sample Output (for above input)
```
- Correctly tagged paragraph
- Correctly tagged paragraph
- Expected </C> found </B>
- Expected # found </C>
- Expected </B> found #
```
