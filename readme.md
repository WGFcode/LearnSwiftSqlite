
#学习swiftSqlite库

使用carthage安装库 
1.cd 工程目录
2.touch Cartfile  创建Cartfile文件
3.open -a Xcode Cartfile  打开Cartfile文件   添加github "stephencelis/SQLite.swift" ~> 0.11.5
4.carthage update --platform iOS
5.点击”项目名称”–> “TARGETS” –> “General”，在最底部找到 “Linked Frameworks and Libraries” 点击 + 号，选择左下角 Add Other… 按钮，选择项目下 Carthage/Build/iOS/Alamofire.framework 文件，点击 Open 加入到项目中
6.下一步选择菜单上的 Build Phases，点击左上角 + 号添加一个新的 Run Script，并添加以下命令：  /usr/local/bin/carthage copy-frameworks
7.点击 Input Files 下面的 + 号为每一个 framework 添加访问路径
carthage copy-frameworks 命令剔除了额外的框架
$(SRCROOT)/Carthage/Build/iOS/SQLite.framework


