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
  gem.name = "hanna_gudao"
  gem.homepage = "http://github.com/cnruby/hanna_gudao"
  gem.license = "MIT"
  gem.summary = %Q{A rework of the Hanna generator for RDoc 3.x}
  gem.description = %Q{}
  gem.email = "gudao.luo@gmail.com"
  gem.authors = ["Erik Hollensbe", "James Tucker", "Mislav Marohnic"]
  # Include your dependencies below. Runtime dependencies are required when using your gem,
  # and development dependencies are only needed for development (ie running rake tasks, tests, etc)
  gem.add_runtime_dependency 'haml', "= 3.0.25"
  gem.add_runtime_dependency 'rdoc', "~> 3.12"
  gem.add_development_dependency 'jeweler', "~> 1.8.3"
  gem.add_development_dependency 'rake', "~> 0.9.2.2"
end
Jeweler::RubygemsDotOrgTasks.new

require 'rdoc/task'
RDoc::Task.new do |rdoc|
  version = File.exist?('VERSION') ? File.read('VERSION') : ""

  rdoc.rdoc_dir = 'rdoc'
  rdoc.title = "hanna_gudao #{version}"
  rdoc.rdoc_files.include('README*')
  rdoc.rdoc_files.include('lib/**/*.rb')
end
