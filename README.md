crashhub
========


[![Travis](https://img.shields.io/travis/bauerj/crashhub.svg?style=flat-square)](https://travis-ci.org/bauerj/crashhub) 
[![Coveralls](https://img.shields.io/coveralls/github/bauerj/crashhub.svg?style=flat-square)](https://coveralls.io/github/bauerj/crashhub) 
[![License](https://img.shields.io/github/license/bauerj/crashhub.svg?style=flat-square)](https://github.com/bauerj/crashhub/blob/master/LICENSE) 
[![Docker build](https://img.shields.io/docker/automated/bauerj/crashhub.svg?style=flat-square)](https://hub.docker.com/r/bauerj/crashhub/) 
[![Image Size](https://img.shields.io/microbadger/image-size/bauerj/crashhub.svg?style=flat-square)](https://hub.docker.com/r/bauerj/crashhub/) 



This is a simple web service that aggregates crash reports and opens issues on Github.

Config file
-----------
To start using crashhub, create a `config.json` based on `config.json.example`:

| config key     | value                                                                                                                                                          |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| db_engine      | Your database engine. Either `postgres`, `mysql` or `sqlite`.                                                                                                  |
| db_name        | The name of the database crashhub should use.                                                                                                                  |
| db_host        | Hostname of the database server. Leave this empty for sqlite.                                                                                                  |
| db_port        | Port of the database server. Leave this empty for sqlite.                                                                                                      |
| db_user        | Name of the database user. Leave this empty for sqlite.                                                                                                        |
| db_password    | Password of the database user. Leave this empty for sqlite.                                                                                                    |
| github_project | The Github project issues should be posted in.                                                                                                                 |
| github_token   | See [:octocat: Creating a personal access token for the command line](https://help.github.com/articles/creating-a-personal-access-token-for-the-command-line/) |

Running crashhub
-------

Database tables will be automatically created once you start crashhub.

### Testing
To run crashhub in a non-production environment (e.g for debugging), simply run `crashhub.py`.


### Production

For an extensive list of options to run crashhub in a high-performance production environment, see [Flask: Deployment Options](http://flask.pocoo.org/docs/0.12/deploying/).

