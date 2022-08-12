# Siv3DTemplate

Linux版OpenSiv3Dのプロジェクトテンプレート

## ファイル構造

```
Siv3DTemplate/
├── .idea: CLion設定
│   (参考: https://intellij-support.jetbrains.com/hc/en-us/articles/206544839-How-to-manage-projects-under-Version-Control-Systems)
│   └── ...
├── .vscode: VSCodeの設定
│   └── extensions.json: 推奨する拡張機能の設定
├── App
│   ├── example: サンプルファイル (削除可能)
│   │   └── ...
│   ├── resources: リソースファイル
│   │   (参考: https://zenn.dev/reputeless/books/siv3d-documentation/viewer/tutorial-resource)
│   │   └── engine
│   │       └── ...
│   ├── Siv3DTemplate: 実行可能ファイル(Releaseビルド)
│   └── Siv3DTemplate_Debug: 実行可能ファイル(Debugビルド)
├── CMakeLists.txt: CMakeプロジェクト設定
├── Main.cpp: ソースファイル
└── README.md: このファイル
```

## 必須環境

- **[OpenSiv3D](https://github.com/Siv3D/OpenSiv3D) v0.6.5** のCMakeパッケージのインストール
- CMake 3.12以上

## 検証済み環境

- Visual Studio Code
- CLion

## プロジェクト名の変更(推奨)

```bash
cd <Siv3DTemplateのディレクトリ>
NAME="<新しいプロジェクト名>"
rm -f App/Siv3DTemplate*
sed -i -e "s/Siv3DTemplate/${NAME}/g" .gitignore CMakeLists.txt
```
