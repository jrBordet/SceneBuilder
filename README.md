# SceneBuilder

## Installation - CocoaPods

```
 source "https://github.com/jrBordet/RxFramework.podspec.git"
 source "https://cdn.cocoapods.org/"
 
 pod 'SceneBuilder', '1.0.0'
 ```

## Usage

```swift
import SceneBuilder

@UIApplicationMain
class AppDelegate: UIResponder, UIApplicationDelegate {
    var window: UIWindow?
    
    func application(_ application: UIApplication, didFinishLaunchingWithOptions launchOptions: [UIApplication.LaunchOptionsKey: Any]?) -> Bool {
        // Override point for customization after application launch.
        
        self.window = UIWindow(frame: UIScreen.main.bounds)
                
        let rootScene =
            Scene<ViewController>()
                .render()
                    
        self.window?.rootViewController = UINavigationController(rootViewController: rootScene)
        
        self.window?.makeKeyAndVisible()
        self.window?.backgroundColor = .white
        
        return true
    }
}
```
