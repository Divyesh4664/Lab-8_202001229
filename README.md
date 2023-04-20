# Lab-8_202001229


Lab Exercises

![img1](https://user-images.githubusercontent.com/77344495/233323107-2d547a97-1aad-4f8c-8b7d-a453d07df375.png)

	private Boa jen;
	private Boa ken;
	
	@Before
	public void setUp() throws Exception {
	jen = new Boa("Jennifer", 2, "grapes");
	ken = new Boa ("Kenneth", 3, "granola bars");
	}

	@Test
	public void testIsHealthy() {
		assertTrue(ken.isHealthy());
		assertFalse(jen.isHealthy());
	}
	

	@Test
	public void testFitsInCage() {
		assertTrue(jen.fitsInCage(3));
		assertFalse(ken.fitsInCage(1));
	}
