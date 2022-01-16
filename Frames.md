How to create a frame
===
```java

import java.awt.Color;

import javax.swing.ImageIcon;
import javax.swing.JFrame;

public class main {
	
	public static void main(String[] args) {
		
		/*JFrame this = new JFrame();  // create a this
		
		this.setTitle("Title");  // set title of this
		
		this.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);  // exit the application
		
		this.setResizable(false);	// prevent this from being resized
		
		this.setVisible(true);  // make this visible
		
		this.setSize(420, 420);	// set the x dimension and y dimension
		
		ImageIcon image = new ImageIcon("logo.png");
		
		this.setIconImage(image.getImage()); // change icon of this
		
		this.getContentPane().setBackground(new Color(230,200, 230));	// change color of background  (0,0,0) --black
																		// can be RGB or oxffffff
		*/
		
		MyFrame myframe = new MyFrame(); 
	}
	
}


public class MyFrame extends JFrame{
	MyFrame() {
		
		this.setTitle("Title");  // set title of this
		
		this.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);  // exit the application
		
		this.setResizable(false);	// prevent this from being resized
		
		this.setVisible(true);  // make this visible
		
		this.setSize(420, 420);	// set the x dimension and y dimension
		
		ImageIcon image = new ImageIcon("logo.png");
		
		this.setIconImage(image.getImage()); // change icon of this
		
		this.getContentPane().setBackground(new Color(230,200, 230));
	}
}
```
