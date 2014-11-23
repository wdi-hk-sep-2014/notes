# Heroku

Heroku is used as quick production deployment, it provides the free subdomain to you.

1. Login to Heroku
2. Download `Heroku Toolbelt`
3. Change database from `sqlite` to `pg`
  - Prepare your application without production mode `bundle install --without production`
4. `heroku apps:create`
5. `git push heroku master`

Heroku is one choice for deployment. In the future, you may want to use AWS or Digital Ocean for your production applications.

## Reference Links

- [Deploying to Heroku with Git](https://devcenter.heroku.com/articles/git)
- [12factor](http://12factor.net/dev-prod-parity)