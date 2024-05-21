## Privacy Policy

This is intended as a simple summary of how the References app accesses and
uses your data. It is not intended as a legal document.

In short: References does the right thing by you as far as possible. It only
accesses the files and folders that you have asked it to, and you can easily
revoke this access at any time. It does not send any information to the
developer or other third parties, except for activities that are beyond its
control (see the end of this policy for some examples of these).

### BibTeX Libraries

The main purpose of the Reference app is for you to view your own BibTeX
libraries. The app will only read those libraries that you explicitly open
(e.g., by linking a BibTeX library on the main screen, or dragging a BibTeX
file into the app). It will store the locations of these libraries in the app
settings so that you can access your libraries again quickly from the main
screen. It will also search through all your linked libraries if you ask it to
(e.g., by clicking on an x-bdsk://citekey link).

The app does not send any information about your libraries, their contents, or
your searches, to any other apps or to any location off the device, unless you
have explicitly asked it to (e.g., by pressing the share button), or if this
is beyond the app's control (see the examples below).

### Folders for Attachments

A BibTeX library contains bibliographic references, and so the app allows you
to attach PDFs to these references (e.g., papers that you have downloaded).
The way you "attach" a PDF to a reference is by storing its location in a
special BibTeX field, such as _Files = {path/to/paper.pdf}_.

The References app allows you to view your PDF attachments from within the
app. To do this, you must explicitly grant the app access to the folder(s)
that contain your PDF attachments by linking a folder on the main screen. You
can easily revoke this access from the main screen by unlinking the folder.

The app will never attempt to open an attachment unless you explicitly ask it
to.

When you do open an attachment, the app will first need to locate it. To do
this, it will only look inside folders that you have explicitly linked, and
will only try locations within these folders that you have explicitly stored
in your BibTeX libraries. It may try several candidate locations (e.g., if you
link the folder _Papers_ and your BibTeX reference has
_Files = {Papers/foo.pdf}_ then the app will look for both
_Papers/foo.pdf_ and _Papers/Papers/foo.pdf_ before it gives up).

### Third-Party Cloud Providers (Dropbox, Google Drive)

You may prefer to store your PDF attachments on a third-party cloud provider,
such as Dropbox or Google Drive. You can link folders that are stored on these
third-party services, and you can easily revoke access to these folders,
following the same procedures as described above.

The app will access the service when you explicitly ask it to link a folder on
that service – it will offer you a file browser interface where you can choose
a folder to link. It will access the service again each time you try to open
an attachment, by attempting to locate your attachment(s) based on the folders
you have linked and the locations that you have stored in your BibTeX
libraries. These candidate locations will always stay inside the folders that
you have explicitly linked (possibly including subfolders).

Once the References app locates your attachment, it will download it to your
device and display it to you for reading. It will also keep a copy of the
attachment in its private cache on your device, so that you do not need to
download it again next time you wish to read it. You can clear the cache at
any time from the References settings panel.

### Activities Beyond Control

There are some activities beyond the app's control that may involve
transmitting your data to third parties. Examples might include (but are not
limited to):

- You backing up your own device to the cloud – this backup may include
  settings from the References app, such as which BibTeX libraries you
  currently have linked and which attachment folders you have currently
  granted access to.

- You clicking on a link in one of your own PDF documents – like any link on
  the Internet, this may leak information about where you clicked from.

- The App Store tracking download statistics, and (if you have opted to send
  diagnostics and usage information to Apple) usage statistics.

- Your cloud provider (e.g., Dropbox or Google Drive) tracking statistics on
  how frequently the app queries the cloud service.

If you have any questions, please contact the developer at bab at benburton.org.

