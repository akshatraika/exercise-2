# X-Team 15 Style Guide
We will use the CS300 course style guide (Gary's style guide).  http://cs300-www.cs.wisc.edu/wp/index.php/2017/08/15/cs300-java-style-guide/
<brief description of your team's opinion or philosophy regarding Style Guides>

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

### Examples

* classes  
/** 
 * The HelloWorldApp class implements an application that
 * simply displays "Hello World!" to the standard output.
 */
class HelloWorldApp {
    public static void main(String[] args) {
        System.out.println("Hello World!"); //Display the string.
    }
}
* fields   -- short explaination
 //Keeps track of all usernames in the system.   
private List<String> usernames = new ArrayList<>();
* constructors  
 
/** Default Constructor.
 *  The default behaviour of this object is
 *  <ul>
 *  <li>XXX is true</li>
 *  <li>YYY is null</li>
 *  </ul>
 */
public MyObject() {
}
 
* methods
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

