## Libraries

### Language Libraries

Official libraries for common programming languages, like PHP, Python etc.

| Language   | Status      | Link                                                  | Package Manager |
| ---------- | ----------- | ----------------------------------------------------- | --------------- |
| Javascript | In progress | [tomba-io/node](https://github.com/tomba-io/node)     |                 |
| Go         | In progress | [tomba-io/go](https://github.com/tomba-io/go)         |                 |
| Java       | In progress | [tomba-io/java](https://github.com/tomba-io/java)     |                 |
| Python     | In progress | [tomba-io/python](https://github.com/tomba-io/python) |                 |
| PHP        | In progress | [tomba-io/php](https://github.com/tomba-io/php)       |                 |
| Ruby       | In progress | [tomba-io/ruby](https://github.com/tomba-io/ruby)     |                 |
| Perl       | In progress | [tomba-io/perl](https://github.com/tomba-io/perl)     |                 |
| Dart       | In progress | [tomba-io/dart](https://github.com/tomba-io/dart)     |                 |
| Rust       | In progress | [tomba-io/rlang](https://github.com/tomba-io/rlang)   |                 |
| R          | In progress | [tomba-io/rlang](https://github.com/tomba-io/rlang)   |                 |

### Framework Libraries

Official libraries for common frameworks. These libraries should use the official lanaguge library as a dependency, so for example the Django library should use the Python library.

In the framework libraries we can assume more about the developer's use case, and we probably have access to more information, such as a HTTP request object. We can therefore implement additional functionality that
doesn't make sense in the core language library. This includes bot filtering (not sending requests to our API if the user agent belongs to a "bot").

### Third party libraries

There are a large number of unofficial tomba-io libraries written by third parties. While these aren't maintained by us and haven't been tested by us these libraries can be a great way to get started quickly with tomba-io if you're using a language or framework that we don't have an official library for. Search GitHub for [tomba-io](https://github.com/search?q=tomba-io) libraries.

If you’ve written a tomba-io library and would like to add it to this page, send an email to info@tomba.io.
