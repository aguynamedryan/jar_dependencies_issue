# mkristian/jar-dependencies issue

I'm not sure if this is a Big Deal, but I'm noticing an error message when
using Bundler to install gems through github.

This repo recreates the problem.

For reasons, I am using JRuby 9.1.2.0

I'm not sure if Bundler changed something recently.  I didn't see this error
under 1.14.3, but I upgraded to 1.15.4 and 1.16.pre.3 and both show the error.

To recreate:

```
git clone https://github.com/aguynamedryan/jar_dependencies_issue
cd jar_dependencies_issue
rvm use jruby-9.1.2.0
gem update bundler
bundle
```


My output was:

```
Using bundler 1.16.0.pre.3
Using dotenv 2.2.1
Using hashie 3.5.6
Using sequel 4.49.0
Using thor 0.20.0
Using sequelizer 0.1.0
Using conceptql 0.3.0 from https://github.com/outcomesinsights/conceptql (at master@1ee5743)
jar-dependencies: spec must be either String or Gem::Specification
Bundle complete! 1 Gemfile dependency, 7 gems now installed.
Use `bundle info [gemname]` to see where a bundled gem is installed.
```

