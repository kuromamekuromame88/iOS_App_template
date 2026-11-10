# iOS_App_template

## 説明
このリポジトリは、iOSのアプリをgithubActionsで未署名の.ipaに変換するときの例のリポジトリです。
.github/workflows/build.ymlがビルドのプログラムです。動作は未検証です。

以下のようなフォルダ構造の場合を想定したビルドスクリプトです。

```
repository_root/
├── .github/worklows/build.yml
├── VRtest/
│   └── Unity-iPhone.xcodeproj/
├── AnotherProject/
│   └── GameProject.xcodeproj/
└── README.md
```

リポジトリのルートに.githubのフォルダと、Xcodeプロジェクトのフォルダをそのまま置くことで、ビルド時に自動で認識されるはずです。
複数の.xcodeprojが見つかった場合には、最初に見つかったほうが優先されます。
