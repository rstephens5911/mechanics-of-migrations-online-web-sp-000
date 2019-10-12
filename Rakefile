require_relative './config/environment'
require 'sinatra/activerecord/rake'

task :console do
  require 'irb'
  ARGV.clear
  IRB.start

  namespace :db do
    desc 'migrate database changes'
    task :migrate => environment do
      CreateArtists.change
    end
  end

end
