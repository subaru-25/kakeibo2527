<!-- # README

# 家計簿アプリ

## 概要 家計簿アプリは、ユーザーが収入や支出を簡単に管理できるWebアプリケーションです。

## テーブル設計

### users テーブル

| Column             | Type   | Options                       |
| ------------------ | ------ | ----------------------------- |
| email              | string | null: false                   |
| encrypted_password | string | null: false, unique: true     |
| name               | string | null: false                   |
| profile            | text   | null: false                   |
| occupation         | text   | null: false                   |
| position           | text   | null: false                   |

### income_categories テーブル

| Column      | Type       | Options                        |
| ----------- | ---------- | ------------------------------ |
| name        | string     | null: false                    |
| user        | references | null: false, foreign_key: true |

### incomes テーブル

| Column              | Type       | Options                        |
| ------------------- | ---------- | ------------------------------ |
| amount              | integer    | null: false                    |
| date                | date       | null: false                    |
| description         | text       |                                |
| income_category     | references | null: false, foreign_key: true |
| user                | references | null: false, foreign_key: true |

### expense_categories テーブル

| Column      | Type       | Options                        |
| ----------- | ---------- | ------------------------------ |
| name        | string     | null: false                    |
| user        | references | null: false, foreign_key: true |

### expenses テーブル

| Column              | Type       | Options                        |
| ------------------- | ---------- | ------------------------------ |
| amount              | integer    | null: false                    |
| date                | date       | null: false                    |
| description         | text       |                                |
| expense_category    | references | null: false, foreign_key: true |
| user                | references | null: false, foreign_key: true | -->