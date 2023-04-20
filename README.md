# Lab-8_202001229


Lab Exercises

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
