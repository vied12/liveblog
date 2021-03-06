# Liveblog Client based on Superdesk Client
[![Build Status](https://travis-ci.org/superdesk/liveblog-client.svg)](https://travis-ci.org/superdesk/liveblog-client)
[![devDependency Status](https://david-dm.org/superdesk/liveblog-client/dev-status.png)](https://david-dm.org/superdesk/liveblog-client#info=devDependencies)
[![Coverage Status](https://img.shields.io/coveralls/superdesk/liveblog-client.svg)](https://coveralls.io/r/superdesk/liveblog-client?branch=master)

Liveblog Client is a javascript client for Liveblog REST API server.

*License*: [GPLv3](http://www.gnu.org/licenses/gpl-3.0.txt)

*Copyright*: [Sourcefabric o.p.s.](http://www.sourcefabric.org)


## Setup

Client requires `nodejs` installed and a few steps:
```
npm install -g bower grunt-cli
npm install # install other node dependencies
bower install # install bower components
```
After you can start local dev server on port `9000`:
```
grunt server
```

### Running with docker
This also will start frontend on localhost:9000.
Change `http://localhost:5000` to an actual backend server.
```
docker build -t liveblog-client:devel ./
docker run -i -p 9000:9000 -t liveblog-client:devel grunt server --server=http://localhost:5000 --force
```

Also u can start it with default parameters using vagrant:
```
vagrant up --provider=docker
```

## Info for contributors

### Commit messages

Every commit has to have a meaningful commit message in form:

```
Title
[<empty line>
Description]
[<empty line>
JIRA ref]
```

Where [JIRA ref](https://confluence.atlassian.com/display/FISHEYE/Using+smart+commits) is at least Issue code eg. ```LBSD-13```.

For trivial changes you can ommit JIRA ref or Description or both: ```Fix typo in liveblog.translate docs.```

### CI

You can test your code before sending a PR via: ```grunt ci```

