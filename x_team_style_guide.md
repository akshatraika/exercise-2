# X-Team 15 Style Guide
We will use the CS300 course style guide (Gary's style guide) because we believe it is straightforward and will be valuable to allow us to have uniform code and to communicate the functionality with each other.  http://cs300-www.cs.wisc.edu/wp/index.php/2017/08/15/cs300-java-style-guide/

**##Source Files**
File Name
The source file name consists of the case-sensitive name of the top-level class it contains (of which there is exactly one), plus the .java extension.

File Encoding: UTF-8
Source files are encoded in UTF-8.

File Organization -
Each source file consists of, in order:

A file header comment in exactly the following form:
//////////////////// ALL ASSIGNMENTS INCLUDE THIS SECTION /////////////////////
//
// Title:           (descriptive title of the program making use of this file)
// Files:           (a list of all source files used by that program)
// Course:          (course number, term, and year)
//Team Number:      (X 15)
// Author:          (all memebrs' name)
// Email:           (all members' @wisc.edu email address)
// Lecturer's Name: (name of our lecturer)
//
//////////////////// PAIR PROGRAMMERS COMPLETE THIS SECTION ///////////////////
All import statements (if any are needed).  Wildcard imports are not used.
Exactly one top-level class (with appropriate javadoc documentation).  The contents of this class may be ordered in a logical fashion of your choosing.
… with exactly one blank line separating each section that is present

**##Layout:**
4 spaces indentation.
Include a line break after the opening brace.
Include a line break before the closing brace.
Do not group parentheses
use capitol letters for long, unsigned etc extensions 
## Naming conventions
Same as class guide.
example:
functionName and ClassName
### Examples
* interfaces -- UpperCamelCase
* classes -- UpperCamelCase
* exception types -- UpperCamelCaseException
* fields -- lowerCamelCase
* methods   -- lowerCamelCase
* parameters   -- lowerCamelCase
* local variables  -- lowerCamelCase
* instance constants  -- All caps ---- VARIABLE_NAME
* class constants   --- All Caps: CONSTANT_NAME

## Commenting style for public and private members of a class or interface:

commenting would also be same as cs300 style guide. 
Use 
/*
*
*/
for long comments and // for short comments.
### Examples

* classes  
```java
/** 
 * The HelloWorldApp class implements an application that
 * simply displays "Hello World!" to the standard output.
 */
class HelloWorldApp {
    public static void main(String[] args) {
        System.out.println("Hello World!"); //Display the string.
    }
}
   ```
* fields   -- short explaination
```java
 //Keeps track of all usernames in the system.   
private List<String> usernames = new ArrayList<>();
* constructors  
 ```java
/** Default Constructor.
 *  The default behaviour of this object is
 *  <ul>
 *  <li>XXX is true</li>
 *  <li>YYY is null</li>
 *  </ul>
 */
public MyObject() {
}
 ```
* methods
```java
/**
 * Returns an Image object that can then be painted on the screen. 
 * The url argument must specify an absolute {@link URL}. The name
 * argument is a specifier that is relative to the url argument. 
 * <p>
 * This method always returns immediately, whether or not the 
 * image exists. When this applet attempts to draw the image on
 * the screen, the data will be loaded. The graphics primitives 
 * that draw the image will incrementally paint on the screen. 
 *
 * @param  url  an absolute URL giving the base location of the image
 * @param  name the location of the image, relative to the url argument
 * @return      the image at the specified URL
 * @see         Image
 */
 public Image getImage(URL url, String name) {
        try {
            return getImage(new URL(url, name));
        } catch (MalformedURLException e) {
            return null;
        }
 }
```
