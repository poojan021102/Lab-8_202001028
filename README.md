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
![image](https://user-images.githubusercontent.com/94627901/233060696-49217ce6-6189-406c-aff1-5f8e2a98f8d4.png)

### Writing BoaTest in java
```import static org.junit.Assert.*;

import org.junit.Before;
import org.junit.Test;

public class BoaTest {
	Boa jen,en;
	@Test
	public void testIsHealthy() {
		assertEquals("Error in isHealthy()",false,jen.isHealthy());
		assertEquals("Error in isHealthy()",true,jen.isHealthy());
		assertEquals("Error in isHealthy()",false,en.isHealthy());
		assertEquals("Error in isHealthy()",true,en.isHealthy());
	}

	@Test
	public void testFitsInCage() {
		assertEquals("Error in fitsInCage()",true,en.fitsInCage(10));
		assertEquals("Error in fitsInCage()",true,en.fitsInCage(0));
		assertEquals("Error in fitsInCage()",false,en.fitsInCage(1));
		assertEquals("Error in fitsInCage()",false,en.fitsInCage(20));
	}
	
	@Before
	public void setUp() throws Exception {
		jen = new Boa("Jennifer", 2, "grapes");
		en = new Boa ("Kenneth", 3, "granola bars");
	}
}

```
![image](https://user-images.githubusercontent.com/94627901/233060832-036af479-15cb-4dfd-9859-09daed33fdb7.png)
![image](https://user-images.githubusercontent.com/94627901/233062375-df9b091a-60d0-4c2e-824e-65f525dea679.png)


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
```
import static org.junit.Assert.*;

import org.junit.Before;
import org.junit.Test;

public class BoaTest {
	Boa jen,en;
	@Before
	public void setUp() throws Exception {
		jen = new Boa("Jennifer", 2, "grapes");
		en = new Boa ("Kenneth", 3, "granola bars");
	}
	
	@Test
	public void testIsHealthy() {
		assertEquals("Error in isHealthy()",false,jen.isHealthy());
		assertEquals("Error in isHealthy()",true,jen.isHealthy());
		assertEquals("Error in isHealthy()",false,en.isHealthy());
		assertEquals("Error in isHealthy()",true,en.isHealthy());
	}

	@Test
	public void testFitsInCage() {
		assertEquals("Error in fitsInCage()",true,en.fitsInCage(10));
		assertEquals("Error in fitsInCage()",1,en.fitsInCage(0));
		assertEquals("Error in fitsInCage()",false,en.fitsInCage(1));
		assertEquals("Error in fitsInCage()",0,en.fitsInCage(20));
	}
	@Test
	public void testLength() {
		assertEquals("Error in lengthInInches()",4,en.lengthInInches(10));
		assertEquals("Error in lengthInInches()",0,en.lengthInInches(0));
		assertEquals("Error in lengthInInches()",0,en.lengthInInches(1));
		assertEquals("Error in lengthInInches()",8,en.lengthInInches(20));
	}
}
```
![image](https://user-images.githubusercontent.com/94627901/233061893-05b93f6f-6f04-477c-b08f-c3bb18e4a2cf.png)

![image](https://user-images.githubusercontent.com/94627901/233061851-6997e5da-5d3b-4978-9b60-e319d3666dab.png)


