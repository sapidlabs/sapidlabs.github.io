---
layout: post
title: "Changing column name in rails"
meta: "enum rails-6 sapidlabs ruby on rails change column name"
categories: "rails"
tags: rails-6 ruby-on-rails rename column
---

![Ruby On Rails - SapidLabs][rails]

# Changing column name in Rails
Rails provides a simple method `rename_column` which can be used in a migration.

<br />
Example: Say you have a `User` model in your rails application, with a db field as `name`. Now, you want to change the name of the column. we should generate a migration by using `rails g migration change_users_name_to_title`. Our migration should look like:

```ruby
class ChangeUsersNameToTitle < ActiveRecord::Migration[6.0]
  def change
    rename_column :users, :name, :title
  end
end
```
<hr /> 
Now run `rails db:migrate` in order to make the changes to the database.

```ruby
## Rename column method
rename_column(:table_name, :column_name, :new_column_name)
```

<br />
Verify from the `schema.rb` to see if the field actually changed.

<br />

[rails]: /assets/images/shared/rails-6.jpg
