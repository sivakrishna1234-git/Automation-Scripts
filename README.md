# Automation-Scripts
Written Automation scripts for multiple demo websites

#Class1:
package Practice;

import java.io.IOException;
import java.time.Duration;
import java.util.List;
import java.util.Set;

import org.openqa.selenium.By;
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.WebElement;
import org.openqa.selenium.chrome.ChromeDriver;
import org.openqa.selenium.interactions.Actions;

public class BasicScript2 {
	static {
		System.setProperty("webdriver.chromdriver.com", "C:\\Users\\sivakrishna.s\\Desktop\\chromedrive.exe");
	}
	static WebDriver driver;
	public static void main(String[] args) throws InterruptedException, IOException {
		driver =new ChromeDriver();
	    driver.manage().timeouts().implicitlyWait(Duration.ofSeconds(20));//implicitly wait
	    
	    //Upload documents
		driver.get("https://www.tutorialspoint.com/selenium/practice/selenium_automation_practice.php");
		WebElement upload=driver.findElement(By.id("picture"));
        Thread.sleep(5000);
		upload.sendKeys("C:\\Users\\sivakrishna.s\\Downloads\\SivakrishnaSannuResume (1).pdf");
		driver.close();

		
		//popups
		driver =new ChromeDriver();
		driver.get("https://www.tutorialspoint.com/selenium/practice/alerts.php");
		WebElement popup=driver.findElement(By.xpath("(//button[@class='btn btn-primary'])[1]"));
		popup.click();
		Thread.sleep(5000);
		driver.switchTo().alert().accept();
		driver.close();
		
		
		//mouse actions
		driver =new ChromeDriver();
		driver.get("https://demoqa.com/menu");
		WebElement hoveriver=driver.findElement(By.linkText("Main Item 2"));
		Thread.sleep(5000);
		Actions action=new Actions(driver);
		action.moveToElement(hoveriver).perform();
		driver.close();
		
		//get window handle and window handles
		driver =new ChromeDriver();
		driver.get("https://www.tutorialspoint.com/selenium/practice/browser-windows.php");
		driver.findElement(By.xpath("(//button[@class=\"btn btn-primary\"])[1]"));
		String window=driver.getWindowHandle();
		System.out.println(window);
		Set<String> list=driver.getWindowHandles();
		System.out.println(list);
		driver.quit();
		
		//findelements
		driver =new ChromeDriver();
        driver.get("https://www.google.com/");
        WebElement element=driver.findElement(By.id("q"));
        element.sendKeys("google");
        Thread.sleep(5000);
        List<WebElement> sugg=driver.findElements(By.xpath("//div[@class='fM33ce dRYYxd']/style"));
       
		int count=sugg.size();
		System.out.println(count);
		
		sugg.get(count-5).click();
		driver.close();
		
		

}
}



#Class2:

package Practice;

import java.io.IOException;
import java.time.Duration;
import java.util.List;
import java.util.Set;

import org.openqa.selenium.By;
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.WebElement;
import org.openqa.selenium.chrome.ChromeDriver;
import org.openqa.selenium.interactions.Actions;

public class BasicScript2 {
	static {
		System.setProperty("webdriver.chromdriver.com", "C:\\Users\\sivakrishna.s\\Desktop\\chromedrive.exe");
	}
	static WebDriver driver;
	public static void main(String[] args) throws InterruptedException, IOException {
		driver =new ChromeDriver();
	    driver.manage().timeouts().implicitlyWait(Duration.ofSeconds(20));//implicitly wait
	    
	    //Upload documents
		driver.get("https://www.tutorialspoint.com/selenium/practice/selenium_automation_practice.php");
		WebElement upload=driver.findElement(By.id("picture"));
        Thread.sleep(5000);
		upload.sendKeys("C:\\Users\\sivakrishna.s\\Downloads\\SivakrishnaSannuResume (1).pdf");
		driver.close();

		
		//popups
		driver =new ChromeDriver();
		driver.get("https://www.tutorialspoint.com/selenium/practice/alerts.php");
		WebElement popup=driver.findElement(By.xpath("(//button[@class='btn btn-primary'])[1]"));
		popup.click();
		Thread.sleep(5000);
		driver.switchTo().alert().accept();
		driver.close();
		
		
		//mouse actions
		driver =new ChromeDriver();
		driver.get("https://demoqa.com/menu");
		WebElement hoveriver=driver.findElement(By.linkText("Main Item 2"));
		Thread.sleep(5000);
		Actions action=new Actions(driver);
		action.moveToElement(hoveriver).perform();
		driver.close();
		
		//get window handle and window handles
		driver =new ChromeDriver();
		driver.get("https://www.tutorialspoint.com/selenium/practice/browser-windows.php");
		driver.findElement(By.xpath("(//button[@class=\"btn btn-primary\"])[1]"));
		String window=driver.getWindowHandle();
		System.out.println(window);
		Set<String> list=driver.getWindowHandles();
		System.out.println(list);
		driver.quit();
		
		//findelements
		driver =new ChromeDriver();
        driver.get("https://www.google.com/");
        WebElement element=driver.findElement(By.id("q"));
        element.sendKeys("google");
        Thread.sleep(5000);
        List<WebElement> sugg=driver.findElements(By.xpath("//div[@class='fM33ce dRYYxd']/style"));
       
		int count=sugg.size();
		System.out.println(count);
		
		sugg.get(count-5).click();
		driver.close();
		
}
}

