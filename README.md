"# selenium-test" 
# 2019-ITCS473-SodaAndTheBoys
### Automated Web Testing using Selenium

The website which we tested is `<link>` : <https://thaiortho.org/> thats about The Thai Association of Orthodontists.

There are 12 test cases that tested this website as list below:
                
1. Get page title text to find whether access correct webpage 
2. Go to FindDentist page from Homepage's nav bar
3. Search by inputting name into search box
4. Search by inputting Country into search box then appears the error alert
5. Access the Facebook page from Thaiortho.org website
6. Access the Youtube channel from Thaiortho.org website
7. Access the Category page
8. Make a Online Payment
9. 
10.
11.
12. 


Which function of the website that the test covers? For example, this test case checks the login of the website using valid/invalid inputs.
What is the expected outputs of the tests?

**Test Case #1** : Get page title text to find whether access correct webpage.

	public static void accessHomepage() {
			WebDriver driver = new ChromeDriver();
			String baseUrl = "https://thaiortho.org/";
			String expectedTitleHome = "สมาคมทันตแพทย์จัดฟันแห่งประเทศไทย";
			String actualTitleHome = "";

			driver.get(baseUrl);

			// get the actual value of the title
			WebElement elementHome = driver.findElement(By.xpath(page_title_home));
			actualTitleHome = elementHome.getText();

			if (actualTitleHome.contentEquals(expectedTitleHome)) {
				System.out.println("Test 1 Passed!");
			} else {
				System.out.println("Test 1 Failed");
			}

			driver.close();
		}

Expected Output: The page title of accessing page must names "สมาคมทันตแพทย์จัดฟันแห่งประเทศไทย"



