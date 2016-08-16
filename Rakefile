# encoding: UTF-8
desc "Deploy the current version to nxtbgthng.com"
task :deploy do
  SERVER = 'evenly@watson.bitfever.de'
  PATH   = '/home/evenly/www'
  
  puts "Generating site…"
  `bundle exec jekyll build`
  puts "Uploading site to #{SERVER}…"
  `rsync -az --delete ./_site/ #{SERVER}:#{PATH}/`
end
