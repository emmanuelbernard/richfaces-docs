# A sample Guardfile
# More info at https://github.com/guard/guard#readme

require 'asciidoctor'
require 'erb'

guard 'shell' do
#  watch /^([^\/]*).*\/([^\/]*)\.asciidoc/ do |m|
  watch /^([^\/]*).*\/(Developer_Guide|Component_Reference)\.asciidoc/ do |m|
    "m[0] +  has changed"
    Asciidoctor.render_file(m[0], :to_file => m[1] + "/target/" + m[2] + ".html")
  end
end

guard 'livereload' do
  watch(%r{target/.+\.(css|js|html)})
end