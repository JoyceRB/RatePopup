# RatePopup

Component to rate/give feedbak. It is made with Swift language. Just need to download RatePopup.swift and RateApp.xib and set them into your project.

![Captura de pantalla 2019-09-03 a las 15 11 14](https://user-images.githubusercontent.com/16594147/64181466-651a9780-ce5e-11e9-8c11-5dd26f048435.png)
![Captura de pantalla 2019-09-03 a las 15 11 18](https://user-images.githubusercontent.com/16594147/64181468-65b32e00-ce5e-11e9-8168-28466dec028b.png)

# USAGE

<h3>First steps:</h3>

* Import RatePopup on your ViewController:
First you need to create a Bridge header file and then import it into your ViewController. Example:
```Objective-C
import "BridgeHeader-Swift.h"
```

* Reference RatePopupDelegate on ViewController:

Objective-C:
```Objective-C
@interface MyController : ViewController <RateAppDelegate>
```

Swift:
```Swift
class MyViewController: UIViewController, RatePopupDelegate {
```

* Instantiate RatePopup:

Objective-C:
```Objective-C
RatePopup *ratePopup = [[RatePopup alloc] init];
```

Swift:
```Swift
let ratePopup = RatePopup()
```

* Set delegate:
```Objective-C
ratePopup.ratePopupDelegate = self
```

* Present RateApp on my ViewController:

Objective-C:
```Objective-C
[self presentViewController:ratePopup animated:NO completion:nil];
```

Swift:
```Swift
self.present(ratePopup, animated: false, completion: nil)
```

### Elements configurations:

* Set message:
Objective-C:
```Objective-C
[ratePopup setMessage:@"Message you want"];
```

Swift:
```Swift
ratePopup.setMessage("How do you value our service?")
```

* Set message color:
Objective-C:
```Objective-C
[ratePopup setMessageColorText:[UIColor blueColor]];
```

Swift:
```Swift
ratePopup.setMessageColorText(UIColor.green)
```

* Set more details textfield placeholder:
Objective-C:
```Objective-C
[ratePopup setMoreDetailsPlaceHolder:@"Add more details"];
```

Swift:
```Swift
ratePopup.setMoreDetailsPlaceHolder("Add more details")
```

* If you want to change title of buttons:
Objective-C:
```Objective-C
[ratePopup setOkButtonTitle:@"Ok title"];
[ratePopup setCancelButtonTitle:@"Cancel title"];
```

Swift:
```Swift
ratePopup.setOkButtonTitle("Ok Title")
ratePopup.setCancelButtonTitle("Cancel Title")
```

* If you want to change color of text of buttons:
Objective-C:
```Objective-C
[ratePopup setOkButtonTitleColor:[UIColor greenColor]];
[ratePopup setCancelButtonTitleColor:[UIColor greenColor]];
```

Swift:
```Swift
ratePopup.setOkButtonTitleColor(UIColor.green)
ratePopup.setCancelButtonTitleColor(UIColor.green)
```

* If you want to change color of stars:
Objective-C:
```Objective-C
[ratePopup setStarsColor:[UIColor redColor]];
```

Swift:
```Swift
ratePopup.setStarsColor(UIColor.green)
```

* Function to call when click on OK Button. You need to set it on your ViewController:
Objective-C:
```Objective-C
- (void)onClickRatePopupOKWithScore:(NSInteger)score comments:(NSString *)comments {
	//Do whatever you want when you click on OK button. Score is how many stars user sets as score and comment is what user	sets on "More Details" TextField:
    NSLog(@"Score: %ld", score);
}
```

Swift:
```Swift
func onClickRatePopupOK(score: Int, comments: String) {
 	//Do whatever you want when you click on OK button. Score is how many stars user sets as score and comment is what user	sets on "More Details" TextField:
    }
```

* Function to call when click on CANCEL button. You need to set it on your ViewController:
Objective-C:
```Objective-C
(void)onClickRateAppCancel {
    //Do whatever you want when you click on Cancel button.
}
```

Swift:
```Swift
func onClickRatePopupCancel() {
	//Do whatever you want when you click on Cancel button.
}
```


