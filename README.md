## groups_usersテーブル

|Column|Type|Options|
|------|----|-------|
|user_id|integer|null: false, foreign_key: true|
|group_id|integer|null: false, foreign_key: true|

### Association
- belongs_to :group
- belongs_to :user

## groupteテーブル

|Column|Type|Options|
|------|----|-------|
|name|string|null: false, default:|

### Association
- 
- 
-