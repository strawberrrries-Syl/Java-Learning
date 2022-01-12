How to make a simple GUI
====
```JAVA
import javax.swing.JOptionPane;

public class main {
	public static void main(String[] args) {
		
		String name = JOptionPane.showInputDialog("Enter your name");
		JOptionPane.showMessageDialog(null, "Hello "+name);
		
		int age = Integer.parseInt(JOptionPane.showInputDialog("How old are you?"));
		JOptionPane.showMessageDialog(null,"You are "+age+" years old");
		
		Double height = Double.parseDouble(JOptionPane.showInputDialog("Enter your height"));
		JOptionPane.showMessageDialog(null,"You are "+height+" cm tall");
	}
}
```
