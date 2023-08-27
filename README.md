# My Maven Archetypes

Maven [archetypes](https://maven.apache.org/archetype/index.html) are project
templates, and they are supposed to make creating a new project easier.
Unfortunately, unlikely the project templates provided by IDEs, the
official Maven templates (e.g. `quickstart`, `webapp`) are quite barebone
and almost never get updated for new versions of JDK or Java EE.

This repository contains the archetypes I created for myself and the classes
I teach:

- `simple-servlet-archetype`: a web application with a single servlet and
  an index page with a link to the servlet. Use Servlet 4.0 and JDK 17.

These archetypes are *not* in Maven Central as the process to publish them
there is quite complicated. To use these archetypes, first clone this
repository, then run `mvn install` to install the archetypes into the local
catalog.