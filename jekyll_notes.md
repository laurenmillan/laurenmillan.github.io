# Notes 
This project can built locally and deloyed using Ruby 2.7.0.

## Ruby Version
Verify version:
```
ruby -v
```

If not 2.7.0 a local Ruby environment can be used: 
```
rbenv init -
rbenv global 2.7.0
rbenv rehash
ruby -v // should now read the correct version
```

## Build Locally
Install RubyGems locally:
```
bundle install --path=vendor
```

Deploy:
```
bundle exec jekyll serve
```