# Meeting minutes from Kreogist Dev Team meeting 18.3.2016
18, March, 2016

Qt released the latest verson on late 16, March, 2016. We checked out the change log of Qt 5.6. Focused on the core and network updates of the latest LTS version.

The biggest changes of the Qt 5.6 is that it no longer contains Qt Webkit module. It will be instead with the Qt WebEngine module. 

Advantages of using Qt WebEngine is that it could provide a better rendering pages than Qt Webkit. The Qt Webkit is based on the webkit engine released with the Safari Windows version. As we all know, the Windows version Safari doesn't get update for several years, it cannot provides a well present page. The Qt WebEngine is using Chromium project as the backend.

The disadvantages of using Qt WebEngine is that it doesn't support 32-bit MinGW version. Because you can only compile the Chromimum project using native compiler under the operating system. This will make the MinGW version Qt 5.6 cannot compile caused by lacking of the WebEngine. To solve this problem, we dicided to use Qt 5.5.1 to compile the 32-bit version binary using Qt WebKit module. That means we have to maintain two version using a abstract port for those solution. This problem is identified and we will expand the solution when we develop the specific module.   

We discussed how to use Github Desktop. Installed the plugin of git for Qt Creator. Set up the repository on all the developing machine.