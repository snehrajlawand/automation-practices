// this is sample 
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.chrome.ChromeDriver;
import org.openqa.selenium.TakesScreenshot;
import org.openqa.selenium.OutputType;
import java.io.File;
import org.apache.commons.io.FileUtils; // For FileUtils.copyFile

public class ScreenshotExample {
    public static void main(String[] args) {
        System.setProperty("webdriver.chrome.driver", "path/to/chromedriver"); // Set path to your ChromeDriver
        WebDriver driver = new ChromeDriver();

        try {
            driver.get("https://www.example.com");

            // Convert WebDriver object to TakesScreenshot
            TakesScreenshot ts = (TakesScreenshot) driver;

            // Get the screenshot as a file
            File sourceFile = ts.getScreenshotAs(OutputType.FILE);

            // Define the destination file path
            File destinationFile = new File("./screenshots/visible_screenshot.png");

            // Copy the source file to the destination
            FileUtils.copyFile(sourceFile, destinationFile);

            System.out.println("Screenshot of visible viewport captured successfully!");

        } catch (Exception e) {
            e.printStackTrace();
        } finally {
            driver.quit();
        }
    }
}
