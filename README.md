Download Link: https://assignmentchef.com/product/solved-comp1210-activity4a-writing-classes
<br>
<strong>Terminology</strong>

<table width="536">

 <tbody>

  <tr>

   <td width="210">attribute / state behaviorclass method header class header instance variable</td>

   <td width="210">UML class diagram encapsulationclientvisibility (or access) modifieraccessor method mutator method</td>

   <td width="116">calling method method declaration method invocation return statement parameters constructor</td>

  </tr>

 </tbody>

</table>

<strong> </strong>

<strong>Goals  </strong>By the end of this activity you should be able to do the following: Ø Create a class with methods that accept parameters and return a value

<ul>

 <li>Understand the constructor and the toString method of a class</li>

 <li>Create a class with main that uses the class created above</li>

 <li>Create a jGRASP project containing all of the classes for your program</li>

 <li>Generate a UML class diagram and documentation</li>

 <li>Create a jGRASP canvas for your program and run the program in the canvas</li>

</ul>




<strong>Description </strong>

In this activity, you will create two classes: one called <strong>UserInfo</strong> and another called <strong>UserInfoDriver</strong> which contains a main method that uses the first class (i.e., UserInfoDriver creates instances of UserInfo and calls its methods).  You will also create a project, UML class diagram, and canvas for the program.

<strong> </strong>

<strong>Part 1: UserInfo.java – Create and test the UserInfo class. </strong>

<strong> </strong>

<ul>

 <li>Create your UserInfo class and add the following comments (there will be no main method in this class). Save this class in a file named UserInfo.java as soon as you have entered the code below. <u>Don’t forget to add your Javadoc comments; the constructor and each method will need one</u>.</li>

</ul>




<ul>

 <li><strong>Instance variables (or fields) represent the information that an object of the class needs to store</strong>. Declare the following variables after the comment: // instance variables o firstName: a <strong>String</strong> for the user’s first name o lastName: a <strong>String</strong> for the user’s last name o location: a <strong>String</strong> for the user’s location o age: an <strong>int</strong> for the user’s age</li>

</ul>

o status: <strong>int</strong> indicates whether the user is online or offline

Hint: Use the <em>private</em> access modifier so that values cannot be directly accessed from outside of the object; for example, declare firstName as follows:

<h1>private String firstName;</h1>




<ul>

 <li><strong>Constants store values that cannot be changed</strong>. Use constants to represent the two possible statuses of the user. Constants are usually grouped with the instance variables.</li>

</ul>

<h1>private static final int OFFLINE = 0, ONLINE = 1;</h1>

<ul>

 <li><strong>The constructor is used in conjunction with the <em>new</em> operator to create an instance of UserInfo and initialize the fields. </strong>It should be placed right below the fields and before the methods in the class; that is, right after the comment // constructor in your class.  The constructor <em><u>does not have a return type</u></em>, and it always has the <em><u>same name as the class</u></em>.  The UserInfo constructor will take two parameters as input representing the first and last name of the user.  The names for these parameters can be anything; however, many professional programmers use the convention of adding the suffix “In” to the corresponding field name as shown below.</li>

</ul>










In the constructor, store the first and last name in the appropriate instance variables:










Because you do not have inputs for age, location, and status, you will need to set those to default values:










Compile your program, click the Interactions tab, and create a new UserInfo object called <em>u</em> and display it by entering the following in Interactions tab.










Note that the odd looking value (<a href="/cdn-cgi/l/email-protection" class="__cf_email__" data-cfemail="01626d6072726f606c644169607269626e6564">[email protected]</a>), which is the object’s default toString value, is not very useful.  When we print or display <em>u</em>, we usually want to see some text that tells us something about the object.  In the Workbench tab, find <em>u</em> and unfold it to see its fields.  We can see that the fields in u do have the values that we set with constructor.  The solution is to add a <em>toString</em> method to our UserInfo class.




<strong>   </strong>

<ul>

 <li><strong>The toString method returns a String representation of the object</strong>. Create and return a local String variable called output that contains information about the UserInfo object. Place this method after the methods comment:  // methods</li>

</ul>




After you have successfully compiled your class, click the Interactions tab, and create a new

UserInfo object called <em>u</em> and display it by entering the following in Interactions tab as you did above.  This time, when <em>u</em> is evaluated, the <em>toString</em> method is implicitly invoked on <em>u</em> and the return value is displayed.







In the example above, you can also display <em>u</em> by entering the print statement in interactions:

<h1>         System.out.println(u);</h1>

When the <em>u</em> is entered without a semi-colon, it is an expression rather than a statement.  You could also enter u.toString() as an expression.  Remember, in the Interactions tab, expressions are evaluated and the result is immediately displayed.  Since u is an object, it

“evaluates” to the result of calling its <em>toString</em> method.




<ul>

 <li><strong>The methods of your class describe what your object can do (the behaviors of an object)</strong>. For a UserInfo object, we want to be able to set the <em>location</em> and <em>age</em> of the user and also to change the status.  First, create a set method for location:</li>

</ul>

