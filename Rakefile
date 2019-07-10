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
  gem.name = "instamojo-ruby"
  gem.homepage = "http://github.com/Instamojo/Instamojo-rb"
  gem.license = "MIT"
  gem.summary = %Q{Instamojo Ruby library - Assists you to programmatically create, edit and delete offers on Instamojo}
  gem.description = %Q{Instamojo Ruby library - Assists you to programmatically create, edit and delete offers on Instamojo. Also supports listing, updation and details of Payments, Payments Requests and Refunds.}
  gem.email = "dev-accounts@instamojo.com"
  gem.authors = ["Instamojo Technologies"]
  # dependencies defined in Gemfile
end
Jeweler::RubygemsDotOrgTasks.new

require 'rspec/core'
require 'rspec/core/rake_task'
RSpec::Core::RakeTask.new(:spec) do |spec|
  spec.pattern = FileList['spec/**/*_spec.rb']
end

task :default => :spec

require 'rdoc/task'
Rake::RDocTask.new do |rdoc|
  version = File.exist?('VERSION') ? File.read('VERSION') : ""

  rdoc.rdoc_dir = 'rdoc'
  rdoc.title = "instamojo-ruby #{version}"
  rdoc.rdoc_files.include('README*')
  rdoc.rdoc_files.include('lib/**/*.rb')
end
