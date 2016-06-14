require 'html-proofer'

task :test do
  sh "bundle exec jekyll build"
  HTMLProofer.check_directory("./_site", :empty_alt_ignore => true, :external_only => true).run
end
