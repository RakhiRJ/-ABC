package Automation;

import org.openqa.selenium.By;
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.WebElement;
import org.openqa.selenium.edge.EdgeDriver;
import org.openqa.selenium.interactions.Actions;
import org.openqa.selenium.support.FindBy;

public class DragandDropHandling {
	public static void main(String[] args) throws InterruptedException {
		System.setProperty("WebDriver.edge.driver", "C:\\Users\\RUSHIKESH\\Downloads\\edgedriver_win64 (2).zip");
		WebDriver dri = new EdgeDriver();
		
		dri.get("https://demo.guru99.com/test/drag_drop.html");
	 WebElement from = dri.findElement(By.xpath("(//a[@class=\"button button-orange\"])[2]"));
	

	 
		Thread.sleep(4000);
		
		WebElement to = dri.findElement(By.xpath("(//li[@class=\"placeholder\"])[2]"));
		Actions a = new Actions(dri);
		a.dragAndDrop(from, to).build().perform();
		
	}

}