<strong>After compiling your class, test it in the interactions pane:  </strong>

<strong> </strong>

<strong> </strong>

Add a method to set the value of age. This will only change age if the age is greater than 0, and it will return a boolean value (true or false) indicating whether the age was set:




Add a method to return the age (fill in the blank). Notice this method takes no parameters, but returns an int value (instead of void).

<strong> </strong>

<strong>Add the following two methods to allow the user to log off and on: </strong>

<strong> </strong>

<strong> </strong>

The actual values (0 and 1) for offline status and online status are not used in the code because they are declared as constants.  This makes code easier to read and modify later. You should also hide the values when printing the class information. Modify the toString method as follows to print “Offline” rather than 0 and “Online” rather than 1:

<strong> </strong>

<strong>After compiling your class, test each of your methods in the interactions pane. </strong>Your output should be as follows<strong>: </strong>

<strong> </strong>

<strong>  </strong>

<strong>Part 2: UserInfoDriver.java – Create UserInfoDriver class with main method; create a project file and generate the UML class diagram for the program; create canvas for UserInfoDriver and run the program in the canvas. </strong>

<strong> </strong>

<ul>

 <li><strong>UserInfoDriver class with main</strong> – You are to create another class, UserInfoDriver, which should have a main method that creates two instances of UserInfo and invokes methods on these instances. In the code below two instances of UserInfo are created and assigned to variables user1 and user2 respectively. These instances are printed after they are created.  Then after several methods are called on instances, the instances are printed again.  Enter the code below incrementally (i.e., <u>write the skeleton code first and save it as UserInfoDriver.java in the same</u> <u>folder as UserInfo</u>). Then compile/run at strategic points to ensure that the program is correct down to that point and that you understand what each statement does. <u>Don’t forget to add your</u> <u>Javadoc comments</u>.</li>

</ul>







<strong>Web-CAT</strong> – After you have created the jGRASP project in the next section, you should submit your UserInfo.java and UserInfoDriver.java files to Web-CAT via the Web-CAT button on the project toolbar.

<ul>

 <li><strong>jGRASP Project</strong> – Create a jGRASP project named UserInfoDriver then add java and UserInfo.java to the project. To do this, with UserInfoDriver in the edit window, click <strong>Project </strong> <strong>&gt;</strong> <strong>New</strong> then in the Create Project dialog enter UserInfoDriver as the Project Name; make sure the folder name is set to the folder of the source files, and click Next.  You can add the two files via the dialog, or alternatively, after the project has been created, you can drag Acivity4A.java and UserInfo.java from the Browse tab file list to project UserInfoDriver in the Open Projects list.</li>

</ul>




<table width="258">

 <tbody>

  <tr>

   <td width="258"> </td>

  </tr>

  <tr>

   <td width="258"><strong>UML Class Diagram for Project UserInfoDriver </strong></td>

  </tr>

 </tbody>

</table>

<ul>

 <li><strong>UML class diagram</strong> – After you have created the project file and added UserInfoDriver.java and UserInfo.java, you should generate the UML class diagram for the project by clicking (or <strong>Project</strong> <strong>&gt; Generate/Update UML Class Diagram</strong>).  After the diagram is generated, you should see green rectangles representing the two classes.  The red dashed arrow from UserInfoDriver to UserInfo indicates that UserInfoDriver depends on UserInfo.  If both classes are selected, deselect by clicking in the space next to the diagram.  Then select a class and drag to reposition it.  In your UML diagram, position the classes as they appear in the figure at right.</li>

</ul>




<table width="256">

 <tbody>

  <tr>

   <td width="256"> </td>

  </tr>

  <tr>

   <td width="256"><strong>Members for UserInfo  in UML Info tab </strong></td>

  </tr>

 </tbody>

</table>

<table width="313">

 <tbody>

  <tr>

   <td width="313"> </td>

  </tr>

  <tr>

   <td width="313"><strong>Dependencies in UML Info tab </strong></td>

  </tr>

 </tbody>

</table>

Right-click on UserInfo and select “Show Class

Info” to see the class member information in the UML Info tab.  See <strong>Members for UserInfo</strong> in the figure at right below the UML class diagram.




Right-click the red dashed dependency arrow and select “Show Dependencies Info” to see the dependencies of between the classes in the UML Info tab; i.e., UserInfoDriver is using the UserInfo constructor, and methods logOn, setAge, and setLocation in the UserInfo class. See figure below.




You can also create instances of the class by rightclicking and selecting “Create New Instance” which places an instance on the workbench.  To invoke a method for an object on the workbench, you can right-click on the object (not the class) and select “Invoke Method”.




<ul>

 <li><strong>jGRASP Canvas</strong> – In this part of the activity, you are to create a viewer canvas for your program. This will allow you to observe the objects created in the program as method are invoked on them.  The canvas works in conjunction with the debugger as well as interactions.</li>

</ul>




After you successfully Compile     your program, you have three ways to run

