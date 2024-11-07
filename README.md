Overview

The Brute Force Simulator is a simple Java application that demonstrates a brute force attack for password guessing. It generates possible password combinations and tests them against a predefined target password.



Features:

- Simulates password guessing using brute force.

- Includes a delay between attempts to mimic real-world conditions.

- Logs each password attempt for transparency.

- Customizable character set and password length.



How to Run

Prerequisites:

- Java Development Kit (JDK) 8 or higher.

- An IDE or command-line environment.

Compilation:

bash

Copy code
javac BruteForceSimulator.java

Execution:

bash

Copy code
java BruteForceSimulator

Code Explanation:

- The bruteForce method recursively generates and tests passwords.

- attemptPassword attempts to match the generated password with the target.

- TimeUnit.MILLISECONDS.sleep(100) simulates a delay between attempts.

Customization:

- Change the PASSWORD variable to modify the target password.

- Adjust maxLength and charset to expand the search space.

Limitations:

- Not optimized for long passwords or large character sets.

- Performance may decrease significantly with increased password length.
