var type: String?
        switch(btn.tag){
        case 1:
            //twitter
            type = Social.SLServiceTypeTwitter
        case 2:
            //fb
            type = Social.SLServiceTypeFacebook
        case 3:
            //sinaweibo
            type = Social.SLServiceTypeSinaWeibo
        case 4:
            //tencentWeibo
            type = Social.SLServiceTypeTencentWeibo
        default:
            type = nil
        }
        if let _ = type {
            if SLComposeViewController.isAvailableForServiceType(type) {
                let cvv = SLComposeViewController(forServiceType: type)
                cvv.setInitialText("设置你要分享的内容")
                
                cvv.addURL(NSURL(string: "https://www.apple.com"))
                cvv.completionHandler = { (result: SLComposeViewControllerResult) -> Void in
                    if result == SLComposeViewControllerResult.Cancelled {
                        NSLog("取消发送")
                    }else {
                        NSLog("发送完毕")
                    }
                }
                presentViewController(cvv, animated: true, completion: { () -> Void in
                    NSLog("presentViewController completion")
                })
            }
        }else {
            
        }
