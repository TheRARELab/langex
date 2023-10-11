# Langex

A generalized Choregraphe project for reproducible **lang**uage-based HRI **ex**periments.

## License

This software is licensed under [MIT licence](LICENSE):

| Permissions                                                               | Limitations                 | Conditions                   |
|---------------------------------------------------------------------------|-----------------------------|------------------------------|
|  ✅ Commercial use<br> ✅ Modification<br> ✅ Distribution<br> ✅ Private use |  ❌ Liability<br> ❌ Warranty | License and copyright notice |

The project (anonymized) that is generalized is also under MIT licence: [anonymized].

## System requirements
 - All software dependencies and operating systems (including version numbers).
    - Choreograph 2.5
    - Ubuntu 14.04+/Windows 7+/macOS 10.11+
 - Versions the software has been tested on.
    - Choreograph 2.5
    - Windows 10 and Ubuntu 20.04
 - Any required non-standard hardware [including specific makes and models for robotic platforms].
    - [NAO](https://www.aldebaran.com/en/nao) or [Pepper](https://www.aldebaran.com/en/pepper) by Aldebaran Robotics

## Installation guide
 - [Download Choreograph 2.5](https://www.aldebaran.com/en/support/pepper-naoqi-2-9/downloads-softwares) ([Windows](https://community-static.aldebaran.com/resources/2.5.10/Choregraphe/choregraphe-suite-2.5.10.7-win32-setup.exe), [macOS](https://community-static.aldebaran.com/resources/2.5.10/Choregraphe/choregraphe-suite-2.5.10.7-mac64-setup.dmg), [Linux](https://community-static.aldebaran.com/resources/2.5.10/Choregraphe/choregraphe-suite-2.5.10.7-linux64-setup.run))
 - Install Choreograph 2.5 by following the [official installation guide](http://doc.aldebaran.com/2-5/software/choregraphe/installing.html)
   - Licence key: 654e-4564-153c-6518-2f44-7562-206e-4c60-5f47-5f45

For people who are not familier with Choreograph, [this guide](http://doc.aldebaran.com/2-5/getting_started/creating_applications/index.html) should be good enough to get you started.

## Demo
 - Instructions for the demo of the code.
   - Open the project in the [`generalized-experiment`](generalized-experiment) folder by clicking on `generalized-experiment.pml`
   - Open the dialog panel from the View menu.
   - Run the project based on the instructions for running the [hello-world project](http://doc.aldebaran.com/2-5/getting_started/helloworld_choregraphe.html).
     - First run the behavior in the `initialize_post` folder
     - Then run the behavior in the `experiment_behavior` folder
   - As you run the program, type `next` or `n` in the dialog panel to make the robot speak the next utterance
 - Expected output.
   - The robot should behave and speak exactly the same as this video: https://www.youtube.com/shorts/5plLXZN3D0E

## Instructions for use
 - Open the project in the [`generalized-experiment`](generalized-experiment) folder by clicking on `generalized-experiment.pml`.
 - The current project is named “general-experiment” and it should be changed in the property of the project and editing the “manifest.xml” file.
 - The “Factor 1” and “Factor 2” nodes should be changed both in their name and the list content.
   - If there are more than three factors, the “Factor 2” and “Append Factor 2” should be duplicated to ensure the third factor appears in the log filename, log header, and log rows.
 - The dialog content needs to be placed in the “utterances” directory at the project root. Each condition should have a dialog file named “factor1-factor2-factor3.txt”
 - To specify where the log directory is, simply change the content of the “Log directory” node
 - For start and end phrases, they can also be changed in the two text box nodes with the same names
 - One last change is the robot’s initial behavior, which can be found in the “initialize_pose” folder.
   - To change the robot’s pose, e.g., to look at the table in front of it, after it speaks the start phase, the node “See Table” (See mid-left of Figure 1) can be used for this purpose by changing its parameters, the offset values (x,y,z) and the reference frame, e.g., torso.

## Maintenance and Contribution

Please use Issues for any questions and Pull Requests (PR) for contribution. We particularly welcome PR with adapted code with this project.

Maintainers:
 - anonymized, email
 - anonymized, email
