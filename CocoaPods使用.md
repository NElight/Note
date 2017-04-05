## CocoaPods使用
1. `cd /usr/projectDic`进入项目目录
2. 创建Podfile文件，文件内容格式：  

    ```
        platform :ios,'7.0'
        target "targetName"do

        pod 'AFNetworking', '~> 3.1.0'
        pod 'SDWebImage', '~> 3.8.1'
        pod 'Masonry', '~> 1.0.1'
        pod 'JSONModel', '~> 1.3.0'
        pod 'SVProgressHUD', '~> 2.0.3'
        pod 'MJRefresh', '~> 3.1.12'

        end
    ```  
3. `pod install`将项目交由CocoaPods托管。
4. `pod search mjrefresh`查找三方库