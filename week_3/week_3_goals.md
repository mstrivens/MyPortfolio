By the end of the week all developers can:

## Build a simple web app

Practical - Build a birthday greeter app
Afternoon challenge - Battle

**Skills**

- Structuring the code for apps that have user interaction and visual output.
- Testing apps that have user interaction and visual output.
- Tracing data between the browser and server.

## Follow an effective debugging process for web applications

- Debugging programs that use multiple languages.
- Using a framework (Sinatra) in your code.

- Debugging 2 skills workshop

## Explain the basics of how the web works (e.g. request/response, HTTP, HTML, CSS)

**Key Concepts**

- The relationship between a client and a server.
- How HTTP is used to send information over the web.
- RESTful APIs.
- The request/response cycle.
- Web templating with HTML/CSS.

**Practicals and Workshops**

- Workshop on Tuesday
- Do practical on HTTP servers on Monday
- Servers Pratical
- Clients Practical

## Explain the MVC pattern

## Use the Technical Learning Resource as a resource

## Daily Goals

**Monday 15th March**

GOAL: Take a look at HTTP servers practical & learning resources if time
PLAN: Look at practical, try and complete
EVIDENCE: Can understand concepts.
LEARNINGS: Looked at servers practical but didn't have the basic understanding to start it.
Doing the pair-programming helped. Some things to remember.
* If creating a Gemfile - you can gem 'name'
* in the Gemfile and then use the bundler.
* Shotgun doesn't work on ruby 3.0 so use 2.7.2
* Use index.erb to store visual elements for web dev
* Can use in conjunction with ruby
* need to require 'sinatra' in rb file and configure secret_sessions

configure do
  set :session_secret, "My session secret"
end

**Tuesday 16th March**

GOAL: Workshop on req-res cycle, look at servers practical
PLAN: Do workshop, discuss. Start servers practical
EVIDENCE: If i understand what's going on
LEARNINGS:
Did morning workshop on req-res flow:
We learned the flow between client, browser and server was as follows:

alias user=“User”
alias client=“Client/Browser ”
alias server=“Server”
alias disk cache=“Cache”
user->client:“User enters (incorrect) URL”
client->server:“GET /”
server-->client:“404, html”
client->client:“renders html”
client->user:“Displays error page”
user->client:“User enters (correct) URL”
client->server:“GET /”
server-->client:“200, html”
client->client:“renders html”
client->user:“Displays page”
user->client:“Click on link”
client->server:“GET /”
server-->client:“200, image request”
client->client:“render HTML”
client->server:“GET /cat.jpg”
server->client:“200, jpg”
client->client:“inject jpg”
(client->client:“renders HTML”)
client->user:“Displays page”

We enter a URL which sends an information request to the server based on the GET/POST defined
Get is generally for requesting information, post is generally for changing something in the server
When we make a get request it will fetch a piece of html which is then rendered and depending on what it says it will either fetch more information (like an image) or render it to the client.

We learned about using params in the afternoon.
You can use param[:name] in the ruby code and this will respond to @name in the erb file
You can also use quesry strings in the url to give information
e.g websitedomain/?name=Max


In the afternoon practical we learned how to set up capybara. Once the gemfiles and bundle has been run you need to enter PRY.
PRY> require 'capybara'
PRY> require 'selenium-webdriver'
PRY> include Capybara::DSL
PRY> visit http://capybaraworkout.herokuapp.com/

You can then use a number of capybara commmands to manipulate the website:

click_button "Start Workout!" --> name of a button
click_on 'Submit' (This is the value= on a button)
within(section .first).click ('left')  --> This says within a certain section click on a button
check (ticks a box)
fill_in 'name', "Max" --> fills in a field with a name

This is a resource for the information https://thoughtbot.com/upcase/test-driven-rails-resources/capybara.pdf

**Wednesday 17th March**

GOAL: Further knowledge on using capybara in web dev
PLAN: Continue through practical resources
EVIDENCE: Find 2 challenges within practicals.
LEARNINGS:

**setting up capybara with rspec**

*in app*

require 'sinatra'
class Battle < Sinatra::Application

*in spec_helper*

ENV['RACK_ENV'] = 'test'

# require Battle
require File.join(File.dirname(__FILE__), '..', 'app.rb')

require 'capybara'
require 'capybara/rspec'
require 'rspec'

Capybara.app = Battle

*in gemfile*

source 'https://rubygems.org'

gem 'rspec'
gem 'sinatra'
gem 'capybara'

*in config.ru*

require './app.rb'
run Battle

**Layout of feature test**

feature 'Testing infrastructure' do
  scenario 'can run app and check page content' do
    visit('/')
    expect(page).to have_content 'Testing infrastructure working!'
  end
end
