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

##usersテーブル
|Colum|type|Options|
|-----|----|-------|
|id|integer|null: false, foreign_key: true|
|password|text|null: false, foreign_key: true|
|email|text|null: false, foreign_key: true|

##groupテーブル
|Colum|type|Options|
|-----|----|-------|
|id|integer|null: false, foreign_key: true|
|groupname|string|null: false, foreign_key: true|
|masseage|string|null: false, foreign_key: true|
|image|integer|null: false, foreign_key: true|
|timestamp|integer|null: false, foreign_key true|

##groups_usersテーブル
|Colum|type|Options|
|-----|----|-------|
|user_id|integer|null: false, foreign_key: true|
|group_id|integer|null: false, foreign_key: true|
|username|string|null: false, foreign_key: true|