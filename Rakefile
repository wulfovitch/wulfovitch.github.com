def jekyll(opts = '')
  sh 'rm -rf _site'
  sh 'jekyll ' + opts
end
 
desc 'Build site using Jekyll'
task :build do
  jekyll
end
 
desc 'Start server on http://localhost:4000'
task :server do
  jekyll('--server --auto')
end
 
desc 'Build and deploy to production'
task :deploy => :build do
  sh 'rsync -rtzh --progress --delete _site/ wulfovitch@b3ta.info:~/www/wulfovitch.net/'
end