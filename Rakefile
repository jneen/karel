class File
  def self.write(filename, content)
    self.open(filename, 'w') do |f|
      f.write content
    end
  end
end

task :build do
  require 'erb'
  content = File.read('karel.html')
  template = File.read('karel.xml.erb')
  File.write(
    'build/karel.xml',
    ERB.new(template).result(binding)
  )
end
