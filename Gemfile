source 'https://rubygems.org'

<% max_width = gemfile_entries.map { |g| g.name.length }.max -%>
<% gemfile_entries.each do |gem| -%>
<% if gem.comment -%>

# <%= gem.comment %>
<% end -%>
<%= gem.commented_out ? '# ' : '' %>gem '<%= gem.name %>'<%= %(, '#{gem.version}') if gem.version -%>
<% if gem.options.any? -%>
,<%= gem.padding(max_width) %><%= gem.options.map { |k,v|
  "#{k}: #{v.inspect}" }.join(', ') %>
<% end -%>
<% end -%>

# Use ActiveModel has_secure_password
# gem 'bcrypt', '~> 3.1.7'

# Use unicorn as the app server
# gem 'unicorn'

# Use Capistrano for deployment
# gem 'capistrano-rails', group: :development

<% unless defined?(JRUBY_VERSION) -%>
# Use debugger
# gem 'debugger', group: [:development, :test]
<% end -%>

<% if RUBY_PLATFORM.match(/bccwin|cygwin|emx|mingw|mswin|wince/) -%>
# Windows does not include zoneinfo files, so bundle the tzinfo-data gem
gem 'tzinfo-data', platforms: [:mingw, :mswin]
<% end -%>

gem "devise"