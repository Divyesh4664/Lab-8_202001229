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


