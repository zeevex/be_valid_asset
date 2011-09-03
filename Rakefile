# encoding: utf-8

require 'rubygems'
require 'bundler'
begin
  Bundler.setup(:default, :development)
rescue Bundler::BundlerError => e
  $stderr.puts e.message
  $stderr.puts "Run `bundle install` to install missing gems"
  exit e.status_code
end
require 'rake'

require 'jeweler'
Jeweler::Tasks.new do |gem|
  # gem is a Gem::Specification... see http://docs.rubygems.org/read/chapter/20 for more options
  gem.name = "be_valid_asset"
  gem.homepage = "http://github.com/unboxed/be_valid_asset"
  gem.license = "MIT"
  gem.summary = %Q{Markup validation for RSpec}
  gem.description = %Q{Provides be_valid_xhtml, be_valid_css and be_valid_feed matchers for rspec controller and view tests.}
  gem.email = "github@unboxedconsulting.com"
  gem.authors = ['Alex Tomlins', 'Sebastian de Castelberg', 'Ben Brinckerhoff']
  gem.files.exclude "*.gemspec", '.gitignore'
end
Jeweler::RubygemsDotOrgTasks.new

require 'spec/rake/spectask'

task :default => :spec
Spec::Rake::SpecTask.new do |t|
  t.spec_opts = ['--options', File.join(File.dirname(__FILE__), %w(spec spec.opts))]
end
