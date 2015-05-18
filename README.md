# lint-config
Configuration files for the source-code checking tools used on Bauer apps.

To add these files to your repo in folder `config/lint` at your root:

```git submodule add git@github.com:bauerpub/lint-config.git config/lint```

Then, to configure Hound, you can add the following `.hound.yml` file at the app root:

```ruby:
  config_file: config/lint/.ruby-style.yml

scss:
  config_file: config/lint/.scss-style.yml

coffeescript:
  config_file: config/lint/.coffeescript-style.json

javascript:
  config_file: config/lint/.javascript-style.json```
