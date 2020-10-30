## users テーブル

| Column     | Type      | Options       |
|----------  | --------- | ------------- |
| email      | string    | NOT NULL      |
| password   | string    | NOT NULL      |
| name       | string    | NOT NULL      |
| profile    | text      | NOT NULL      |
| occupation | text      | NOT NULL      |
| position   | text      | NOT NULL      |


## prototypes テーブル

| Column     | Type       | Options                        |
|---------   | ---------  | ------------------------------ |
| title      | string     | NOT NULL                       |
| catch_copy | text       | NOT NULL                       |
| concept    | text       | NOT NULL                       |
| user       | references | null: false, foreign_key: true |

## comments テーブル

| Column     | Type       | Options                        |
|---------   | ---------  | ------------------------------ |
| text       | text       | NOT NULL                       |
| user       | references | null: false, foreign_key: true |
| prototype  | references | null: false, foreign_key: true |