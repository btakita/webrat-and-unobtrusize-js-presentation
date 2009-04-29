task :default do
  system("slideshow presentation.markdown --fullerscreen")
  puts "run rake | tail -n1 | [pbcopy|xsel -b]"
  puts "Open Firefox and paste the address in the address bar"
  puts "file://#{File.dirname(__FILE__)}/presentation.html"
end