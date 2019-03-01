namespace :db do
  
  desc 'database functionality'
  task :migrate => :environment do
    Student.create_table
  end
  
  desc 'check environment'
  task :environment do
    require_relative './config/environment.rb'
  end
  
  desc 'seed the database' 
  task :seed do
      require_relative './db/seeds.rb'
  end
end

desc 'drop into pry'
task :console => :environment do
    Pry.start
end
