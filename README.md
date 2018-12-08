# Se--WebDriver-Basics

package SeleniumSession;

import org.openqa.selenium.WebDriver;
import org.openqa.selenium.chrome.ChromeDriver;
import org.openqa.selenium.firefox.FirefoxDriver;

public class WebDriverBasics {

	public static void main(String[] args) {
		
		//System.setProperty("webdriver.gecko.driver", "C:\\Users\\Arun\\Downloads\\geckodriver-v0.23.0-win64\\geckodriver.exe");
		//System.setProperty("webdriver.gecko.driver", "C:\\Users\\Arun\\eclipse-workspace\\Selenium\\lib\\geckoDriver\\geckodriver.exe");
		
		//WebDriver driver = new FirefoxDriver();
		
		System.setProperty("webdriver.chrome.driver", "C:\\Users\\Arun\\eclipse-workspace\\Selenium\\lib\\chromedrivers\\chromedriver.exe");
		WebDriver driver = new  ChromeDriver();
		
		driver.get("http://www.seleniumhq.org");
		
		String title = driver.getTitle();
		System.out.println("title: " + title);
		
		if(title.equals("Selenium - Web Browser Automation"))
			System.out.println("Correct");
		else
			System.out.println("Not correct");
		
		System.out.println(driver.getCurrentUrl());
		
		//driver.quit();
	}
	
}
