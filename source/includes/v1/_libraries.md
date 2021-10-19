## Libraries

### Language Libraries

Official libraries for common programming languages, like PHP, Python etc.

| Language   | Status      | Link                                                  | Package Manager                                             |
| ---------- | ----------- | ----------------------------------------------------- | ----------------------------------------------------------- |
| Javascript | Released    | [tomba-io/node](https://github.com/tomba-io/node)     | [tomba](https://www.npmjs.com/package/tomba)                |
| Ruby       | Released    | [tomba-io/ruby](https://github.com/tomba-io/ruby)     | [tomba](https://rubygems.org/gems/tomba)                 |
| Python     | Released    | [tomba-io/python](https://github.com/tomba-io/python) | [tomba-io](https://pypi.org/project/tomba/)                 |
| PHP        | Released    | [tomba-io/php](https://github.com/tomba-io/php)       | [tomba-io/php](https://packagist.org/packages/tomba-io/php) |
| Go         | In progress | [tomba-io/go](https://github.com/tomba-io/go)         |                                                             |
| Java       | In progress | [tomba-io/java](https://github.com/tomba-io/java)     |                                                             |
| Perl       | In progress | [tomba-io/perl](https://github.com/tomba-io/perl)     |                                                             |
| Dart       | In progress | [tomba-io/dart](https://github.com/tomba-io/dart)     |                                                             |
| Rust       | In progress | [tomba-io/rlang](https://github.com/tomba-io/rlang)   |                                                             |
| R          | In progress | [tomba-io/rlang](https://github.com/tomba-io/rlang)   |                                                             |

### Framework Libraries

Official libraries for common frameworks. These libraries should use the official lanaguge library as a dependency, so for example the Django library should use the Python library.

In the framework libraries we can assume more about the developer's use case, and we probably have access to more information, such as a HTTP request object. We can therefore implement additional functionality that
doesn't make sense in the core language library. This includes bot filtering (not sending requests to our API if the user agent belongs to a "bot").
