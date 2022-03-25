# Challenge-5-
Recursion
package challenge5;

/**
 *
 * @author user
 */
public class Challenge5 {

    /**
     * @param args the command line arguments
     */
    public static void main(String[] args) {
        System.out.println(transform("codex"));
        System.out.println(transform("xxhixx"));
        System.out.println(transform("xhixhix"));
        System.out.println(transform("xxabcxdxexf")); //replace with a variable that was user input
    }
    
    public static String transform (String str) {
        
        if (str.length()==0)   //base case
        {
        return str;   // no more calls to transform
                      // return something
        }   
        else if (str.charAt(0) == ('x'))
        {
        return 'y' + transform(str.substring(1));  //replace the x with a y
        }                                        
        else
        {
        return str.charAt(0) + transform(str.substring(1)); //leave the letter alone
        }
 
    }

    
}
