## Libraries

### Language Libraries

Official libraries for common programming languages, like PHP, Python etc.

| Language   | Status      | Link                                                    | Package Manager                                                       |
| ---------- | ----------- | ------------------------------------------------------- | --------------------------------------------------------------------- |
| Javascript | In progress | [tomba-io/node](https://github.com/tomba-io/node)     | [tomba-io](https://www.npmjs.com/package/tomba-io)                    |
| Java       | In progress | [tomba-io/java](https://github.com/tomba-io/java)     | [tomba-io](https://search.maven.org/search?q=a:tomba-io)            |
| Python     | In progress | [tomba-io/python](https://github.com/tomba-io/python) | [tomba-io](https://pypi.org/project/tomba-io/)                      |
| PHP        | In progress | [tomba-io/php](https://github.com/tomba-io/php)       | [tomba-io/tomba-io](https://packagist.org/packages/tomba-io/tomba-io) |
| Ruby       | In progress | [tomba-io/ruby](https://github.com/tomba-io/ruby)     | [tomba-io](https://rubygems.org/gems/tomba-io)                        |
| Perl       | In progress | [tomba-io/perl](https://github.com/tomba-io/perl)     | [IO-tomba-io](https://metacpan.org/release/tomba-io/IO-tomba-io-1.0)  |
| D          | In progress | [tomba-io/dlag](https://github.com/tomba-io/dlang)    | [tomba-io](https://code.dlang.org/packages/tomba-io)                  |
| Lua        | In progress | [tomba-io/lua](https://github.com/tomba-io/lua)       | [tomba-io](https://luarocks.org/modules/benemohamed/tomba-io)         |
| elixir     | In progress | [tomba-io/elixir](https://github.com/tomba-io/elixir) | [tomba-io](https://hex.pm/packages/tomba-io)                          |
| Dart       | In progress | [tomba-io/dart](https://github.com/tomba-io/dart)     | [tomba-io](https://pub.dev/packages/tomba-io)                         |
| R          | In progress | [tomba-io/rlang](https://github.com/tomba-io/rlang)   |                                                                       |
| Swift      | In progress | [tomba-io/swift](https://github.com/tomba-io/swift)   |                                                                       |
| Go         | In progress | [tomba-io/go](https://github.com/tomba-io/go)         |                                                                       |
| C#         | In progress |                                                         |                                                                       |
| Rust       | In progress |                                                         |                                                                       |
| Haskell    | In progress |                                                         |                                                                       |
| Erlang     | In progress |                                                         |                                                                       |
| C          | In progress |                                                         |                                                                       |


### Framework Libraries

Official libraries for common frameworks. These libraries should use the official lanaguge library as a dependency, so for example the Django library should use the Python library.

In the framework libraries we can assume more about the developer's use case, and we probably have access to more information, such as a HTTP request object. We can therefore implement additional functionality that
doesn't make sense in the core language library. This includes bot filtering (not sending requests to our API if the user agent belongs to a "bot").

The framework libraries should make it *as simple as possible* to use our API. For example, ideally only a few lines of code would be required to get tomba-io data for everyone accessing your Ruby site.

| Framework                      | Status      | Link                                                                                |
| ------------------------------ | ----------- | ----------------------------------------------------------------------------------- |
| CodeIgniter (PHP)              | In progress | [tomba-io/codeigniter-tomba-io](https://github.com/tomba-io/codeigniter-tomba-io) |
| cakephp (PHP)                  | In progress | [tomba-io/cakephp-tomba-io](https://github.com/tomba-io/cakephp-tomba-io)         |
| Meteor (NodeJS - Javascript)   | In progress | [tomba-io/meteor](https://github.com/tomba-io/meteor)                             |
| Express  (NodeJS - Javascript) | In progress |                                                                                     |
| Spring  (Java)                 | In progress |                                                                                     |
| Laravel (PHP)                  | In progress |                                                                                     |
| Django (Python)                | In progress |                                                                                     |
| Rails (Ruby)                   | In progress |                                                                                     |

### Third party libraries
There are a large number of unofficial tomba-io libraries written by third parties. While these aren't maintained by us and haven't been tested by us these libraries can be a great way to get started quickly with tomba-io if you're using a language or framework that we don't have an official library for. Search GitHub for [tomba-io](https://github.com/search?q=tomba-io) libraries.


If you’ve written a tomba-io library and would like to add it to this page, send an email to info@tomba.io.
