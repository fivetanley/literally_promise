# LiterallyPromise

Stolen promise implementation from @tenderlove's talk at MWRC 2014.

## Installation

Add this line to your application's Gemfile:

    gem 'literally_promise'

And then execute:

    $ bundle

Or install it yourself as:

    $ gem install literally_promise

## Usage

```ruby
require 'literally_promise'

LiterallyPromise::Promise.new do
  puts "omg"
end
```

## Advanced Usage


```ruby
require 'literally_promise'

my_promise = LiterallyPromise::Promise.new do
  puts "omg it's starting"
  sleep 10
  2 * 2
end
```
Check the status of a promise:

``` ruby
my_promise.alive? # Checks the to see if a promise is pending
my_promise.stop?  # Checks the to see if a promise is fulfilled
my_promise.status # Shows the status of a promise
my_promise.raise  # halt a promise
my_promise.value  # Check the return value of a promise
my_promise.kill   # Break a promise. .terminate is an alias
```

## Contributing

1. Fork it ( http://github.com/fivetanley/literally_promise/fork )
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Add some feature'`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create new Pull Request
