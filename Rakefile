namespace :greeting do
  desc 'outputs hello to the terminal'
  task :hello do
    puts "hello from Rake!"
  end

  desc 'outputs hello in spanish to terminal'
  task :hola do
    puts "hola de Rake!"
  end
end

desc 'console'
task :console do

end

task :environment do
  require_relative './config/environment'
end

namespace :db do
  desc 'migrate db'
  task :migrate => :environment do
    Student.create_table
  end

  desc 'seed the db with dummy data'
  task :seed do
    require_relative './db/seeds.rb'
  end
end
