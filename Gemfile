source "https://rubygems.org"

# Core Jekyll gem
gem "jekyll", "~> 4.4.1"

# Theme and style-related gems
gem "minima", "~> 2.5"
gem "jekyll-sass-converter"

# Jekyll plugins (these can be in a separate group)
group :jekyll_plugins do
  gem "jekyll-feed", "~> 0.12"
end

# Platform-specific gems (only needed for Windows or JRuby platforms)
platforms :mingw, :x64_mingw, :mswin, :jruby do
  gem "tzinfo", ">= 1", "< 3"
  gem "tzinfo-data"
end

gem "wdm", "~> 0.1", :platforms => [:mingw, :x64_mingw, :mswin]
gem "http_parser.rb", "~> 0.6.0", :platforms => [:jruby]
