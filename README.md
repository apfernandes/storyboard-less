# storyboard-less
Creating an Xcode project without a storyboard

I never liked to use Xcode Interface Builder. It is a great tool for learning and I am sure a lot of developers find it an excellent tool to build their APPS. 

This is just my personal choice. I like to (think) I control, as much as possible, what my code is doing (the reality is has many points of view).

Not following Apple path of using Storyboards might have some undesired consequences. However, not even one of the APPS that I have put on the APP store has used Storyboards (and I did work on some complex ones), so this not a hard limitation.

Do not follow these steps on and exiting Xcode project, use them only when creating a blank project from scratch.

This guide has been updated to Xcode Version 14.2.

- Create a new iOS APP Project

![Create a new iOS Projet](Image-Assets/new-project.jpg)

![Create a new iOS Projet Step 2](Image-Assets/new-project-step-2.jpg)

- Delete Main.storyboard file

![Delete Main Storyboard](Image-Assets/delete-main-storyboard.jpg)

- Delete Storyboard name from Info.plist

![Delete Storyboard name from Info.plist](Image-Assets/delete-story-board-name.jpg)

- Delete Storyboard name from Target -> Info

![Delete Storyboard name from target](Image-Assets/delete-story-board-name-from-target.jpg)
