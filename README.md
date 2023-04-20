# Lab-8_202001229

# Name : Divyesh Baravaliya
# Lab 8

Goal:
The goal of this lab is to learn how to use JUnit to write unit tests for Java programs.

Preliminary: Learn about JUnit in Eclipse:
The primary goal of unit testing is to take the smallest piece of testable software in an
application, isolate it from the remainder of the code, and determine whether or not it behaves
the way you expect it to behave. Each unit is tested separately before integrating it into the
rest of the program. In other words, classes should be tested in isolation from other classes
(test the methods of a class before you use the class elsewhere). Unit testing has proven its
value in that a large percentage of defects are identified during unit testing.

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
// returns true if this boa constrictor is healthy
public boolean isHealthy(){
	return this.favoriteFood.equals("granola bars");
}
// returns true if the length of this boa constrictor is
// less than the given cage length
public boolean fitsInCage(int cageLength){
	return this.length < cageLength;
}
```

![img1](https://user-images.githubusercontent.com/77344495/233327696-e91e1ba3-1ea5-452e-a9df-dce1ed26a48f.png)


```
  private Boa jen;
  private Boa ken;
  
	@Before
	public void setUp() throws Exception {
	jen = new Boa("Jennifer", 2, "grapes");
	ken = new Boa ("Kenneth", 3, "granola bars");
	}

	@Test
	public void testIsHealthy() {
		assertTrue(ken.isHealthy()); // isHealthy() will return true
		assertFalse(jen.isHealthy()); // isHealthy() will return false
	}
	

	@Test
	public void testFitsInCage() {
		assertTrue(jen.fitsInCage(3));
		assertFalse(ken.fitsInCage(1));
	}
```

In the first test case, I am testing the isHealthy method of the Boa class. I created two Boa objects with different favorite foods, and verify that isHealthy returns true for the first object and false for the second object.
In the second test case, I am testing the fitsInCage method of the Boa class. I created two Boa objects with different lengths, and test whether they fit in cages of different lengths.

Here, for ken ishealthy() will return true and for jen ishealthy() will return false so testcases are valid.

![img2](https://user-images.githubusercontent.com/77344495/233329464-9feeacb1-2bdf-404c-bb2e-b7ef11f8e506.png)

Here, for ken ishealthy() will return true and for jen ishealthy() will return false so testcases are invalid.

![img3](https://user-images.githubusercontent.com/77344495/233330349-d71c98fa-9f6d-426a-8c90-a4a9f6a92707.png)

Here, for fitsInCage() will return true if cagelength > 2 for jen and fitsInCage() will return true if cagelength > 3 for ken. so our testcases are valid.
Added assertions to the testFitsInCage method to check that the fitsInCage method returns the expected results for both jen and ken when the cage length is less than, equal to, and greater than the length of the boa.
Note that the testFitsInCage method is now more robust, as it checks the behavior of the fitsInCage method for different input values.



# Code is updated with lengthInInches()
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
// returns true if this boa constrictor is healthy
public boolean isHealthy(){
	return this.favoriteFood.equals("granola bars");
}
// returns true if the length of this boa constrictor is
// less than the given cage length
public boolean fitsInCage(int cageLength){
	return this.length < cageLength;
}

//produces the length of the Boa in inches
public int lengthInInches(){
//you need to write the body of this method
	return this.length * 12;
}
```

![img5](https://user-images.githubusercontent.com/77344495/233333382-d93dd5ad-0b43-4f89-9315-85b80155c1d4.png)

Here, lengthInInches() will return length of object in inches. so for jen it will return 24 and for ken it will return 36. so testcases are valid.
