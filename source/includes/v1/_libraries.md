## Libraries

### Language Libraries

Official libraries for common programming languages, like PHP, Python etc.

| Language   | Status      | Link                                                  | Package Manager                                                  |
| ---------- | ----------- | ----------------------------------------------------- | ---------------------------------------------------------------- |
| Javascript | Released    | [tomba-io/node](https://github.com/tomba-io/node)     | [NPM package](https://www.npmjs.com/package/tomba)               |
| Ruby       | Released    | [tomba-io/ruby](https://github.com/tomba-io/ruby)     | [Ruby Gems](https://rubygems.org/gems/tomba)                     |
| R          | Released    | [tomba-io/r](https://github.com/tomba-io/r)           | [CRAN](https://cran.r-project.org/web/packages/tomba/index.html) |
| Dart       | Released    | [tomba-io/dart](https://github.com/tomba-io/dart)     | [Pub](https://pub.dev/packages/tomba)                            |
| Python     | Released    | [tomba-io/python](https://github.com/tomba-io/python) | [PyPi](https://pypi.org/project/tomba-io/)                       |
| PHP        | Released    | [tomba-io/php](https://github.com/tomba-io/php)       | [Packagist](https://packagist.org/packages/tomba-io/php)         |
| Deno       | Released    | [tomba-io/deno](https://github.com/tomba-io/deno)     | [Deno land](https://deno.land/x/tombaio)                         |
| C#         | Released    | [tomba-io/csharp](https://github.com/tomba-io/csharp) | [Nuget](https://www.nuget.org/packages/Tomba)                    |
| Rust       | Released    | [tomba-io/rust](https://github.com/tomba-io/rust)     | [crates.io](https://crates.io/crates/tomba)                      |
| Lua        | Released    | [tomba-io/lua](https://github.com/tomba-io/lua)       | [luarocks](https://luarocks.org/modules/benemohamed/tomba)                      |
| Elixir     | Released    | [tomba-io/elixir](https://github.com/tomba-io/elixir) | [hex.pm](https://hex.pm/packages/tomba)                          |
| Go         | In progress | [tomba-io/go](https://github.com/tomba-io/go)         | GitHub                                                           |
| Java       | In progress | [tomba-io/java](https://github.com/tomba-io/java)     | Maven Central                                                    |
| Perl       | In progress | [tomba-io/perl](https://github.com/tomba-io/perl)     | CPAN                                                             |

### Framework Libraries

Official libraries for common frameworks. These libraries should use the official language library as a dependency, so for example the Django library should use the Python library.

In the framework libraries we can assume more about the developer's use case, and we probably have access to more information, such as a HTTP request object. We can therefore implement additional functionality that
doesn't make sense in the core language library. This includes bot filtering (not sending requests to our API if the user agent belongs to a "bot").
