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


Adding label
===
```java
import java.awt.Color;
import java.awt.Font;
import javax.swing.BorderFactory;
import javax.swing.ImageIcon;
import javax.swing.JFrame;
import javax.swing.JLabel;
import javax.swing.border.Border;

public class main {
	
	public static void main(String[] args) {
		
		ImageIcon pic = new ImageIcon("pic1.png");
		
		Border border = BorderFactory.createLineBorder(Color.white, 10);
		
		JLabel label = new JLabel();	// create label
		label.setText("Morning ```````````````");		// set text of label
		label.setIcon(pic);
		label.setHorizontalTextPosition(JLabel.CENTER);
		label.setVerticalTextPosition(JLabel.TOP);		// text location of image
		label.setForeground(new Color(230,200, 230));
		label.setFont(new Font("MV Boli", Font.PLAIN,20));	// set font of text 
		label.setIconTextGap(3);	// set gap of text to the image
		label.setBackground(new Color(180,150, 180));
		label.setOpaque(true);
		label.setBorder(border);
		label.setVerticalAlignment(JLabel.CENTER);
		label.setHorizontalAlignment(JLabel.CENTER);
		//label.setBounds(0,0,400,400);		//set the x and y position of label
		
		
		JFrame frame = new JFrame();  // create a frame
		frame.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);  // exit the application
		frame.setVisible(true);  // make frame visible
		frame.setSize(600, 600);	// set the x dimension and y dimension
		//ImageIcon image = new ImageIcon("logo.png");
		//frame.setIconImage(image.getImage()); // change icon of frame
		//frame.getContentPane().setBackground(new Color(230,200, 230));	// change color of background  (0,0,0) --black
																		// can be RGB or oxffffff
		frame.setLayout(null);
		
		frame.add(label);
		
		frame.pack();
		
		
	}
	
}
```
