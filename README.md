# Eclipse aCute: C# in Eclipse IDE

Support for C# editing in Eclipse IDE. Relies on OmniSharp and Language Server Protocol.

aCute is an Eclipse.org project. See https://projects.eclipse.org/projects/tools.acute .

[Video Demo of Editor and .NET Core Commands Integration](https://www.dropbox.com/s/yc60dsoslv0hedd/aCute.mp4)

![screenshot](aCute.png "Screenshot of aCute editor")

## Prerequisites

* On **any OS**, `node` and `dotnet`(v2.0 or later) needs to be available in your PATH.
* On **Windows**, .NET SDK needs to be installed.
* On **Mac**: Unknown. If you discover an issue or required prerequisite, please [report the issue.](https://github.com/eclipse/aCute/issues)

Or see [Alternative server setup](#alternative-server-setup)

## Installation in Eclipse IDE

Using Eclipse Marketplace: https://marketplace.eclipse.org/content/acute-c-edition-eclipse-ide-experimental

Using p2 repository: use `http://repository.jboss.org/nexus/content/unzip/unzip/org/eclipse/acute/repository/0.1.0-SNAPSHOT/repository-0.1.0-SNAPSHOT.zip-unzip/` in the [Install New Software wizard](http://help.eclipse.org/topic/org.eclipse.platform.doc.user/tasks/tasks-127.htm)

## Concept

aCute uses the [lsp4e](https://projects.eclipse.org/projects/technology.lsp4e) project to integrate with [OmniSharp Language Server](https://github.com/OmniSharp/omnisharp-node-client) and [TM4E](https://projects.eclipse.org/projects/technology.tm4e) project to provide syntax highlighting in order to provide a rich C# editor in the Eclipse IDE.

## Alternative server setup

You can setup a local [OmniSharp Language Server](https://github.com/OmniSharp/omnisharp-node-client) fetched, configured and working locally. Then at least one of the following *environment variables* should be set to make Eclipse IDE able to locate your specific OmniSharp-node-client:
* `OMNISHARP_LANGUAGE_SERVER_COMMAND`: a command-line to start omnisharp-node-client (such as `/usr/bin/node /home/mistria/git/omnisharp-node-client/languageserver/server.js`)
* `OMNISHARP_LANGUAGE_SERVER_LOCATION`: the location when omnisharp-node-client is installed (such as `/home/mistria/git/omnisharp-node-client`).

Note that this approach isn't recommended nor supported by the aCute project developers. It's mainly useful for contributors who want to hack things around Omnisharp-node-client and/or aCute.
