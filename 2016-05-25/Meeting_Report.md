#Meeting minutes from Kreogist Dev Team meeting 25.5.2016
25, May, 2016

The application now could already manage one single application. We have to design for the future. We design a multi-account management system, but now it will only be used for managing single account.

The managing class will support the following basic operations of an E-mail account list:

- Add a new account class to the list.
- Remove an existing account in the list.

The update operation will be done by the account class itself. This function won't be included in the management class.

Add signals for switching the models. And the left bar is now working with different models.

Fullfil the functions of inbox, draft, etc.

Do another code review. Fixed the following outstanding bugs:

1. Fixed the rvalue reference supporting bug in the QPixmap class. The code is using normal (lvalue) reference but we want rvalue reference.
2. Fixed the color is not correct under Mac OS X. Because the palette settings cannot be implemented from the parent widget under Mac OS X. We add the specific settings of the widget in the theme file.