your program in jGRASP: Run , Debug           , and Run in Viewer Canvas .  In this part of the activity, we focus on Run in Viewer Canvas , which opens a canvas window on a new or existing canvas file.  When any primitive, object, or field of an object in the Debug or Workbench tabs is dragged onto the canvas, a viewer is opened using one of several viewers associated with the variable type.  Below are the basic steps for creating a canvas for your program.

Make sure that UserInfoDriver.java is in the edit window and that you have compiled it.  Now you are ready to follow the steps below to create a viewer canvas for Activty4A.

<ul>

 <li>On the desktop toolbar, click the Run in Canvas button . This launches the program in the debugger, stops at the first executable statement, and opens an empty canvas window (since a canvas has not yet been created for program) as shown below.</li>

</ul>







<strong>Running UserInfoDriver in the canvas and stopped at the first executable statement </strong>

<ul>

 <li>Click the Step button on the canvas window or debug tab. This creates an instance of UserInfo and assigns it to the variable <em>user1</em>.  You should see <em>user1</em> in the Variables tab of the Debug pane.</li>

</ul>




<ul>

 <li>Drag <em>user1</em> from the Debug tab onto the canvas; a default viewer should open for <em>user1</em> as shown below.</li>

</ul>







<strong>After user1 has been dragged onto the canvas </strong>




<ul>

 <li>Click the Step button on the canvas window or debug tab to execute next statement in UserInfoDriver. When a method is invoked on user1, you should see the respective field updated on the canvas.</li>

</ul>




<ul>

 <li>Keep stepping until you have created the second instance of UserInfo and assigned it to the variable <em>user2</em>. Now drag <em>user2</em> onto the canvas and position it to the right of <em>user1</em>.  Your canvas should look similar to the one below.</li>

</ul>







<strong>Canvas with user1 and user2 </strong>




<ul>

 <li>Save the canvas by clicking the Save button on the canvas window.</li>

</ul>




<ul>

 <li>Now click the Step button until the program ends. After the last step in the program, you should see a status message at the bottom the canvas indicating that the run in canvas has ended.  If you step one more time, the objects will be grayed out.  At this time, the viewers on the canvas should be grayed out to indicate that the objects no longer exist.  Now close the canvas window by clicking the close button on the upper left corner.</li>

</ul>




<ul>

 <li>On the desktop toolbar, click the Run in Canvas button . This launches the program in the debugger, stops at the first executable statement, and opens the canvas window that you created above.  Now step  through the program as you did above and observe the changes in the objects and the output of program.  After the last step in the program, you should see a status message at the bottom the canvas indicating that the run in canvas has ended.  If you step one more time, the objects will be grayed out as before.</li>

</ul>




<ul>

 <li>Now you are going to “play” your program. On the desktop toolbar, click the Run in Canvas button .  This launches the program in the debugger, stops at the first executable statement, and opens the canvas window that you created above.</li>

</ul>




On the canvas, click the Play button  (auto step-in) on the canvas to start the visualization.  Use the Pause button  and Stop button           as needed.  To regulate the speed of the program, decrease or increase the delay between steps using the Delay slider.




<h1><strong> of 10    </strong></h1>




When you play  your program, you will be stepping into each of your methods.  If it is going too fast for you to see and understand what is happening at each step, then increase the delay between steps by using the Delay slider.    You can also click the Pause button .




After you pause  your program, you can step  as you did above.  Or if you want to step into a method at a statement that calls the method then you can click the Step-in button .




You can also set one or more <strong>breakpoints</strong> (right-click on the line and select <em>Toggle Breakpoint</em>) in any of your methods and then Resume  to the next breakpoint.  The debugger will stop at the breakpoint, and you can examine the variables in the Debug tab or on the canvas.  You can then step , step-in    , or play             your program as needed.




You can always stop       (or end) the program, and then start it again by clicking the Run in Canvas button  followed by the Play button .




It is important that you understand what your program is doing at each step.  Although you can observe the behavior of your program using the debugger alone, the canvas works with the debugger to provide a more conceptual visualization of your program.  When you are studying the example programs provided with the class notes, you are encouraged to run these in canvas mode.  After you have added the variables of interest to your canvas and saved the canvas, you should be able to play or step through the program to understand the details of its behavior.  Until are able to understand the example programs, it will be difficult for you to write your own programs for the project assignments.

For the UserInfoDriver program above, you wrote the entire program before you created the canvas for it.  However, you could have created the canvas as soon as you were able to compile and run part of the program.  As you write you own programs for the project assignments, you can create a canvas as soon as there is any observable behavior.  This will help you ensure that the program is correct at each increment during development.  The canvas will be particularly useful when you are attempting to discover and correct errors in your program.

Note that you can also use the canvas via the Debug or Workbench tabs by clicking the Open New Viewer Canvas  button on the debug or workbench toolbar and then dragging one or more variables onto the canvas.  Changes to these variables resulting from statements executing in the Interactions tab, from stepping the debugger, and/or from executing methods via the Invoke Method dialog will be reflected on the canvas.

Usually, you will need only one canvas for your program.  However, if you need more than one, you can open a new canvas window via the Debug tab drag variables onto it and save it as described above.