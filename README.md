使用这个来创建 iOS 各类证书和文件，能够将各类证书和文件提交到 gitlab 管理。  


## 使用

必须clone到本地，**不能直接下载**。  
```
git clone git@gitlab.kosun.net:iOS-Team/PushCerts.git
cd PushCerts
git checkout -b develop origin/develop
```

生成账号相关文件。  
```
fastlane shake username:'*****@****.com'
```

## 传参

| Key          | Optional | Meaning          |
| ------------ | -------- | ---------------- |
| `username`   | NO       | Apple ID         |
| `identifier` | YES      | Bundle ID        |
| `appname`    | YES      | App Store Name   |
| `language`   | YES      | Primary Language |

**用例**

```
fastlane shake username:'prefix@suffix.com' identifier:'com.prefix.*********' appname:'prefix' language:'English'
```

## Bundle ID 命名规则

上线管理后台的**唯一 ID** 指的便是 **Bundle ID**

例如 Apple ID 为

```
prefix@suffix.com
```

则 Bundle ID 命名为

```
com.prefix.*********
```
