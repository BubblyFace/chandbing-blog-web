# coding:utf-8
desc 'hexo clean'
task 'c' do
  system 'hexo clean'
end

desc 'hexo generate'
task 'g' do
  # system 'hexo clean'
  system 'hexo generate'
end

desc 'hexo deploy'
task 'd' do
  system 'hexo deploy'
end

desc "备份到hexo分支"
task 'b' do
  system 'git add --all'
  system "git commit -a -m \"backup at #{Time.now.to_s.slice(0..-7)}\""
  system 'git push github hexo'
end

desc "clean -> generate -> deploy -> backup"
task :default => ['c','g','d','b']