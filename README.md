# テーブル設計
## users テーブル

| Column            | Type       | Options                   |
| ----------------- | ---------- | --------------------------|
| name              | string     |  null: false, unique:true |
| first_name        | string     |  null: false              |
| first_name_kana   | string     |  null: false              |
| last_name         | string     |  null: false              |
| last_name_kana    | string     |  null: false              |
| birthday          | date       |  null: false              |
| email             | string     |  null: false, unique:true |
| encrypted_password| string     |  null:false               |

### Association

- has_many :food-racks
## food-racks テーブル

| Column          | Type       | Options                        |
| --------------- | -----------| -------------------------------|
| food_name       | string     | null: false                    |
| user            | references | null: false, foreign_key: true |
| memo            | text       |                                |
| category_id     | integer    |                                |
| food_deadline   | integer    | null: false                    |
### Association

- belongs_to :user