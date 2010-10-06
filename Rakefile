$:.unshift(File.dirname(__FILE__) + '/../../lib')
require 'cucumber/rake/task'
require "bundler/version"
require "ruby_reddit_api/version"

Cucumber::Rake::Task.new do |t|
  t.cucumber_opts = %w{--format pretty}
end

task :build do
    system "gem build .gemspec"
end

task :release => :build do
    system "gem push ruby_reddit_api-#{Reddit::VERSION}.gem"
end

task :default => [:cucumber]
