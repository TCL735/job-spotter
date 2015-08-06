# JobSpotter

Search, Compare, Apply

> Search for open positions in your desired geographical locations and industries. Simply click on a map marker, or make specific location and title searches, to view the jobs list.

> Review the available postings to find the role that's best suited to you. Compare average salaries and openings by city and title.

> Click on the provided job link to view the source of the posting and apply to the position. Check back in regularly to see the newest postings - jobs are updated daily.

## Team

  - __Product Owner__: Paul Sokolik
  - __Development Team Members__: Ashwin Aravindan, Chris Staton, Timmy Luong

## Table of Contents

1. [Usage](#Usage)
1. [Requirements](#requirements)
1. [Development](#development)
    1. [Installing Dependencies](#installing-dependencies)
    1. [Tasks](#tasks)
1. [Testing](#testing)
1. [Deployment](#deployment)
1. [Team](#team)
1. [Contributing](#contributing)

## Usage

> [Install dependencies](#installing-dependencies)

> Start MySQL server
```sh
mysql.server start
mysql -u root
```

> Run gulp
```sh
gulp
```

## Requirements

- backbone: 1.2.1
- bcrypt-nodejs: 0.0.3
- bluebird: 2.9.30
- body-parser: 1.13.1
- bookshelf: 0.8.1
- chai: 1.9.0
- cookie-parser: 1.3.5
- cron: 1.0.9
- d3-browserify: 3.4.12
- express: 4.12.4
- express-method-override: 0.0.3
- express-session: 1.11.3
- indeed-api: 1.0.0
- jquery: 2.1.4
- jquery-ui-browserify: 1.11.0-pre-seelio
- knex: 0.8.6
- mocha: 2.0.1
- morgan: 1.6.0
- mysql: 2.7.0
- node: 0.0.0
- passport: 0.2.2
- passport-linkedin-oauth2: 1.2.1
- passport-local: 1.0.0
- react: 0.13.3
- react-d3: 0.3.1
- request: 2.58.0
- underscore: 1.8.3

## Development


### Installing Dependencies

From the root directory:

```sh
npm install -g bower
npm install
bower install
mysql.server start
```

## Testing

> Must use mocha version 2.0.1 for React testing
```
npm install mocha@2.0.1
```

> Do not remove or rename compiler.js

> Do not remove or rename testdom.js

> Avoid adding any new files to folder test/

> Additional tests should be added in shallowRenderSpec.js or serverSpec.js


## Deployment

Heroku:
The deployment process will depend upon your source of data and may require additional steps specific to your own implemention.

> (Optional) For better performance, add a Google Maps API key in client/index.html by replacing "sensor=true"

> (Optional) Use a local file for Google Maps Utility Marker Clusterer rather than the default svn

> Remove dist/ folder from .gitignore

> Run gulp to update dist/src/build.js

> (Recommended) Install a utility that minifies JavaScript files
```sh
npm install -g uglifyjs
```
> (Recommended) Minify dist/src/build.js

> (Recommended) Rename the minified file as build.js (this fill will be included in index.html)

> From the root directory, make a commit from your master branch, then push to Heroku (may require force push)
```sh
git add *
git commit
git push --force heroku master
```
> After Heroku confirms deployment, reset the temporary changes by resetting the HEAD of your master branch
```sh
git reset HEAD~1
git checkout -- .
```

> To manage your app log in to the Heroku Dev Center

> For a tutorial on deployment read https://devcenter.heroku.com/articles/getting-started-with-nodejs#introduction

### Database
ClearDB MySql 

> Only needs to be set up once when you deploy the first time to Heroku

> Set up your database initially
```sh
heroku addons:create cleardb
```

### Roadmap


View the project roadmap [here](https://waffle.io/unbiased-marsupial/job-spotter)


## Contributing

See [CONTRIBUTING.md](https://github.com/unbiased-marsupial/job-spotter/blob/master/CONTRIBUTING.md) for contribution guidelines.
