require "rubygems"
require "bundler/setup"
require "stringex"
require 'nokogiri'
require 'redcarpet'
require 'open-uri'

FILE_SEARCH_PATTERN = "source/**/*.{markdown, textile}"
MARKERS = {"todo" => :red, "outline" => :yellow, "pending" => :yellow, "edit" => :yellow, "review" => :green, "wip" => :red}
COLORIZE = true

namespace "tags" do
  MARKERS.keys.each do |marker|
    desc "Pull out #{marker.upcase} lines"
    task marker do
      count = print_lines_containing(marker)
      puts "#{count} #{marker.upcase} tags remain\n\n"
    end
  end
  
  desc "Pull out all marked lines"
  task :all do
    print_lines_containing(MARKERS.keys)
  end
  
  class String
    def red; colorize(self, "\e[1m\e[31m"); end
    def yellow; colorize(self, "\e[1m\e[33m"); end
    def green; colorize(self, "\e[1m\e[32m"); end
    def underline; colorize(self, "\e[1m\e[4m"); end
    def colorize(text, color_code)
      COLORIZE ? "#{color_code}#{text}\e[0m" : text
    end
  end
end

def print_lines_containing(*keywords)
  counter = 0
  Dir.glob(FILE_SEARCH_PATTERN) do |filename|
    filename_printed = false
    File.open(filename).lines.each do |line|
      if line.downcase.match(/.*[^\`]?\[(#{keywords.join("|")})+.*\].*/)
        unless filename_printed
          puts "\n" + filename.underline
          filename_printed = true
        end
        counter += 1
        puts line.chomp.send(MARKERS[$1.downcase])
      end
    end
  end
  puts ""
  return counter
end