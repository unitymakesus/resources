# Install SSL Certificate with Cloudflare

## In website's cPanel

1. Scroll to ‘Security’, click on ‘SSL TLS’
2. Click ‘Generate, View, Uploader, Delete or Private Keys’
3. Generate private key
4. Scroll to bottom, click ‘Return to SSL Manager’
5. Click ‘CSR’ from SSL manager
6. Generate key, fill out the required fields
7. Copy all encrypted text

## In CloudFlare

1. Go to Crypto > Origin Certificates and click ‘Create Certificate’
2. Select ‘I have my own private key in CSR’, paste
3. Click ‘Next’ to get ‘Origin Certificate’
4. On next page copy ‘Origin Certificate’
5. Click ‘OK’

## Back in cPanel

1. Scroll to bottom of page and click ‘Return to SSL Manager’
2. Click on ‘Certificates (CRT)’
3. Paste certificate in the box, then click ‘Save’
4. Click ‘Go Back’
5. Scroll to bottom of page, click ‘Back to SSL Manager’
6. Click ‘Install And Manage’ in SSL Manager
7. Click ‘Browse Certificates’ blue button
(Use the certificate you recently installed, it may be the only one, it will probably be highlighted and on the top of the que)
8. Click ‘Yes’
SELECT THE CORRECT DOMAIN NAME IN THE DROPDOWN
(If CS bundle is not there with all the characters, alisa sent a slack message with stuff
Scroll down and click install blue button)

ALMOST DONE!

## Back in CloudFlare Crypto
1. Set SSL to ‘full’ or ‘flexible’
2. Make sure ‘edge certificates’ is not empty.

DONE.
