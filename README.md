# PassCrackGUI
*PassCrackGUI* is a graphical interface created to join some tools freely available on the Internet. The primary goal was to create a platform that can help people using some experts tools for passwords representation cracking (*i.e* hash functions). Understanding and execute tools Like *Hashcat*, *John The Ripper (JTR)* and *RainbowCrack* can be hard, and the time wasting written the commands can be exhausting. The *PassCrackGUI* has a friendly and smooth environment that can help people using the tools mentioned  before, without any preoccupation to write a thousand times the executing commands.

This interface hold the possibility of multiple different attacks. The different types of attacks available in the *PassCrackGUI* are already development in the tools *Hashcat*, *JTR* and *RainbowCrack*. **Dictionary Attack** and **Brute-Force** are the main algorithms that we can find in these two first tools. The *RainbowCrack* use a *time-memory tradeoff* algorithm (that uses a pre-computated data call **Rainbow Tables**) to crack hashes.

Towards these functions mentioned are some others that the users can resort. One available allow to create a dictionary, that combined all possible cases of conjugations to the chars previously chosen. Such functionality is provided thanks to the implementation of a tool int the *PassCrackGUI* call *Crunch*.

This graphical interface was created mainly to academic proportions, but can be an open mind for all users to see how week their passwords are nowadays and how easy is to crack them.

# User Manual and Working Example
The interface are build to allow the user a self discovered and self use of the *PassCrackGUI*. The main preoccupation was to make it easy to comprehend and intuitive. 

- The first thing the user has to choose while in the platform, is method to input the data, that can be in clean text, input a file with multiple passwords representations, or input a simple hash. The first allow the user the  option of choice on three different hash algorithms, SHA1, MD5 and SHA256.

- If on the first option the user will chose the hash type, on the other two option, the program as to know what kind of password representation was insert. So the next step is click on button *Verify Hash* to find a possible hash type. Once verified, the user will choose from a list what hash algorithm he want to use for crack (the choice of a wrong type can leave to no results, so if the user can't be sure what kind of hash is dealing with, the more safe proceed is choose all).

- Complete this steps above, its crucial pick at least one tool (*e.g* *Hashcat*, *JTR*, *RainbowCrack*). Inside of the first two tools, will be presented a button *Preferences*, that can be select the attack algorithm (*e.g* *dictionary attack*, *brute-force* or *default* a mixed attack used by *JTR*).

- After this, you most select a *dictionary* (if selected the *dictionary attack*) , a *Rainbow Table* (if chosen the *RainbowCrack*) or use Mask on brute-force attack. On dictionary attack is given the possibility of choice of *Replacement Tables*, that can replace some characters for others in a dictionary:
```
a for 4 will make the follow word be 
water -> w4ter
```
- To make an attempt to crack a password representation, after all obligatory fields are filled, click on the white arrow with green background (*Crack*).

An example of a result using the *PassCrackGUI* is illustrated below through a figure. Is a *dictionary attack* using the well known *RockYou* dictionary and the *Hashcat* tool. An attempt to crack a password representation SHA1 of *superman*.

#Requirements and Dependencies
This graphical interface was build in a *IDE NetBeans 7.0.4* and also needs a *IDE* to run. In order to avoid problems and some possible incompatibilities is recommended using the same *IDE* and the same or more recent version. Another requisite is having the JAVA on the computer. 

To run this application most be executed the file ```\toolkit\src\toolkit\Interface.java```, inside of the *IDE*.There has to be install also the tools used in the *PassCrackGUI*, like *Hashcat*, *JTR*, *Crunch* and *RainbowCrack*.
The interface has a size minimum of 0000x000 being crucial has a computer resolution in accordance. Any attempt to reduce the size of the application window could leave to visibility lost.
