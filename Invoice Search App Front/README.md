# Invoice Search React App
English version of README.md is on [here](./README_EN.md)  
<img src="src/assets/img/Invoice%20Search%20App-logo.png" width="50%">  

## 本ディレクトリの目的
本ディレクトリは、インボイス番号の単一検索、複数検索、およびCSVファイルアップロードでのインボイス番号の整合性確認を可能とするReactアプリです。  
なお、本ディレクトリはAzure App Serviceへのデプロイ専用に記載しています。

## 環境変数
| カテゴリ         | キー                | 値                     | 
| ---------------- | ------------------- | ---------------------- | 
| .env.development | `VITE_APP_API_URL` | http://localhost:8000/ | 
| .env.production  | `VITE_APP_API_URL` | Fast APIのURL          | 

## 使用方法
### 単一検索、複数検索モード
1. 検索したいインボイス番号をテキスト入力欄に入力し、「検索」ボタンを押下してください。
2. テーブルに結果が表示されるので、不要なものがあれば「データ削除」ボタンを押下し、問題なければ「ダウンロード」ボタンを押下してください。

### 整合性検索モード
1. 確認したいインボイス番号が記載されたCSVをアップロードし、「検証」ボタンを押下。
2. CSVファイルの会社名・住所とAPI検索の結果に相違がある場合はテーブル内の「元データとの整合性」列に✕印が表示されます。API検索の結果にマージする場合は「マージ」列のマージアイコンを押下しマージしてください。

## 注意点
### CSVファイルアップロード時の注意点
CSVファイルアップロード時には、1行目にヘッダー、2行目以降にデータを記載してください。また、ヘッダー列は左から「インボイス番号、会社名、住所」にしていただき、それ以外の列は削除ください。

## ライセンス
MIT  
Copyright (c) 2023-2024 Lotus
