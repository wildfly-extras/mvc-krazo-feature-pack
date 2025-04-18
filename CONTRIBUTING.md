:toc:

= Contributing Guide

Want to contribute to the WildFly MVC Krazo Feature Pack? We try to make it easy, and all contributions, even the smaller ones,
are more than welcome. This includes bug reports, fixes, documentation, etc. First though, please read this page
(including the small print at the end).

== Legal

All original contributions to the WildFly MVC Krazo Feature Pack are licensed under the
https://repository.jboss.org/licenses/apache-2.0.txt[Apache License Version 2.0], or, if another
license is specified as governing the file or directory being modified, such other license.

All contributions are subject to the https://developercertificate.org/[Developer Certificate of Origin (DCO)].
The DCO text is also included verbatim in the [dco.txt](dco.txt) file in the root directory of the repository.

== Reporting an issue

This project uses https://github.com/wildfly-extras/mvc-krazo-feature-pack/issues[GitHub issues] for filing issues.

If you believe you found a bug, and it's likely possible, please indicate a way to reproduce it, i.e. what you are seeing and what you would expect to see.

== Before you contribute

To contribute, use GitHub Pull Requests, from your **own** fork.

Also, make sure you have set up your Git authorship correctly:

----
git config --global user.name "Your Full Name"
git config --global user.email your.email@example.com
----

If you use different computers to contribute, please make sure the name is the same on all your computers.

We use this information to acknowledge your contributions in release announcements.

== Setup

If you have not done so on this machine, you need to:

* Install Git and configure your GitHub access
* Install Java SDK 11+ (OpenJDK recommended)

=== IDE Config and Code Style

The WildFly Arquillian Adapter has a strictly enforced code style. Code formatting is done by the Eclipse code formatter,
using the config files found in the
https://github.com/wildfly/wildfly-dev-tools/tree/main/ide-config/src/main/resources[eclipse-code-formatter.xml]
file. By default, when you run `./mvnw install`, the code will be formatted automatically. When submitting a pull
request the CI build will fail if running the formatter results in any code changes, so it is recommended that you
always run a full Maven build before submitting a pull request.

If you want to run the formatting without doing a full build, you can run `./mvnw process-sources`.

==== Eclipse Setup

Open the *Preferences* window, and then navigate to _Java_ -> _Code Style_ -> _Formatter_. Click _Import_ and then
select the `eclipse-code-formatter.xml` downloaded from the above link or clone the repository and navigate to the file.

Next navigate to _Java_ -> _Code Style_ -> _Organize Imports_. Click _Import_ and select the `eclipse.importorder` file.

==== IDEA Setup

Install the https://plugins.jetbrains.com/plugin/6546-adapter-for-eclipse-code-formatter/[Adapter for Eclipse Code Formatter].
See the https://github.com/krasa/EclipseCodeFormatter#instructions[documentation] on how to configure the plugin.