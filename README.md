<div align="center">

## Swing Tutorial & double button listener


</div>

### Description

Learn swing basic and double button listener (easy way)
 
### More Info
 


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[J\-f Mitchell](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/j-f-mitchell.md)
**Level**          |Beginner
**User Rating**    |4.8 (19 globes from 4 users)
**Compatibility**  |Java \(JDK 1\.1\), Java \(JDK 1\.2\)
**Category**       |[Controls/ Forms/ Graphics/ Menus](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/controls-forms-graphics-menus__2-59.md)
**World**          |[Java](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/java.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/j-f-mitchell-swing-tutorial-double-button-listener__2-3077/archive/master.zip)





### Source Code

```
// Copyright J-f Mitchell, this litle peace of code is a great
// tutorial for swing begigner.
import java.awt.*;
import java.awt.event.*;
import javax.swing.*;
public class JavaApp {
	JFrame frame1;
	JButton command1;
	JTextField text1; //Declaring variables in class to able to use it in the whole class.
	JPanel panel1;
	JButton command2;
	public JavaApp() {
		frame1 = new JFrame("Put your title here"); //Main frame
	frame1.setSize(50, 50);
		command1 = new JButton("Button 1"); // creating control from declared variable in the class
		text1 = new JTextField(20);
		panel1 = new JPanel();
		command2 = new JButton("Button 2");
			command1.setMnemonic(KeyEvent.VK_I); //This is an event listener without the implements in the class, I like this method!
    command1.addActionListener(new ActionListener() {
      public void actionPerformed(ActionEvent e) {
    text1.setText("Button 1!");
      }
    });
				command2.setMnemonic(KeyEvent.VK_I); // listener for the second button
    command2.addActionListener(new ActionListener() {
      public void actionPerformed(ActionEvent e) {
    text1.setText("Button 2!");
      }
    });
		panel1.setLayout(new FlowLayout());
		panel1.add(text1);
		panel1.add(command1); //adding components to pane, you need this to be able to see ure component,
		panel1.add(command2);
		frame1.getContentPane().add(panel1, BorderLayout.CENTER); //add my pane to my frame
    // Exit when the window is closed.
    frame1.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
	// show the frame!
	frame1.pack();
	frame1.setVisible(true);
}
 public static void main(String[] args) {
	// set the look and feel
	try {
	  UIManager.setLookAndFeel(
		UIManager.getCrossPlatformLookAndFeelClassName()); //getting the java swing look
	} catch(Exception e) {}
	JavaApp javaapp = new JavaApp(); // tell the program to show up the frame by calling my GUI function
  }
}
```

