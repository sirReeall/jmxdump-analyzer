abort('Please run this using `bundle exec rake`') unless ENV["BUNDLE_BIN_PATH"]
require 'html-proofer'

desc "Test the website"
task :html_proofer do
  options = {
    :empty_alt_ignore => true, # maven-site-plugin does not add alt to images for some reason
    :allow_hash_href => true, # maven docs skin has "back to top href=# link"
    :check_html => true,
    :check_img_http => false, # gravatar images are configured as http
    :url_ignore => [/artifacts.alfresco.com/,/#astrachan/,/#sirReeall/], # Nexus artifacts requre a log in and retun 401 errors when tested
    :cache => {
      :timeframe => '6w'
    }
  }
  begin
    HTMLProofer.check_directory("./docs", options).run
  rescue => msg
    puts "#{msg}"
  end
end

task :default => [:test]