#this is Rake. Rake is better than bash for creating database tables.
#use rake (taskname) in the terminal to run the task
#and rake -T for a list of tasks with their description.

namespace :greeting do
  #putting them both under a greeting heading.
  desc 'outputs hello to the terminal' #the description.
    task :hello do #the name
    puts "hello from Rake!" #what it does
  end

  desc 'outputs hola to the terminal'
    task :hola do
    puts "hola de Rake!"
  end
end

namespace :db do
  desc 'migrate changes to your database'
  task :migrate => :enviornment do
    Student.create_table
  end

  #this is happening in the file
  # task :environment do
  #  require_relative './config/environment'
  # end

  desc 'seed the database with some dummy data'
  task :seed do
    require_relative './db/seeds.rb'
  end

  desc 'drop into the Pry console'
  task :console => :enviornment do
    Pry.start
  end
end
