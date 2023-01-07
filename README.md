# storyboard-less
Creating an Xcode project without a storyboard

I never liked to use Xcode Interface Builder. It is a great tool for learning and I am sure a lot of developers find it an excellent tool to build their APPS. 

This is just my personal choice. I like to believe that I control, as much as possible, what my code is doing (the reality has many different points of view).

Not following Apple path of using Storyboards might have some undesired consequences. However, not even one of the APPS that I have put on the APP store has used Storyboards (and I did work on some complex ones), so this is not a hard limitation.

Do not follow these steps on an existing Xcode project. Use them only when creating a blank project from scratch.

This guide was updated to Xcode Version 14.2.

- Create a new iOS APP Project

<img alt="Create a new Project" src="Image-Assets/new-project.jpg" width="729">

<img alt="Create a new iOS Projet Step 2" src="Image-Assets/new-project-step-2.jpg" width="729">

- Delete Main.storyboard file

<img alt="Delete Main Storyboard" src="Image-Assets/delete-main-storyboard.jpg" width="300">

- Delete Storyboard name from Info.plist

<img alt="Delete Storyboard name from Info.plist" src="Image-Assets/delete-story-board-name.jpg" width="1100">

- Delete Storyboard name from Target -> Info

<img alt="Delete Storyboard name from target" src="Image-Assets/delete-story-board-name-from-target.jpg" width="1100">

We should be ready and free to start our little APP how we desire.

First let's just have the ViewController do something so that we know that we were successful

We will change the background color by editing ViewController.swift

```
    override func viewDidLoad() {
        super.viewDidLoad()
        // Do any additional setup after loading the view.
        
        view.backgroundColor = UIColor.yellow
    }
```

Next we need to create and show our ViewController.

We do this by modifying the SceneDelegate file

```
    func scene(_ scene: UIScene, willConnectTo session: UISceneSession, options connectionOptions: UIScene.ConnectionOptions) {
        // Use this method to optionally configure and attach the UIWindow `window` to the provided UIWindowScene `scene`.
        // If using a storyboard, the `window` property will automatically be initialized and attached to the scene.
        // This delegate does not imply the connecting scene or session are new (see `application:configurationForConnectingSceneSession` instead).
        
        guard let windowScene = (scene as? UIWindowScene) else { return }
              
        window = UIWindow(windowScene: windowScene)
        window?.rootViewController = ViewController() // Your initial view controller.
        window?.makeKeyAndVisible()

    }
```

We can now run our APP and view the Yellow color of success:

<img alt="iPhone image with full screen in yellow" src="Image-Assets/success.jpg" width="300">

Free as a bird!
