# teamcity-jasmine

After a bit of pain, I managed to get TeamCity to run my Jasmine tests as a build step, and output the results into TeamCity. This repo simply contains the files that were successful.

Deps
====

- TeamCity
- Jasmine
- PhamtomJS

Usage
=====

Add a command line build step in TeamCity. Have a custom script run:

```
phantomjs run-jasmine.js <your test runner>
```

So in this case:

```
phantomjs run-jasmine.js test/index.html
```

Note that you'll have to specify the full system path for this to work, so more like:

```
phantomjs /users/blah/Sites/blah/run-jasmine.js ...
```

Credits
=======

There was no skill involved from my part. Just a fair bit of trial and error. The cool stuff is Larry Myers TeamCity reporter:

https://github.com/larrymyers/jasmine-reporters
