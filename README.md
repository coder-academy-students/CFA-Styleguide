<p align="center"><img src="https://github.com/coder-factory-academy/cf-guidline-css/blob/master/CFA.png"></p>

Coder Factory Academy - Styleguide
======

- Use soft-tabs with a two space indent.
- Keep lines fewer than 80 characters.
- Never leave trailing whitespace.
- End each file with a blank newline.
- Use spaces around operators, after commas, colons and semicolons, around { and before }.

```
  sum = 1 + 2
  a, b = 1, 2
  1 > 2 ? true : false; puts "Hi"
  [1, 2, 3].each { |e| puts e }
```

- No spaces after (, [ or before ], ).

```
  some(arg).other
  [1, 2, 3].length
```

- No spaces after !.

```
  !array.include?(element)
```

- Define classes with the following structure (comments are for the clarity of the example and are not required):

```
  class User
    # Constants
    TIME_ALLOWED_INACTIVE = 10.minutes
  
    # Class method calls / DSL calls
    attr_reader :name, :address
  
    # Class method definitions
    def self.create(attrs)
      # ...
    end
  
    # Instance methods
    def send_email(email)
      # ...
    end
  
    # protected methods
    protected
  
    def protected_call_here
    end
  
    # private methods
    private
  
    def private_call_here
    end
  
    # Inner classes
    FakeUserError = Class.new(StandardError)
  
    class InnerClassMagic
    end
  end
```

- Don't align tokens

```
  # Bad, adding, removing, or changing values will be both annoying and produce
  # a noisy diff if it requires re-alignment
  foo       = "foo"
  bar_thing = "thing"
  other     = "other"
  
  {
    foo:       "foo"
    bar_thing: "thing"
    other:     "other"
  }
  
  # Good
  foo = "foo"
  bar_thing = "thing"
  other = "other"
  
  {
    foo: "foo"
    bar_thing: "thing"
    other: "other"
  }
```
