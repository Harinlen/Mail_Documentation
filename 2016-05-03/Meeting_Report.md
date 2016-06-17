#Meeting minutes from Kreogist Dev Team meeting 03.5.2016
03, May, 2016

Solution to the scroll bar problems mentioned in the last meeting. We decide to use the auto hide scroll bar.

The contact area may contains a long list (mentioned by Kyle). The super long list in a discussion group. In this situation, our previous design won't support the solution. Add the scorll bar in the contact area for more than four lines of contacts.

Add the scorll bar in the user list.

Emerge the web engine problems. We design an abstract class for the rendering area. The Webkit module and WebEngine module are design to be a plugin of the port. Using macros to decide with module should be used according to the Qt version. The major version of Qt must be 5. When we are using a minor version which is later than 6 (including 6), we will use the Qt WebEngine part. When we are using a minor version lower than 6 (excluding 6), we will use Qt WebKit module. For 32-bit version, we will only use Qt 5.5.1 to compile the 32-bit Windows version. On Mac OS X and Linux, we will use WebEngine module.
