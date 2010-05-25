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
  File.write(
    'build/karel.xml',
    ERB.new('karel.xml.erb').result(binding)
  )
end
