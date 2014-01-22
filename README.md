# EmailComposer with attachments handling

 Forked from https://github.com/phonegap/phonegap-plugins

 Installation:
 Add the plugin using Cordova's CLI:

	cordova plugin add httpshttps://github.com/cre80vty/CordovaEmailComposer.git 


Callable interface:

	window.plugins.emailComposer.showEmailComposerWithCallback(callback,subject,body,toRecipients,ccRecipients,bccRecipients,isHtml,attachments);

or

	window.plugins.emailComposer.showEmailComposer(subject,body,toRecipients,ccRecipients,bccRecipients,isHtml,attachments);

**ATTENTION:** the callback will never be triggered, it's here only for consistency with the iOS plugin

**Parameters:**
- callback: never used
- subject: a string representing the subject of the email; can be null
- body: a string representing the email body (could be HTML code, in this case set **isHtml** to **true**); can be null
- toRecipients: a js array containing all the email addresses for TO field; can be null/empty
- ccRecipients: a js array containing all the email addresses for CC field; can be null/empty
- bccRecipients: a js array containing all the email addresses for BCC field; can be null/empty
- isHtml: a bool value indicating if the body is HTML or plain text
- attachments: a js array containing all full paths to the files you want to attach; can be null/empty

**Example**

	window.plugins.emailComposer.showEmailComposerWithCallback(null,"Look at this photo","Take a look at <b>this<b/>:",["example@email.com", "johndoe@email.org"],[],[],true,["_complete_path/image.jpg", "_other_complete_path/file.zip"]);
