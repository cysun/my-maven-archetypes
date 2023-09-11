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
catalog. You can do this in Eclipse instead of from command line as described
in the next section.

## Install The Archetypes Using Eclipse

First, copy the repository URL `https://github.com/cysun/my-maven-archetypes.git` .

Then, in Eclipse, open Git perspective (Window -> Perspective -> Open Perspective -> Git).
Select `Clone a Git Repository`, then select `Clone URI` in the popup window:

![Screenshot of Select Repository Source](https://mynotes.cysun.org/files/view/1002393)

Click Next, and a popup window like the following would appear:

![Screenshot of Source Git Repository](https://mynotes.cysun.org/files/view/1002396)

The URI field should already be filled with the repository URL you copied
earlier; if not, you can simply paste it into the field yourself.

Click the Next button, then on the next screen, click the Next button again. On
the Local Destination screen (shown below), note down the directory where the
repository is going to be cloned to - you will import the projects from this
directory later.

![Screenshot of Local Destination Screen](https://mynotes.cysun.org/files/view/1002395)

Click the Finish button to clone the repository, then go back to Java EE
perspective (Window -> Perspective -> Open Perspective -> Java EE). From the
File menu, select Import -> Existing Maven Projects as shown below:

![Screenshot of Import Existing Maven Project](https://mynotes.cysun.org/files/view/1002394)

Click the Next button, and on the next screen, set Root Directory to the directory
where the repository was cloned to earlier.

![Screenshot of Select Maven Projects](https://mynotes.cysun.org/files/view/1002392)

Click the Finish button to import the projects. It will take Eclipse a little time
to complete the import (you can see the progress at the bottom right corner of
Eclipse).

After the projects are imported, right click on the `maven-archetypes` project in
the Project Explorer view, and select Run As -> Maven install. After a little
while (Maven will download lots of stuff on the first run), you should see
the build success message in the Console view like the following:

![Screenshot of Build Success](https://mynotes.cysun.org/files/view/1002397)

After the archetypes are installed, you can remove the `maven-archetypes` project
from Eclipse as it is no longer needed - right click on the project then select
Delete. In the popup window, make sure the `Delete nested project` option is checked
as shown in the screenshot below. You can leave the `Delete project contents on
disk` option unchecked in case you need to import the projects back into Eclipse
again.

![Screenshot of Delete Projects](https://mynotes.cysun.org/files/view/1002390)

## Use the Archetypes in Eclipse

In Eclipse, select File -> New -> Maven Project, then click Next. On the next
screen, select `Default Local` for Catalog, and you should see the archetypes
like `simple-servlet-archetype`.

![Screenshot of Archetype Selection](https://mynotes.cysun.org/files/view/1002389)