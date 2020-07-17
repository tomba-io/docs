## Libraries

### Language Libraries

Official libraries for common programming languages, like PHP, Python etc.

| Language   | Status      | Link                                                    | Package Manager                                                       |
| ---------- | ----------- | ------------------------------------------------------- | --------------------------------------------------------------------- |
| Javascript | In progress | [tomaba-io/node](https://github.com/tomaba-io/node)     | [tomba-io](https://www.npmjs.com/package/tomba-io)                    |
| Java       | In progress | [tomaba-io/java](https://github.com/tomaba-io/java)     | [tomaba-io](https://search.maven.org/search?q=a:tomaba-io)            |
| Python     | In progress | [tomaba-io/python](https://github.com/tomaba-io/python) | [tomaba-io](https://pypi.org/project/tomaba-io/)                      |
| PHP        | In progress | [tomaba-io/php](https://github.com/tomaba-io/php)       | [tomba-io/tomba-io](https://packagist.org/packages/tomba-io/tomba-io) |
| Ruby       | In progress | [tomaba-io/ruby](https://github.com/tomaba-io/ruby)     | [tomba-io](https://rubygems.org/gems/tomba-io)                        |
| Perl       | In progress | [tomaba-io/perl](https://github.com/tomaba-io/perl)     | [IO-tomba-io](https://metacpan.org/release/tomba-io/IO-tomba-io-1.0)  |
| D          | In progress | [tomaba-io/dlag](https://github.com/tomaba-io/dlang)    | [tomba-io](https://code.dlang.org/packages/tomba-io)                  |
| Lua        | In progress | [tomaba-io/lua](https://github.com/tomaba-io/lua)       | [tomba-io](https://luarocks.org/modules/benemohamed/tomba-io)         |
| elixir     | In progress | [tomaba-io/elixir](https://github.com/tomaba-io/elixir) | [tomba-io](https://hex.pm/packages/tomba-io)                          |
| Dart       | In progress | [tomaba-io/dart](https://github.com/tomaba-io/dart)     | [tomba-io](https://pub.dev/packages/tomba-io)                         |
| R          | In progress | [tomaba-io/rlang](https://github.com/tomaba-io/rlang)   |                                                                       |
| Swift      | In progress | [tomaba-io/swift](https://github.com/tomaba-io/swift)   |                                                                       |
| Go         | In progress | [tomaba-io/go](https://github.com/tomaba-io/go)         |                                                                       |
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
| CodeIgniter (PHP)              | In progress | [tomaba-io/codeigniter-tomba-io](https://github.com/tomaba-io/codeigniter-tomba-io) |
| cakephp (PHP)                  | In progress | [tomaba-io/cakephp-tomba-io](https://github.com/tomaba-io/cakephp-tomba-io)         |
| Meteor (NodeJS - Javascript)   | In progress | [tomaba-io/meteor](https://github.com/tomaba-io/meteor)                             |
| Express  (NodeJS - Javascript) | In progress |                                                                                     |
| Spring  (Java)                 | In progress |                                                                                     |
| Laravel (PHP)                  | In progress |                                                                                     |
| Django (Python)                | In progress |                                                                                     |
| Rails (Ruby)                   | In progress |                                                                                     |

### Third party libraries
There are a large number of unofficial tomba-io libraries written by third parties. While these aren't maintained by us and haven't been tested by us these libraries can be a great way to get started quickly with tomba-io if you're using a language or framework that we don't have an official library for. Search GitHub for [tomba-io](https://github.com/search?q=tomba-io) libraries.


If you’ve written a tomba-io library and would like to add it to this page, send an email to info@tomba.io.
