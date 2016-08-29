# Regime
Regime is a ruby gem that checks the length of your source code files. It allows you to limit the length of your files, by reporting which files are going beyond the limit.
Just run the `regime` command at your 

## Installation

Add this line to your application's Gemfile:

```ruby
group :development do
  gem 'regime', github: 'Captive-Studio/regime'
end
```

And then execute:

    $ bundle


## Configuration
If the directory in which you run `regime` contains a `regime.yml` file, it will be used to configure regime.
Here's a sample of `regime.yml` file:

```YML
# authorized_line_count sets the limit of lines for each files. Default is a hundred.
authorized_line_count: 100

# warning_line_count sets a warning of lines for each files. Default is 80.
warning_line_count: 80

# checked_extensions lists the type of files that regime checks. Default settings only checks `rb` files.
checked_extensions:
  - rb

# the whitelist contains files that should be ignored by regime.
whitelist:
  - db/schema.rb # ignores db/schema.rb for a rails project
  - spec/**/*    # ignores all files in the spec folders
  
# tolerate_too_long_files specifies whether the regime command should raise an error when a file goes beyond the line limit. Default is false.
tolerate_too_long_files: false
```
