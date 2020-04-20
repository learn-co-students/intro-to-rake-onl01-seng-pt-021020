desc 'outputs hello to the terminal'
task :hello do
  puts "hello from Rake!"
end

namespace :greeting do
  desc 'outputs hello in terminal'
  task :hello do
    puts "hello from Rake!"
  end

  desc 'outputs hola in terminal'
  task :hola do
    puts "hola de Rake!"
  end
end

task :environment do
  require_relative './config/environment'
end

namespace :db do
  desc 'migrate changes to you database'
  task :migrate => :environment do
    Student.create_table
  end

  desc 'seed the database with dummy data'
  task :seed do
    require_relative './db/seeds.rb'
  end
end

desc 'drop into Pry console'
task :console do
  Pry.start
end
