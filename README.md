# README

# RailAppTrial

## Create Rails App (postgresql as database)

- rails new blog -d postgresql

## Start postgre

- brew services start postgresql

## Create the database

- ~~rails db:migrate:reset~~
- ~~rails db:seed~~
- ~~bin/setup~~

- rails db:create

## Generate new controller

- rails generate controller Welcome index

## Set root page

- config/routes.rb
- add "root 'welcome#index'"

## Creating new resource

- config/routes.rb
- add "resources :articles"
- run "rails routes"

## Generate controller for articles

- run "rails generate controller Articles"

## Create action in Articles controller

- controllers/articles_controller.rb
- add "def new
  end"

## Create new view for new action of Articles controller

- create "new.html.erb" in views/articles

## Create forms using form builder and the helper method form_with

## Create model "create" in Articles controller

- run "rails generate model Article title:string text:text"

Migrate db

- run "rails db:migrate"

## Create action "create" in Articles controller

## Create action "show" in Articles controller

## Create new view for show action of Articles controller

- create "show.html.erb" in views/articles

## Create action "index" in Articles controller

## Create new view for index action of Articles controller

- create "index.html.erb" in views/articles

## Adding links using link_to method

- <%= link_to 'My Blog', controller:'articles' %>
- <%= link_to 'New article', new_article_path %>

## Adding some validation

- In the Articles controller under the "def new ... end"
- add "Article.new"
- this is to avoid nulls

## Updating Articles

- Create edit action
- Create update action
- Create view for edit action
- use form_with(model: @article ...

## Using partials to clean up duplication in views

- create \_form.html.erb
- in partials it is by convention to be prefixed by an underscore(\_)

## Deleting articles

- Create destroy action
- Add link to delete with option of method: :delete, data" {confirm: 'Are you sure?"}

## Adding a second model

## Generating a Model

- \$ rails generate model Comment commenter:string body:text article:references
- belongs_to :article
- rails db:migrate

## Associating Models

- has_many :comments

## Adding a Route for Comments

- resources :articles do resources :comments end

## Generating a Controller

- rails generate controller Comments

## Refactoring

## Rendering Partial Collections

## Rendering a Partial Form

## Deleting Comments

## Deleteing Associated Objects

- has_many :comments, dependent: :destroy

## Security

## Basic Authentication

- http_basic_authenticate_with name: "dhh", password: "secret", except: [:index, :show]

_https://guides.rubyonrails.org/getting_started.html_
