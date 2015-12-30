## APK packaging env

- JAVA_VERSION 8
- GRADLE_VERSION 2.2.1
- ANDROID_SDK_VERSION r24.4.1
- ANDROID_M2REPOSITORY_VERSION r25
- ANDROID_SUPPORT_VERSION r23.1.1
- ANDROID_PLATFORM_VERSION 22_r02
- ANDROID_BUILD_TOOLS_VERSION r23.0.2

## How to use
`sudo docker run -v /project/path:/app lhcpig/android`

If you don't want to download the dependency everytime, you can use the command:
`sudo docker run -v ~/.gradle:/root/.gradle -v /project/path:/app lhcpig/android`
so you can cache it in the path `~/.gradle`.
