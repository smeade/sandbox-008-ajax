## Readme

An application to experiment with JavaScript in Rails.

Will demonstrate (not there yet):

* the basics of Ajax
* Unobtrusive JavaScript
* Rails' built-in helpers
* Ajax on the server side

Based on [RailsGuides documentation](http://edgeguides.rubyonrails.org/working_with_javascript_in_rails.html)

Demo Heroku app is [here](http://sandbox-008-ajax.herokuapp.com/).

## Notes

Demonstrates dynamic creation of modals upon demand, vs. loading up multiple modals waiting to be revealed.

In an initial version/commit, a modal dialog is created for each product listed in /products. A product's "reviews" modal dialog is revealed upon clicking
the 'Reviews' link for that product. This results in multiple, unnecessary and mostly un-viewed modals rendered on the page; killing page load times.

A future commit will replace that with Ajax generation of the modal upon clicking the 'Reviews' link (and then perhaps right before based on hover).

## Getting Started

1. Install gems:

        bundle install

2. Create the database:

        rake db:create

2. Migrate the database:

        rake db:migrate

4. Start the web server:

        rails server

5. Using a browser, go to [http://localhost:3000](http://localhost:3000) and you'll see:
"Listing products"

6. Create some Products and Reviews.

## Running the test suite

        rake

## Deploying to Heroku

1. Install the [Heroku toolbelt](https://devcenter.heroku.com/articles/getting-started-with-rails4#local-workstation-setup) on local workstation (if not already installed).

2. Create the [Heroku app](https://devcenter.heroku.com/articles/getting-started-with-rails4#deploy-your-application-to-heroku) (if not already created).

        heroku apps:create

3. [Deploy](https://devcenter.heroku.com/articles/git#deploying-code)

        git push heroku master

4. Run migrations

        heroku run rake db:migrate

5. Visit the deployed app

        heroku open

## License

This project is released under the [MIT License](http://www.opensource.org/licenses/MIT).