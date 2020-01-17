## groups_usersテーブル

|Column|Type|Options|
|------|----|-------|
|user_id|integer|null: false, foreign_key: true|
|group_id|integer|null: false, foreign_key: true|

### Association
- belongs_to :group
- belongs_to :user

## groupテーブル

|Column|Type|Options|
|------|----|-------|
|name|string|null: false, default:|

### Association
- 
- 
-

## userテーブル

|Column|Type|Options|
|------|----|-------|

### Association
- 
- 
-

## commentsテーブル

|Column|Type|Options|
|------|----|-------|

### Association
- 
- 
-