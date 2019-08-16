
namespace :greeting do
  desc 'outputs hello to the terminal'
  task :hello do
    puts "hello from Rake!"
  end

  desc 'prints friendly message to screen'
  task :goodmorning do
    puts "good morning to you!"
  end  # ends goodmorning task

  desc 'outputs hola to the terminal'
  task :hola do
    puts "hola de Rake!"
  end  # ends hola task
end  # ends greeting namespace


namespace :db do
  desc 'migrate changes to your database'
  task :migrate => :environment do
    Student.create_table
  end  # ends migrate task

  desc 'seed the database with some dummy data'
  task :seed do
    require_relative './db/seeds.rb'
  end  # ends seed task
end  # ends db namespace

task :environment do
  require_relative './config/environment'
end  # ends environment task

desc 'drop into the Pry console'
task :console => :environment do
  Pry.start
end  # ends console task