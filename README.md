# MediaKit 
 - A work-in-progress concept for streaming media development and presentation
 - A document object model to describe inter-connected media streaming components
 - This project is in a conceptual / research stage

###### This project serves 
 - to provide an initial specification of the media document object model
 - to organise and store research notes and links useful projects
 - to provide a set of necessary proof-of-concepts

###### Reference projects 
- Chromium / Chromium Embedded Framework CEF
    - Chromium 
        - https://www.chromium.org
    - CEF 
        - https://bitbucket.org/chromiumembedded/cef/overview
    - CEF3-based application shell for Brackets
        - https://github.com/adobe/brackets-shell  
        - http://brackets.io
    - interoperability between javascript in browser view and native code
        - https://bitbucket.org/chromiumembedded/cef/wiki/JavaScriptIntegration 
- V8 
    - Javascript engine from google
    - https://code.google.com/p/v8/
    - https://developers.google.com/v8/embed
- C8 
    - MACOSX: A bridge between Objective-C and Google's V8 Javascript engine  
    - Somewhat outdated but still useful as a reference
    - https://github.com/Grayson/c8
- FreeFrameGL 
    - http://freeframe.sourceforge.net/
- Syphon (inter-application frame sharing libraries)
    - http://syphon.v002.info/

 
###### Media Document Object Model (MDOM)
 - Describes an acyclic graph of interconnected media components, and the properties of each component.
 - Example
    - audio source(s)  ==> audio mixer ==> audio output(s)
    - audio generator(s) ==> audio mixer ==> audio output(s)
    - video source --> video effect --> video mixer --> video output

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
 - Decouple component processing thread from user interface thread
    - component processing to be done in native code.
    - component user interface to be faciliated by via html5/ javascript via chromium.
 - Use chromium embedded framework for HTML/Javascript module user interfaces
 - Use V8 javascript engine to create and connect modules, expose Document Object Model of all components including sequencer, mixer channels, modules, module parameters... 

##### Future : 
###### Long term objectives:
 - Media Transfer Protocol: introduce p:// protocol for distributed / collaborative media streaming development
 - Browser: implement a browser client with view source access to document object model 
 - Protocol Daemon: implement a server
###### Media Transfer Protocol
 - tpc protocol to relay information between the client and server to facilitate interaction 
 
