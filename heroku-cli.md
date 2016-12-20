# Heroku CLI

Installing heroku toolbelt
```bash
$ wget -qO- https://toolbelt.heroku.com/install.sh | sh
```

Verify installation
```bash
$ heroku --version
```

Login
```bash
$ heroku login
```

Start a new app
```bash
$ cd ~/myapp
$ heroku create
```

Run Postgres server locally
```bash
$ heroku local web
```

Start a console
```bash
$ heroku run --app pillow-qa rails console
```

