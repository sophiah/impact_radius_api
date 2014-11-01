# ImpactRadiusApi

Ruby wrapper for [Impact Radius API](http://dev.impactradius.com/display/api/Home).  Only [Media Partner Resources](http://dev.impactradius.com/display/api/Media+Partner+Resources) is supported.

## Installation

Add this line to your application's Gemfile:

```ruby
gem 'impact_radius_api'
```

And then execute:

    $ bundle

Or install it yourself as:

    $ gem install impact_radius_api

## Usage
This gem is designed to support [Media Partner Resources](http://dev.impactradius.com/display/api/Media+Partner+Resources).
All requests to the Impact Radius REST API require you to use HTTP Basic Authentication to convey your identity.

The username is your AccountSid (a 34 character string identifying your API account, starting with the letters "IR"). The password is your authentication token (AuthToken). These values are available on the Technical Settings page of your account. 

To start using the gem, you need to set up the AccountSid (username) and authentication token first. If you use Ruby on Rails, the API key can be set in a configuration file (i.e. `app/config/initializers/impact_radius.rb`), otherwise just set it in your script.

```ruby
require "impact_radius_api" # no need for RoR  :account_sid, :auth_token,
ImpactRadiusAPI.auth_token = ENV["IR_AUTH_TOKEN"]
ImpactRadiusAPI.account_sid = ENV["IR_ACCOUNT_SID"]
```

TODO: Write usage instructions here

## Contributing

1. Fork it ( https://github.com/[my-github-username]/impact_radius_api/fork )
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Add some feature'`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create a new Pull Request