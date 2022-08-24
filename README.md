# rails-sso-example

An example Ruby on Rails application demonstrating how SSO works with WorkOS and Rails.
The application is built with Rails 6 and Bootstrap with Webpack, and also uses Devise.

## Get Started

### Requirements

- Ruby 2.7.2
- Rails 7
- Foreman gem

### Clone, install and migrate the database

```bash
git clone https://github.com/sgrant0225/okta_sso_sample_app.git
cd okta_sso-sample_app.git
bundle install
yarn install --check-files
rails db:migrate
```

## Run the application and sign in using SSO

Start the server:
```bash
foreman start -f Procfile.dev
```

### Application Flow

- Head to `http://localhost:5000`
- If you're not authenticated, the site will re-direct to `http://localhost:5000/users/sign_in`
- Here you can authenticate with Username/Password, or with the SSO you set up with WorkOS
- To authenticate with SSO, input the domain you used to set up your WorkOS connection, and select the `Sign in with SSO` button
- After you sign in with SSO, it will take you to the Okta login page 
- For email input: sgrant@2u.com and the password: demoaccount02*
- After successfully authenticating, you should see a JSON print out of your user information

For more information, see the [WorkOS Ruby SDK documentation](https://docs.workos.com/sdk/ruby).
