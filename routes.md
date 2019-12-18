#### Define route on the fly
```ruby
  # Domain Verification through random text
  match 'MP_verify_PLik6rsBaV39n4y2.txt' => lambda { |_env|
    [200, { 'Content-Type' => 'text/plain' }, ['PLik6rsBaV39n4y2']]
  }, via: :get
```
