# README

# テーブル設計
# users
| Column           | Type     | Options                     |
|------------------| ---------|-----------------------------|
|email             |string    |null: false, unique: true    |
|encrypted_password|string    |null: false                  |
|name              |string    |null: false                  |
|profile           |text      |null: false                  |
|occupation        |text      |null: false                  |
|position          |text      |null: false                  |

# prototypes
| Column           | Type     | Options                     |
|------------------| ---------|-----------------------------|
|title             |string    |null: false,foreign_key: true|
|catch_copy        |text      |null: false                  |
|concept           |text      |null: false                  |
|user              |references|null: false                  |

# comments
| Column           | Type     | Options                     |
|------------------| ---------|-----------------------------|
|content           |text      |null: false                  |
|prototype         |references|null: false,foreign_key: true|
|user              |references|null: false,foreign_key: true|

