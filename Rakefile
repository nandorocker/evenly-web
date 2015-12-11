# encoding: UTF-8
desc "Deploy the current version to nxtbgthng.com"
task :deploy do
  SERVER = 'toto@watson.bitfever.de'
  PATH   = '/var/www/evenly.io'
  
  puts "Generating site…"
  `bundle exec jekyll build`
  puts "Uploading site to #{SERVER}…"
  `rsync -az --delete ./_site/ #{SERVER}:#{PATH}/`
end
