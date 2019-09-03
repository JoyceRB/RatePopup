# RatePopup

Component to rate/give feedbak. It is made with Swift language. Just need to download RatePopup.swift and RateApp.xib and set them into your project.

![Captura de pantalla 2019-09-03 a las 15 11 14](https://user-images.githubusercontent.com/16594147/64181466-651a9780-ce5e-11e9-8c11-5dd26f048435.png)
![Captura de pantalla 2019-09-03 a las 15 11 18](https://user-images.githubusercontent.com/16594147/64181468-65b32e00-ce5e-11e9-8168-28466dec028b.png)

# USAGE

<h3>First steps:</h3>

* Import RateApp on my ViewController:
```Objective-C
import "RateApp.h"
```

* Reference RateAppDelegate on my ViewController:
```Objective-C
@interface MyController : ViewController <RateAppDelegate>
```

* Instantiate RateApp:
```Objective-C
RateApp *rateApp = [[RateApp alloc] init];
```

* Set delegate:
```Objective-C
rateApp.rateAppDelegate = self;
```

* Present RateApp on my ViewController:
```Objective-C
[self presentViewController:rateApp animated:NO completion:nil];
```

### Elements configurations:

* Set message:
```Objective-C
rateApp.message = @"Message you want";
```

* Set message color:
```Objective-C
rateApp.messageColorText = [UIColor blueColor];
```

* Set more details textfield placeholder:
```Objective-C
rateApp.moreDetailsPlaceHolder = @"Add more details";
```

* If you want to change title of buttons:
```Objective-C
rateApp.okButtonTitle = @"TITLE";
rateApp.cancelButtonTitle = @"TITLE";
```

* If you want to change color of text of buttons:
```Objective-C
rateApp.okButtonColor = [UIColor greenColor];
rateApp.cancelButtonColor = [UIColor greenColor];
```

* If you want to change color of stars:
```Objective-C
rateApp.starsColor = [UIColor redColor];
```

* Function to call when click on OK Button. You need to set it on your ViewController:
```Objective-C
(void)onClickRateAppOK:(NSInteger) score {
    //Do whatever you want when you click on OK button. Score is how many stars user set as score
    NSLog(@"Score: %ld", score);
}
```

* Function to call when click on CANCEL button. You need to set it on your ViewController:
```Objective-C
(void)onClickRateAppCancel {
    //Do whatever you want when you click on Cancel button.
}

