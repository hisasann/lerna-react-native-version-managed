# lerna-react-native-version-managed

`monorepo` 環境における **package** と **react-native アプリ** のバージョンアップの考察

```bash
$ lerna init
$ yarn
```

```bash
$ lerna create package-node
```

```bash
$ cd packages
$ npx react-native init PackageReactNative
```

```bash
$ lerna add react-native-version --scope=PackageReactNative --dev
```

```bash
$ react-native-version
```

**react-native-version** は package.json の **version** を元に react-native のバージョン管理している箇所を書き換えてくれる npm モジュールです。

[stovmascript/react-native-version: :1234: Version your React Native or Expo app in a `npm version` fashion.](https://github.com/stovmascript/react-native-version)

つまり、順番としては、 lerna version で各 package のバージョンアップを行い、その後に **react-native-version** で react-nativeのバージョンアップを行えば、キレイにバージョンが揃うという寸法。
