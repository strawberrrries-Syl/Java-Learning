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

About ArrayList
---Java
import java.util.ArrayList;

public class main {
	public static void main(String[] args) {
		
		ArrayList<String> food = new ArrayList<String>();
		
		food.add("Noodle");
		food.add("Dumpling");
		food.add("Chicken");
		System.out.println(food);
		food.add(1, "Pork");			// add at index
		System.out.println(food);
		food.remove(0);					// remove
		System.out.println(food);
		food.set(0, "Noodle");			// replace
		System.out.println(food);
		food.trimToSize();				// delete extra storage
		System.out.println(food);
		food.clear();					// clear all
		System.out.println(food);
	}
}
```
