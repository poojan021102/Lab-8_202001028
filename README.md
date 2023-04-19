# Lab-8_202001028
# Name:  POOJAN PATEL
# ID: 202001028

### Writing Boa class in java.
```
public class Boa {
	private String name;
	private int length; // the length of the boa, in feet
	private String favoriteFood;
	public Boa (String name, int length, String favoriteFood){
		this.name = name;
		this.length = length;
		this.favoriteFood = favoriteFood;
	}
	// returns true if this boa constructor is healthy
	public boolean isHealthy(){
		return this.favoriteFood.equals("granola bars");
	}
	// returns true if the length of this boa constrictor is
	// less than the given cage length
	public boolean fitsInCage(int cageLength){
		return this.length < cageLength;
	}
}
```
![image](https://user-images.githubusercontent.com/94627901/233046737-02997fd2-531b-46ea-9d63-297d40901c9c.png)
### Writing BoaTest in java
```import static org.junit.Assert.*;

import org.junit.Before;
import org.junit.Test;

public class BoaTest {
	Boa jen,en;
	@Test
	public void testIsHealthy() {
		assertEquals("Error in isHealthy()",0,jen.isHealthy());
		assertEquals("Error in isHealthy()",1,jen.isHealthy());
		assertEquals("Error in isHealthy()",0,en.isHealthy());
		assertEquals("Error in isHealthy()",1,en.isHealthy());
	}

	@Test
	public void testFitsInCage() {
		assertEquals("Error in fitsInCage()",1,en.fitsInCage(10));
		assertEquals("Error in fitsInCage()",1,en.fitsInCage(0));
		assertEquals("Error in fitsInCage()",0,en.fitsInCage(1));
		assertEquals("Error in fitsInCage()",0,en.fitsInCage(20));
	}
	
	@Before
	public void setUp() throws Exception {
		jen = new Boa("Jennifer", 2, "grapes");
		en = new Boa ("Kenneth", 3, "granola bars");
	}
}

```
![image](https://user-images.githubusercontent.com/94627901/233046815-db85d818-e55b-48e6-8a1b-8b9c7e95744c.png)

### Now adding new function.
```/**
 * 
 */
/**
 * @author student
 *
 */
//module Junit_q1{
//	
//}
public class Boa {
	private String name;
	private int length; // the length of the boa, in feet
	private String favoriteFood;
	public Boa (String name, int length, String favoriteFood){
		this.name = name;
		this.length = length;
		this.favoriteFood = favoriteFood;
	}
	// returns true if this boa constructor is healthy
	public boolean isHealthy(){
		return this.favoriteFood.equals("granola bars");
	}
	// returns true if the length of this boa constrictor is
	// less than the given cage length
	public boolean fitsInCage(int cageLength){
		return this.length < cageLength;
	}
	// produces the length of the Boa in inches
	public int lengthInInches(int a){
	// you need to write the body of this method
		return (int) (a/2.5);
	}
}
```
![image](https://user-images.githubusercontent.com/94627901/233048567-23bbe496-f1e6-43ad-a088-8826991400e9.png)
