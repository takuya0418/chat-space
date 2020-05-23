# README

This README would normally document whatever steps are necessary to get the
application up and running.

Things you may want to cover:

* Ruby version

* System dependencies

* Configuration

* Database creation

* Database initialization

* How to run the test suite

* Services (job queues, cache servers, search engines, etc.)

* Deployment instructions

* ...
## usersテーブル
|Colum|type|Options|
|-----|----|-------|
|id|integer|null: false, unique: true|
|name|string|null: false|
|password|text|null: false|
|email|text|null: false, unique: true|

### Association
- has_many :groups, through: :groups_users
- has_many :groups_users
- has_many :messages

## groupsテーブル
|Colum|type|Options|
|-----|----|-------|
|id|integer|null: false, unique: true|
|name|string|null: false|

### Association
- has_many :users, through: :groups_users
- has_many :groups_users
- has_many :messages

## groups_usersテーブル
|Colum|type|Options|
|-----|----|-------|
|user_id|integer|null: false, foreign_key: true|
|group_id|integer|null: false, foreign_key: true|

### Association
- belongs_to :user
- belongs_to :group

## messagesテーブル
|Colum|type|Options|
|-----|----|-------|
|id|integer|null: false, unique: true|
|masseage|string|null: false|
|image|integer|null: false|
|timestamp|integer|null: false|

### Association
- belongs_to :user
- belongs_to :group
