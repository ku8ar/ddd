import UIKit
import React

class ReactViewController: UIViewController {
  override func viewDidLoad() {
    super.viewDidLoad()

    guard let jsBundleURL = Bundle.main.url(forResource: "main", withExtension: "jsbundle") else {
      fatalError("Brak main.jsbundle")
    }

    let rootView = RCTRootView(
      bundleURL: jsBundleURL,
      moduleName: "WCSOnboarding", // MUSI odpowiadać AppRegistry.registerComponent(...)
      initialProperties: nil,
      launchOptions: nil
    )

    rootView.frame = self.view.bounds
    self.view.addSubview(rootView)
  }
}
