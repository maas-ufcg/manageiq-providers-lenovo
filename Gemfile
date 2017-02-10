# Declare your gem's dependencies in manageiq-providers-lenovo.gemspec.
# Bundler will treat runtime dependencies like base dependencies, and
# development dependencies will be added by default to the :development group.
gemspec

group :test do
  gem "simplecov", :require => false
  gem "codeclimate-test-reporter", "~> 1.0.0", :require => false
end


unless dependencies.detect { |d| d.name == "xclarity_client" }
  gem "xclarity_client", git: "git://github.com/lenovo/xclarity_client", :branch => "development"
end

# Declare any dependencies that are still in development here instead of in
# your gemspec. These might include edge Rails or gems from your path or
# Git. Remember to move these dependencies to your gemspec before releasing
# your gem to rubygems.org.

# Load Gemfile with dependencies from manageiq
eval_gemfile(File.expand_path("spec/manageiq/Gemfile", __dir__))
