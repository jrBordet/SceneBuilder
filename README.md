# SceneBuilder

## Installation - CocoaPods

 
 ```ruby
source 'https://github.com/jrBordet/Sources.git'
source 'https://cdn.cocoapods.org/'

target 'Target' do

 pod 'SceneBuilder', '1.0.0'

end


## Usage

```swift
import SceneBuilder

@UIApplicationMain
class AppDelegate: UIResponder, UIApplicationDelegate {
    var window: UIWindow?
    
    func application(_ application: UIApplication, didFinishLaunchingWithOptions launchOptions: [UIApplication.LaunchOptionsKey: Any]?) -> Bool {
        // Override point for customization after application launch.
        
        self.window = UIWindow(frame: UIScreen.main.bounds)
                
        let rootScene = Scene<ViewController>().render()
                    
        self.window?.rootViewController = UINavigationController(rootViewController: rootScene)
        
        self.window?.makeKeyAndVisible()
        self.window?.backgroundColor = .white
        
        return true
    }
}
```
