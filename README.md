GAME ANALYSIS
Initialization: Pins are initialized for input and output. The LCD screen and the speaker are initialized.
1.	Main Menu Display: The main menu is displayed on the LCD, and the user can select a difficulty level by pressing the corresponding buttons.
2.	Button Feedback: When a difficulty level is selected, a tone is played, the selected push button lights up briefly, and the selected difficulty level is briefly displayed on the LCD screen.
3.	Game Start: After selecting a difficulty level, the game begins. A message indicating the start of the game is displayed on the LCD screen.
4.	Game Generation: A random sequence of tones is generated based on the selected difficulty level.
5.	Game Progression: The Arduino plays the generated sequence of tones, and the player is prompted to repeat the sequence. If the player repeats the sequence correctly, the game continues; otherwise, the game ends.
6.	End of Game Approach: If the player loses, they are given the option to play again. If the player wins, their final score is calculated based on the number of completed rounds and any bonus points based on the difficulty level. The final score is displayed on the LCD screen.
7.	Main Menu Restart: After displaying the end of game message, the main menu is displayed again so the player can start a new game.

Hardware Requirements:
1.	Arduino Uno board (No Due or other boards!)
2.	Adafruit RGB LCD Shield (16x2 I2C)
3.	Push buttons with built-in LEDs (4 pieces)
4.	Resistors (e.g., 220 ohms) for the LEDs
5.	Active buzzer (piezoelectric speaker)
6.	Breadboard (optional)
7.	Jumper wires

Connections:
1.	Adafruit RGB LCD Shield: • Connect the Adafruit RGB LCD Shield to the Arduino Uno as indicated in the Adafruit documentation.
2.	Push Buttons with LEDs: • Connect each push button to a digital pin of the Arduino Uno (e.g., pins 6, 7, 8, and 9). • Connect the LED legs of the push buttons to the GND of the Arduino via resistors (e.g., 220 ohms). • Connect the other leg of each LED to the digital pin used for LED control.
3.	Piezoelectric Speaker: • Connect the positive side of the buzzer to a digital pin of the Arduino (e.g., pin 11). • Connect the negative side of the buzzer to the GND of the Arduino.
4.	Optional Steps: • If using the push buttons and LEDs on a breadboard, first connect the push buttons and resistors to the breadboard and then connect the wires to the Arduino. • Use jumper wires to make connections between the components according to the above instructions. Ensure to connect the components carefully to prevent damage. Also, check if the pins of the LCD Shield are correctly aligned with the pins of the Arduino. Once everything is properly connected, you can upload the code to the Arduino and start the game. Have fun playing!
5.	Adafruit RGB LCD Shield: • The code utilizes the Adafruit_RGBLCDShield library, indicating that the LCD is controlled via the I2C interface. • There is no explicit wiring in the code for the LCD since it's connected to the I2C interface of the Arduino via the shield. This significantly simplifies the wiring.
6.	Push Buttons with LEDs: • Four push buttons with LEDs are used for the game. • The push buttons are activated when pressed and may also include LEDs that light up to provide feedback. • In the initializePins() function, the pins are initialized for the push buttons (input) and the LEDs (output). • The push buttons are connected to digital pins 6, 7, 8, and 9 of the Arduino, as specified in the showMainMenu() function where the buttons are read. • The LEDs of the push buttons are connected to the digital pins and are controlled to provide feedback to the user in the buttonFeedback() function.
7.	Piezoelectric Speaker: • An active buzzer (piezoelectric speaker) is used to play tones. • The buzzer is connected to digital pin 11 of the Arduino, as indicated in the playNotes() function. • By sending different frequencies to the buzzer, different tones are generated to indicate the game progression. The code provides a clear insight into how the hardware components are used and connected. Utilizing the Adafruit RGB LCD Shield simplifies the wiring for the LCD screen, while the push buttons and LEDs are directly connected to the Arduino to enable user interaction. The piezoelectric speaker is used for auditory feedback during the game.

