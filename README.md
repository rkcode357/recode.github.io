# rkcode coding tutorials!
### these coding tutorials start with c++. I will add a python tutorial later but for now enjoy the tutorial!
## table of contents
### 1. Introduction
### 2. Setup
### 3. How to use the print function and coding basics
### 4. A note on functions 
### 5. Variables and adding
# introduction for c++
###  Welcome to the world of c++! a coding language used for game development, web development, and so much more! Any electronic computer has code, most of it being c++ so it is a great language to learn. Being brutally honest, c++ is a very hard language to learn for begginers but stick to it and TRUST ME you WILL get it! The most important takeway is don't get discouraged, every developer had to go through the stuff you have to get throught to get to an expert level. 
# setup 
## Before you setup! NOTES!
### this tutorial I will be using a tool called arduboy. An arduboy is an 8 bit game console that has a special coding library to assist in learning c++. If you don't have the physical arduboy that is ok we will show you the digital version and how you can use that to code! 
### Lets get your computer all of the tools it needs to make code and run it! First we are going to grab an app that is kind of like google docs that will let us write code. This app is called the arduino IDE and ide stands for an integrated development enviroment. This is an enviroment where you can develop code and work on your game projects. Lets go to the website you need to download arduino ide. This websites link is www.arduino.cc/en/software. After you get to the website go to download options, and then download the app according to what operating system you have e.x (Windows mac linux). Once you have the app downloaded open it up. Once opened you should see some code and a dark mode google docs like thing. This is an IDE. This is what master coders and game devs use to code :). (Not really but you get the point). Now that we have our development enviroment all set up we need an arduboy to run it. If you have the physical arduboy FX which you can buy here: https://www.arduboy.com that is great but if you don't want to spend 80 dollars to buy one you can use the digital website simulator to simulate the games. You can find that website here: https://tiberiusbrown.github.io/Ardens/ You will need to drag and drop the hex file of your game into this website to simulate it. We will show you how to do this later. One more thing to note is that Whenever I represent code in this tutorial I add a space between every line of code this is not how it works in the ide, Basically you don't need to do this when you are coding. Now you are ready to go to the first part of the tutorial, Basic coding and the print function!
# How to use the print function and coding basics
### The first thing we are going to learn how to do to our arduboy is make it say something this is called the print function. But before you do that I need to explain see something. When you open up a project in arduino ide you will see a void setup() {
### } 
### and a 
### void loop() {
### }
### the setup is where you add code that will only run once and the loop will run continously. The next thing I have to explain is comments, comments are little notes to yourself that the computer ignores it helps keep your code more clear, to comment you just type // and the your note so if I wanted to comment "Hi" to myself I would write: //hi. 
### Now there is still more to explain so bear with me! Something really important to remember is that all of the code commands you write NEED to go inside of the curly braces, these things: {} so if the code isn't INSIDE of those you will get a million errors and things. another thing is after almost every line of code you put a semicolan to tell the computer the code command has ended. like this; The last thing to do is explain what a library is, a library is a special code that you can install in the ide that lets you write code for certain computer hardware. If you are going to use the physical arduboy fx for this tutorial, then you will need to install the arduboy2 library in the arduino ide. Also if you are going to use the arduboy fx, I would learn first how to connect and upload code to the computer. There are many tutorials for this online. So basically if you do not want to go throught the whole process of uploading to the arduboy, just use the online simulator and you will be fine :). 
# print function
### now it is time to teach you the print function, In the arduino ide you will see this code: 

### void setup() {

### }

### void loop() {

### } 
### the first thing we need to do is include the arduboy2 library so before and above the setup function we will need to add: #include Arduboy2.h also put the "Arduboy2.h inside of these more than or less than symbols like this: < >. below that we will need to add: Arduboy2 arduboy; I won't explain this now because it is complicated but all you need to know is that this isn't important know. Next we need to tell the computer to start the game and to clear the screen kind of like painting a canvas white. to do this move into the void setup area and type arduboy.begin(); then below that type arduboy.clear(); Then move into the void loop section and type again arduboy.clear();. Now we are ready to rumble, we are now going to actually print a message to the screen so after the clear command in loop type arduboy.print("whatever you want to say"); you can add any message where I put the "whatever you want to say" message. Just be careful because if you keep typing on and on forever the screen will run out of space, it is only 128 pixels wide! So to stop this and go to the line below that, type arduboy.print("\n"); this will not print \n but it instead will go to a new line like when you press return on your keyboard. Now what if you want to put a message anywhere you want on the screen? Well then you will have to type arduboy.setCursor(0,0); the two zeros are coardinates on the screen. To put your cursor wherever you want 
### I would advise making a pixel art screen that is 128 pixels wide and 64 pixels tall so you can visually see where you want your letters to be. And finally when you are done coding add the command arduboy.display(); in the curly braces as the last thing in your void loop code to tell the computer to display it. Here is a full code that uses all of these features: 
 #include Arduboy2.h  // Remember these!!! <  > 
 
 Arduboy2 arduboy; 
 
 void setup() {
 
  arduboy.begin();
  
  //this is a comment!!!
  
  arduboy.clear();
  
 }

 void loop() {
 
  arduboy.setcursor(17,6);
  
  arduboy.print("h");
  
  arduboy.print("\n");
  
  arduboy.print("i");
  
  arduboy.display();
  
 }
### congratulations! you are done with the first lesson! 
# a note on functions
### So, what is a function? A function is a command that does something on the arduboy screen or in code altogether. For example some functions would be arduboy.print(""); and arduboy.clear(); these are functions and remember, they are always followed by a semicolan. Like this; Always remember that!
# variables and adding
### Math is a HUGE part of coding in any language. Using basic logic and mathematics, you can achieve almost anything in coding. So this lesson will be all about math and things like that. So our first thing we have to learn is varaibles, what I think is the most important element in a code. A variable is a string of letters and is usually a word. So Lets use how to use variables, you create a variable by after you add the Arduboy2 arduboy; element before void setup you will have to add: int variable name goes here so it would look like:
 #include <Arduboy2.h>
 
 Arduboy2 arduboy; 
 
 int int_stands_for_integer

 void setup(); {
 
   arduboy.begin();
   
   arduboy.clear();
   
   int_stands_for_integer = 1 
 }
 void loop(); {
 
   arduboy.clear();
   
 }
 ### in this code we declare the variable, int_stands_for_integer (it does) and notice how I gave it an initial value in the setup section. I gave the integer the value of one. So now we can add this variable do math with it. Now what if you want to add a bigger value to a variable? There is a command to do this. The command is:
 int_stands_for_integer = int_stands_for_integer + 1; 
 ### This line of code adds one to the variable int_stands_for_integer. This variable is now holding the value of 2. There is also a different way to do this you can re-declare the value of the variable to anything we want. If I wanted to declare the variable as the number 2, I would write: 
 int_stands_for_integer = 2; 
 ### this is a little bit shorter if you are using long variable names. 
