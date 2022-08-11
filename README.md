# Siv3DTemplate

Linux版OpenSiv3Dのプロジェクトテンプレート

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
rm App/Siv3DTemplate*
sed -i -e "s/Siv3DTemplate/${NAME}/g" .gitignore CMakeLists.txt
```
