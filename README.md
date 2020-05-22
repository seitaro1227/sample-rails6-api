# sample-rails6-api
apiモードでnewしてrspecとfactory_botを設定したプロジェクト

## 作成時のコマンド
```
bundle install --path=vendor/bundle
bundle exec rails new ./ -B --api
gibo dump rails  >> .gitignore
bin/rails generate rspec:install
bundle exec spring binstub rspec
```

## generatorsの設定
config/application.rb
```
config.generators do |generator|
  generator.test_framework :rspec,
    fixtures: false,
    request_specs: true,
    helper_specs: false,
    routing_specs: false
  generator.factory_bot true
end
```

## rename
config/application.rb
```
module SampleRails6Api
```
## config/credentials.yml.enc
https://railsguides.jp/security.html#%E7%8B%AC%E8%87%AA%E3%81%AEcredential