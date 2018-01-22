# Fix-ProxyAddress
## A small script with a GUI that simplifies the process of adding an SMTP proxy address to mailboxes that are not being updated by Exchange email address policies.

Are you migrating to Exchange Online? If so, you may come across the following error: "MigrationPermanentException: The target mailbox doesn't have an SMTP proxy matching 'company.mail.onmicrosoft.com'." This script was written to simplify the process adding an SMTP proxy address to mailboxes that are not being updated by Exchange email address policies. For more information about the error and use case,[please see this post on my blog.] (http://www.cgoosen.com/2014/11/migrationpermanentexception-the-target-mailbox-doesnt-have-an-smtp-proxy-matching-company-mail-onmicrosoft-com/)

Once launched, the script will prompt for your tenant routing domain in the format 'company.mail.onmicrosoft.com' and will search for all mailboxes in the organization that do not have an email address policy applied. A new SMTP proxy address will be added to all mailboxes without an email address policy. The proxy address will be based on the alias of the primary SMTP address and the routing domain entered, e.g if the primary SMTP address is john.smith@company.com and the routing domain entered is company.mail.onmicrosoft.com the resulting proxy address will be john.smith@company.mail.onmicrosoft.com.

**Requirements:**
This script has been tested and is known to work with Exchange 2010 and Exchange 2013.

**Usage:**
There are no parameters or switches, simply execute the script: .\Fix-ProxyAddress.ps1

**Screenshots:**

![alt text](https://www.cgoosen.com/wp-content/uploads/2014/11/script1.png)

![alt text](https://www.cgoosen.com/wp-content/uploads/2014/11/script2.png)

![alt text](https://www.cgoosen.com/wp-content/uploads/2014/11/script3.png)
