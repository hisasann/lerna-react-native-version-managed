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

[stovmascript/react-native-version: :1234: Version your React Native or Expo app in a `npm version` fashion.](https://github.com/stovmascript/react-native-version)
