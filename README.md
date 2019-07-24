# InstaMarlin
A configuration tool that will auto-generate Marlin binaries

## Overview
The idea of this tool, is to allow you to declare only the changes to Marlin that matter
to _you_, by using a GUI or a simple JSOn file, rather than cloning and managing your own fork.

### Why InstaMarlin

Marlin is an awesome project. There is one thing that has bothered me though, which is the need to maintain configuration
within the version controlled source, instead of that source being able to ingest external configuration. Let me expand on this
a bit.

Over the last few years, I've spent time working with infrastructure automation, and I've also spent time using 
Funcional Reactive Programming for software I've written.
The one thing that has been common among those two things is a declaritive approach to problem
solving. Declarative in this case means describing to the computer what you want to achieve,
as oppossed to describing to the computer how to achieve something (called an imperative approach). 

The typical procedure for building Marlin is to clone Marlin, and then modify header files to achieve
the configuration you desire. This seems like a smell to me. 

At the moment, _configuring_ Marlin feels very imperative to me. Every new merge request to Marlin requires you to
merge or rebase your own configuration, and this makes it very easy to introduce mistakes to your configuration
that can damage your hardware.

To me, the right approach would allow me to describe what changes my printer wants, and be able to apply _that_ to any version
of Marlin, and achieve the correct binary as a result.
