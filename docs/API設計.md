# API設計

## ユーザー認証
POST   /api/auth/register　ユーザー登録  
POST   /api/auth/login　ログイン  
POST   /api/auth/logout　ログアウト  

## 作業概要
GET    /api/tasks　作業一覧の取得  
POST   /api/tasks　作業の新規登録  
PATCH  /api/tasks/{id}　作業概要の編集  
DELETE /api/tasks/{id}　作業の削除  

## 作業履歴
GET    /api/tasks/{id}　指定した作業の履歴一覧を取得  
GET    /api/tasks/{id}/work-logs/{id}　作業履歴の詳細取得  
POST   /api/tasks/{id}　指定した作業に履歴を追加  
PATCH  /api/tasks/{id}/work-logs/{id}　作業内容・作業時間などの編集  
DELETE /api/tasks/{id}　作業履歴の削除  

## 課題管理
GET    /api/tasks/{id}/work-logs/{id}/issues　指定した作業の課題一覧を取得  
GET    /api/tasks/{id}/work-logs/{id}/issues/{id}　課題の詳細取得  
POST   /api/tasks/{id}/work-logs/{id}/issues/{id}　指定した作業に課題を追加 (作業記録が残るときにも追加できる)
PATCH  /api/tasks/{id}/work-logs/{id}/issues/{id}　課題内容・習熟状況・改善案などの編集  
DELETE /api/tasks/{id}/work-logs/{id}/issues/{id}　課題の削除  

