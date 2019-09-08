# useDelimiter

import java.util.*; 
import java.util.regex.Pattern; 

public class HelloWorld {
  public static void main(String[] args) {
  
  	String s = "AGTC"; 
  	
  	//Create Key/Value pairs
  	Map<String, String> pair1 = new HashMap<String, String>();
	pair1.put("A", "T");
	pair1.put("T", "A");
	
	Map<String, String> pair2 = new HashMap<String, String>();
	pair2.put("G", "C");
	pair2.put("C", "G");
  	
	Scanner scanner = new Scanner(s); 
		
	//define tokens to pair up
	scanner.useDelimiter(Pattern.compile("(A|T),(G|C),(T|A),(C|G)")); 

	//display original order
	while(scanner.hasNext()){
          System.out.println(scanner.next());
	}
	
	//display key/value pair order
	  System.out.print(pair1.get("A"));
	  	  System.out.print(pair2.get("G"));
	  System.out.print(pair1.get("T"));
	  	  System.out.print(pair2.get("C"));      

	// close the scanner 
	scanner.close(); 

  }
}
