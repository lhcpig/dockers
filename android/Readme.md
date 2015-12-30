This docker is to build Android Gradle project with Java 8.

---
# 1. Version
- Java 8
- Gradle 2.2.1
- Android_sdk r24.4.1
- Android_m2repository r25
- Android_support r23.1.1
- Android_platform 22_r02
- Android_build_tools r23.0.2

---
# 2. How to use

just use the command:
```bash
sudo docker run --rm -v /project/path:/app lhcpig/android
```

If you don't want to download the dependency everytime, you can use the command:
```bash
sudo docker run --rm -v ~/.gradle:/root/.gradle -v /project/path:/app lhcpig/android
```
so you can cache it in the path `~/.gradle`.
