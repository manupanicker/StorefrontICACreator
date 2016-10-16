# Storefront ICA file creator

Tested with Storefront 3.6

Version: 0.8

Date: 7-20-16

## Changelog:

7-26-16: Added PowerShell script for accessing authenticated store 

10-16-16 : Removed get-ICAfile_v3_auth.ps1 from branch master and moved to auth while troubleshooting.  Not working with recent release of Storefront.

[See blog for more information.](http://techdrabble.com/citrix/21-create-an-ica-file-from-storefront-using-powershell-or-javascript)

## Requirements
* For PowerShell v3 must be installed
* Unauthenticated StoreFront Store must be created for JavaScript
* Anonymous Delivery Group must be created for JavaScript

## Powershell v3 
Uses PowerShell web requests to create, download and launch a Citrix ICA file via an unauthenicated or authenticated Storefront URL.  Currently uses PowerShell v3.

`.\get-ICAfile_v3.ps1 -unauthurl "https://storefront.mydomain.local/Citrix/unauthWeb/" -appname "Notepad++" -icapath "C:\temp\myica.ica"`

## Javascript
Uses XMLHTTP request and JSON2 to create and download a Citrix ICA file via an unauthenicated Storefront URL

`<button onclick="starticaurl('https://storefront.mydomain.local/Citrix/unauthWeb/', 'Notepad++')">Launch App</button>`
