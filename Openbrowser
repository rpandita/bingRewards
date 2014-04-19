package hello;

import java.awt.Desktop;
import java.io.IOException;
import java.net.URI;
import java.net.URISyntaxException;

public class Openbrowser {
	public static void main(String[] args) {
		String url = "http://www.bing.com/search?q=hello";
		String url2 = "http://www.bing.com/rewards/dashboard";
		if (Desktop.isDesktopSupported()) {
			Desktop desktop = Desktop.getDesktop();
			try {
				// using the default browser chrome for searches
				desktop.browse(new URI(url2));
				Thread.sleep(3000);
				for (int i = 0; i < 34; i++) {
					desktop.browse(new URI(url + i));
					Thread.sleep(3000);
				}
				Runtime.getRuntime().exec("taskkill /F /IM chrome.exe");
				
				//using firefox for searches
				Runtime.getRuntime().exec("cmd /c start firefox "+url2);
				Thread.sleep(3000);
				for (int i = 0; i < 32; i++) {
					Runtime.getRuntime().exec("cmd /c start firefox "+url+i);
					Thread.sleep(3000);
				}
				Runtime.getRuntime().exec("taskkill /F /IM firefox.exe");
				
				// using internet explorer
				Runtime.getRuntime().exec("cmd /c start iexplore "+url2);
				Thread.sleep(3000);
				for (int i = 0; i < 32; i++) {
					Runtime.getRuntime().exec("cmd /c start iexplore "+url+i);
					Thread.sleep(4000);
					Runtime.getRuntime().exec("taskkill /F /IM iexplore.exe");
					Thread.sleep(1000);
				}
				Runtime.getRuntime().exec("taskkill /F /IM iexplore.exe");
				
				//using opera for searches
				Runtime.getRuntime().exec("cmd /c start opera "+url2);
				Thread.sleep(3000);
				for (int i = 0; i < 32; i++) {
					Runtime.getRuntime().exec("cmd /c start opera "+url+i);
					Thread.sleep(3000);
				}
				Runtime.getRuntime().exec("taskkill /F /IM opera.exe");
				
				// using safari 
				Runtime.getRuntime().exec("cmd /c start safari "+url2);
				Thread.sleep(3000);
				for (int i = 0; i < 32; i++) {
					Runtime.getRuntime().exec("cmd /c start safari "+url+i);
					Thread.sleep(4000);
					Runtime.getRuntime().exec("taskkill /F /IM safari.exe");
					Thread.sleep(1000);
				}
				Runtime.getRuntime().exec("taskkill /F /IM safari.exe");

			} catch (IOException | URISyntaxException e) {
				// TODO Auto-generated catch block
				e.printStackTrace();
			} catch (InterruptedException e) {
				// TODO Auto-generated catch block
				e.printStackTrace();
			}
		} else {
			Runtime runtime = Runtime.getRuntime();
			try {
				runtime.exec("xdg-open " + url);
			} catch (IOException e) {
				// TODO Auto-generated catch block
				e.printStackTrace();
			}
		}
	}
}
