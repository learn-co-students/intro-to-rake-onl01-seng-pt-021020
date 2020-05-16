namespace :greeting do
  desc 'outputs hello to the terminal'
  task :hello do
    puts "hello from Rake!"
  end

  desc 'outputs hola to the terminal'
  task :hola do
    puts "hola de Rake!"
  end
end

namespace :db do
  desc 'migrate changes to the database'
  task :migrate => :environment do
    Student.create_table
  end

desc 'adds filler data (seed the database with data) to the table'
  task :seed => :environment do
    require_relative "./db/seeds.rb"
  end
end

desc 'requires environment file for task dependencies'
task :environment do
  require_relative './config/environment'
end

desc 'drop into the Pry console!'
task :console => :environment do
  Pry.start
end
