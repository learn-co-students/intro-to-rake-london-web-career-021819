desc 'outputs hello to the terminal'
task :hello do
  puts "hello from Rake!"
end

namespace :greeting do
  desc 'outputs hello to terminal'
  task :hello do
    puts 'hello from Rake!'
  end

  desc 'outputs hola to terminal'
  task :hola do
    puts 'hola de Rake!'
  end
end

desc 'Pry'
task :console => :environment do
  Pry.start
end

namespace :db do
  desc 'migrates'
  task :migrate => :environment do
    Student.create_table
  end

  desc 'seeds database'
  task :seed do
    require_relative './db/seeds.rb'
  end
end

desc 'accesses environment'
task :environment do
  require_relative './config/environment'
end
