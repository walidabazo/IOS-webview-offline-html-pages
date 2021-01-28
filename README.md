# IOS-webview-offline-html-pages
IOS xcode webview offline html pages 

     import UIKit
     import WebKit

    class ViewController: UIViewController {

    @IBOutlet var webviews: WKWebView!
    override func viewDidLoad() {
        super.viewDidLoad()
        // Do any additional setup after loading the view.
        let url = Bundle.main.url(forResource: "index", withExtension: "html", subdirectory: "Lecoxenweb")!
        webviews.loadFileURL(url, allowingReadAccessTo: url)
        let request = URLRequest(url: url)
      webviews.load(request)
        
    }
    }


