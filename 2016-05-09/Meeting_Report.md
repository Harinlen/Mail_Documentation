#Meeting minutes from Kreogist Dev Team meeting 09.5.2016
09, May, 2016

Main topic of this week is to make the unibar start to work.

The folders, for instance your inbox, draft box and trash box in the E-mail account, will be treated as a single model. All the data will be presented and managed via the MVC (Model-View-Controller) architectural pattern. The View widget is a list view with a special delegate class installed. And the model is already design in the previous process.

We are now having a user account module which supports for multiple folders which could also record the information of the E-mail account, including:

6. Username
2. Password
7. Nickname
3. Sending protocol and its settings, e.g. port number and Transport Layer Protocol.
4. Receiving protocol and its settings.

Set up the individual account backend (personal informations).

Save the settings in the user configuration file using JSON format. The data is not encrypted via the whole development process. In the release, the data will be encrypted using 256-bit AES.

Fixed unibar button bugs.

