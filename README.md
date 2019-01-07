# Zendesk Guide Redirection

## Summary
Currently there is no way to redirect Zendesk Guide articles using a 301 redirect. 

While this a 301 is the right way to forward a URL, it is currently not an option for Zendesk Guide users. In certain instances, however, redirection is still necessary for education, content availability, and a positive end user experience.

The JS script contained in this repository provides a workaround to redirect end users from archived Zendesk Guide articles to either a new article or a new URL altogether.

## Usage Instructions
There are several steps that must be taken in order to redirect.
 
 1. If redirecting from a Zendesk Guide article to another Zendesk Guide article, collect both of those article IDs. If redirecting from a Zendesk Guide article to an external URL, collect the old Zendesk Guide ID and the external URL.
 
     • The Article ID can be gathered from the URL of the article
 
 2. Edit the JavaScript Snippet. 
 
     • Replace "YOURSUBDOMAIN" with your Zendesk Guide subdomain. For example, "help.scottsupport.com" or .    "support.scottcompany.com". This should ultimately match the URL of the Zendesk Guide help center.
     
     • If redirecting from a Guide article to another Guide article, place the old article id and the new article id in the hash table as specified in the code comment.
     
     • If redirecting from a Guide article to an external URL, place the old article id in the hash table, and the newExternalURL variable as specified in the code comment.
     
     • Place this snippet in `<script>` tags in the `<head>...</head>` section of the Help Center code. This is likely in document_head.hbs.
     
3. Adding additional redirects requires adding any old/new article ID's or external URLs to the hash table, and pushing the updated code live. 
 
 
 
