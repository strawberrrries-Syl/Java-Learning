How to play a clip of audio:
===
1. need .wav file
2.  code:
```java
import javax.sound.sampled.*;

import java.io.File;
import java.io.IOException;
import java.util.Scanner;

public class main {
	
	public static void main(String[] args) throws UnsupportedAudioFileException, IOException, LineUnavailableException {
		
		Scanner scanner = new Scanner(System.in);  
		
		File file = new File("Busy City - TrackTribe.wav");
		AudioInputStream audiostream = AudioSystem.getAudioInputStream(file);
		 
		Clip clip  = AudioSystem.getClip();
		clip.open(audiostream);
		
		String response = "";
		
		while(!response.equals("Q")) {
			System.out.println("P = play, S = stop, R = reset, Q = quit");
			System.out.print("Please enter your choice: ");
			
			response = scanner.next();
			response = response.toUpperCase();
			
			switch(response) {
				case "Q" : clip.close(); break;
				case "P" : clip.start(); break;
				case "S" : clip.stop(); break;
				case "R" : clip.setMicrosecondPosition(0); break;
				default: System.out.println("Not a response");
			}
			
		}
		
		System.out.println("See you next time!");
	}
	
}
```
