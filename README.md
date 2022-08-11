# Siv3DTemplate

Linux版OpenSiv3Dのプロジェクトテンプレート

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
