require 'shellwords'

# require 'github/markup'

task 'render' do
  FileList.new('content/*.md').each do |file|
    dest = File.join('rendered', "#{File.basename(file, '.md')}.html")
    sh(['octodown', '--style', 'atom', '--raw', file].shelljoin, out: dest)
    # File.write(dest, GitHub::Markup.render('content/index.md', File.read('content/index.md')))
  end
end
