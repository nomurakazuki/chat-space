## groups_users table

|Column|Type|Options|
|------|----|-------|
|user_id|integer|null: false, foreign_key: true|
|group_id|integer|null: false, foreign_key: true|

### Association
- belongs_to :group
- belongs_to :user

## group table

|Column|Type  |Options|
|------|----  |-------|
|name  |string|null: false, default:|

### Association
- 
- 
-

## users table

|Column|Type|Options|
|------|----|-------|
|name|string|index:true,null:false,unique:true|
|mail|string|null:false|

### Association
- has_many:groups,through:members
- has_many:comments
- has_many:members

## comments table

|Column|Type|Options|
|------|----|-------|

### Association
- 
- 
-