## group_users table

|Column|Type|Options|
|------|----|-------|
|user|references|null:false,foreign_key:true|
|group|references|null:false,foreign_key:true|

### Association
- belongs_to :group
- belongs_to :user

## groups table

|Column|Type|Options|
|------|----|-------|
|name|string|null: false,default:|

### Association
- has_many:messages
- has_many:users,through:group_users
- has_many:group_users

## users table

|Column|Type|Options|
|------|----|-------|
|name|string|null:false,default:|
|email|string|null:false,default:|

### Association
- has_many:messages
- add_index:users,:name,unique:ture
- add_index:users,:email,unique:ture
- has_many:groups,through::group_users
- has_many:group_users

## messages table

|Column|Type|Options|
|------|----|-------|
|body|text| |
|image|string| |
|user|references|null:false,foreign_key:true,index:true|
|group|references|null:false,foreign_key:true,index:true|

### Association
- belongs_to:user
- belongs_to:group

