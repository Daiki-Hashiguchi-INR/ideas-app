# DB設計

## categoriesテーブル

| Column             | Type   | Options      |
| ------------------ | ------ | -----------  |
| name           | string | null: false , uniqueness: true |


### Association

has_many :ideas

## ideasテーブル

| Column              | Type       | Options     |
| ------------------- | ---------- | ----------- |
| body                | text       | null: false |
| category            | references | foreign_key: true , null: false |

### Association

belong_to :category

