# First Install Eclipse/Sloeber/Doxygen 

 [See Eclipse install instructions in InstallEclipse.md](https://github.com/WPIRoboticsEngineering/RobotInterfaceBoard/blob/master/InstallEclipse.md)

# Set up an eclipse project

In eclipse, open 
```
Window->Show View-> Other -> Git ->Git Repositories
```
![alt text](/docs/GitRepositories.png)

In the browser, Click the clone or download button in your new project and select clone (Be sure HTTPS not SSH is selected, unless you have set up your SSH keys).

 ![alt text](/docs/cloneFromGithub.png)

Copy the clone URL.

In Eclipse, click the clone button: 

 ![alt text](/docs/cloneNewRepo.png)

If your URL is still copied in the clip board, Eclipse will autofill most the clone information for the first step. Add your username and password.

 ![alt text](/docs/startCloning.png)

Hit next and get to the Branch Selection window, change nothing and hit next.

Use the default checkout location. 

Hit Finish

## Open your project and start working

In Eclipse, Right click in the Project View and select 
```
New->Arduino Sketch
```

 ![alt text](/docs/chreateNewSketch.png)

Un-check the default location, and seclect where you just cloned your code. Mine looks like: 

```
R:\RBE\gitRbe\RBE2001Code20
```

Give it the name:

```
RBE2001Code20
```
![alt text](/docs/NewArduinoSketch1.png)

![alt text](/docs/NewArduinoSketch2.png)

Hit next then select the ESP32 toolchain. 

![alt text](/docs/setESPConfigs.png)

```
Board: ESP32 Dev Module
Upload Protocol: Default
Port (the port your device is on)
Core Debug Level: None
Flash Frequency 80mhz
Flash Mode: QIO
Flash Size: 4mb
Partition Scheme: Default
PSRAM: Disabled
Upload Speed: 921600
```



Then hit next and select Default ino file

![alt text](/docs/defaultINO.png)

Hit finish. 

Once the project shows up in Project Explorer tab, build index:

![alt text](/docs/rebuildIndexToAddLibs.png)


# Commit your changes

### Unfamiliar with Git?

run through this tutorial: https://resources.github.com/videos/github-best-practices/

Also check out this cheat sheet: http://overapi.com/git

### Familiar with Git?
When you make a change to any line of code, you should commit your changes. If you have worked for ~1 hour, then you should make a commit with a message describing your work. To do so, go back to 

Finally right click on your project
```
Team->Commit
```
Be sure to set the "Author" and "Committer" fields sould both contain the same data like this:
```
Kevin Harrington <harrington@wpi.edu>
```

Messages should consist of 60 charrectors of short description describing what changed, 2 new lines, then a t least one full sentance describing the justification for the change. If you have more than one file, only commit one at a time. using the "+" and "-" buttons in the Git Staging section. 

When you have chages to share with your team, first Right click on the repository and select "Pull". Merge any changes your team mates made and published to upstream. Then commit the merge (or commit nothing if the merge was clean) and push your changes to the upstream server.

Once you have pushed your changes, be sure to verify that they are on the GitHub.com website in Firefox. On your repository, go to
```
Insights->Network
```
and verify your changes are there. 



# Troubleshooting

## arduinoPlugin\tools\make\make not found in PATH

There can be a currupted download to the Make tools, if this error comes up follow these instructions to correct it
Follow the instructions here : https://github.com/Sloeber/arduino-eclipse-plugin/issues/767



