# Appium

STep1:-Install android studio(android sdk) and nodejs(npm) using commands-
                     
		    	curl -sL https://deb.nodesource.com/setup_8.x | sudo -E bash -
                    
		   	sudo apt-get install -y nodejs
                      
                     
Step2:- install appium using commands-

npm install -g appium

npm install wd 

appium &


Step3:-start appium using command-

appium


Step4:-now create a project in eclipse

Step5:-add jar files to project-

1.selenium jar files

2.selenium-server-standalone-3.8.1 jar file

3.java-client-6.0.0-BETA1 jar files(download it 1st).

Step6:-connect your device with system and get the device id by writing "adb devices" on terminal install adb devices 1st(sudo apt install adb)

Step7:-write code

public class AppiumTest {

public static void main(String[] args) throws InterruptedException, MalformedURLException

{

//String AppPath = "/home/mubashir/Videos/goplay.apk";

//Set the Desired Capabilities

DesiredCapabilities caps = new DesiredCapabilities();

caps.setCapability("deviceName", "My Phone");

caps.setCapability("udid", "674862d4"); //Give Device ID of your mobile phone

caps.setCapability("platformName", "Android");

caps.setCapability("platformVersion", "5.1.1");

//caps.setCapability("app", AppPath);

caps.setCapability("appPackage", "com.goplaybook");

caps.setCapability("appActivity", "com.goplaybook.activities.MainActivity");

caps.setCapability("noReset", "true");


			

AppiumDriver<MobileElement> driver = new AndroidDriver<MobileElement>(new URL("http://0.0.0.0:4723/wd/hub"), caps);

driver.manage().timeouts().implicitlyWait(600, TimeUnit.SECONDS);

Thread.sleep(5000);

driver.findElement(By.id("com.goplaybook:id/mobileNoET")).sendKeys("7500355112");

password.click();



}

}


Step8:-get 

caps.setCapability("appPackage", "com.goplaybook");

caps.setCapability("appActivity", "com.goplaybook.activities.MainActivity");
           
by install app in mobile apk info here select your app and find app package and appactivity.

STep9-now to find the element id install uiautomaterviewer by using command

sudo apt install androidsdk-uiautomatorviewer


Step10-now finall run the command

uiautomatorviewer
 and find the element
