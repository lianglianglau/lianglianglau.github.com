---
layout: post
category: Eclipse
tagline: "Supporting tagline"
tags: [Eclipse]
---
{% include JB/setup %}

create an eclipse executable

input this:

> sudo touch /usr/bin/eclipse
> sudo chmod 755 /usr/bin/eclipse
> sudoedit /usr/bin/eclipse

With this contents

> #!/bin/sh
> #export MOZILLA_FIVE_HOME="/usr/lib/mozilla/"
> export ECLIPSE_HOME="/opt/eclipse"

> $ECLIPSE_HOME/eclipse $*

Then create a gnome menu item

> [Desktop Entry]
> Encoding=UTF-8
> Name=Eclipse
> Comment=Eclipse IDE
> Exec=eclipse
> Icon=/opt/eclipse/icon.xpm
> Terminal=false
> Type=Application
> Categories=GNOME;Application;Development;
> StartupNotify=true

Then ,you can run eclipse in your ubuntu.
