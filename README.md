# MediaKit 
 - A work-in-progress alternative to web pages for media applications.   
 - A document object model to describe inter-connected media streaming components.
 - This project is in a conceptual / research stage. 

###### This repository serves 
 - to provide a rough description of the media document object model
 - to provide a rough description of media transfer protocol
 - to organise research, notes and useful projects
 - to provide a set of necessary proof-of-concepts

###### Media Document Object Model (MDOM)
 - Describes an acyclic graph of interconnected media components, and the properties of each component.
 - Example
    - audio source(s)  ==> audio mixer ==> audio output(s)
    - audio generator(s) ==> audio mixer ==> audio output(s)
    - video source --> video effect --> video mixer --> video output

###### Media Transfer Protocol
 - tpc or udp protocol to relay information of the media document object model to facilitate interaction between the client and server
 - multicast or request/response?

###### Immediate objectives: 
 - c++ native application to allow media streaming components to interconnect in an acyclic graph.
    - Audio streaming / audiobuffer 
    - Video streaming / framebuffer 
    - Midi streaming / eventbuffer 
    - Parameter streaming / parameterbuffer
        - vectors
        - primatives
        - string
 - Expose media document object model to chromium window
    - html5 interface for viewing/editing graph of interconnected media components.
 - Decouple processing thread from user interface thread.
    - component processing to be done in native code.
    - component user interface to be faciliated by via html5/ javascript via chromium.
 - Components use native code for processing thread, while using chromium for displaying user interface. 
 - using Html and javascript for user interface for modules, while the modules and framework are implemented in native code.
 - Use chromium embedded framework for HTML/Javascript module user interfaces
 - Use V8 javascript engine to create and connect modules, expose Document Object Model of all components including sequencer, mixer channels, modules, module parameters... 

###### Intermediate objectives:
 - To provide a development & presentation enivronment for scriptable media streaming components

###### Long term objectives:
 - Hypermedia Transfer Protocol: introduce htp:// protocol for distributed / collaborative media streaming development
 - Browser: implement a browser client with view source access to document object model 
 - HTP Daemon: implement a server

###### Reference projects 
- CEF / Chromium
    - https://github.com/adobe/brackets-shell CEF3-based application shell for Brackets. http://brackets.io
* FreeFrameGL http://freeframe.sourceforge.net/
* Syphon http://syphon.v002.info/
* Chromium https://www.chromium.org/
* CEF https://bitbucket.org/chromiumembedded/cef/overview
