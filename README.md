# lint-config
Configuration files for the source-code checking tools used on Bauer Xcel Media USA apps.:
* [Rubocop](https://github.com/bbatsov/rubocop)
* [CoffeeLint](http://www.coffeelint.org/)
* [JSHint](https://github.com/jshint/jshint)
* [SCSS-Lint](https://github.com/causes/scss-lint)

To add these files to your repo in folder `config/lint` at your root:

```git submodule add git@github.com:bauerpub/lint-config.git config/lint```

## To run lint tools locally

### Rubocop
Install https://github.com/bbatsov/rubocop localy with `gem install rubocop`.

To use Rubocop to check file.rb:
`$ rubocop file.rb --config config/lint/.ruby-style.yml`

### CoffeeLint
Install [CoffeeLint](http://www.coffeelint.org/) locally with `gem install coffeelint`.

To use CoffeeLint to check file.coffee:
`$ coffeelint -f config/lint/.coffeescript-style.json file.coffee`

### JSHint
Install [JSHint](https://github.com/jshint/jshint) locally with `gem install jshint` or `npm install jshint`.

To use JSHint to check file.js:
`$ jshint --config config/lint/.javascript-style.json file.js`

### SCSS-Lint
Install [SCSS-Lint](https://github.com/brigade/scss-lint) locally with `gem install scss-lint`.

To use SCSS-Lint to check file.scss:
`$ scss-lint --config config/lint/.scss-style.yml file.scss`


## Using these config files with Hound

To configure Hound's behavior on a repository, you can add the following `.hound.yml` file at the app root:

    ruby:
      config_file: config/lint/.ruby-style.yml
    scss:
      config_file: config/lint/.scss-style.yml
    coffeescript:
      config_file: config/lint/.coffeescript-style.json
    javascript:
      config_file: config/lint/.javascript-style.json
