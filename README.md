# ROS Android Sample App

公式のサンプルコードが Android Studio 4.0.1 ではなかなかビルドできなかったのでここに保存。

注意：
　ビルドを通しただけです。動作確認してません。


キモは build.gradle の
``` build.gradle
dependencies {
 ...
    implementation 'org.ros.android_core:android_15:[0.3,0.4)'
    implementation 'org.ros.rosjava_bootstrap:message_generation:[0.3, 0.4)'
    implementation 'org.ros.rosjava_core:rosjava_tutorial_pubsub:[0.2,0.3)'
    implementation 'org.ros.rosjava_messages:std_msgs:0.5.11'
}
```
ですね。
rosjava_bootstrap がないと org.ros.internal.message.Message が見つからないとエラーが出ます。
