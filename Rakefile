namespace :greeting do
  desc 'Outputs hello to terminal'
  task :hello do
    puts "hello from Rake!"
  end

  desc 'outputs hola to the terminal'
  task :hola do
    puts "hola de Rake!"
  end
end

namespace :db do
  desc 'migrate changes to your database'
  task migrate: :environment do
    Student.create_table
  end

  desc 'seed the database with dummy c=data'
  task seed: :environment do
    require_relative './db/seeds'
  end
end

desc 'drop into pry console'
task console: :environment do 
  Pry.start
end

task :environment do
  require_relative './config/environment'
end