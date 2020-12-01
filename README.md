# The Default BC Templates
The BigCommerce default email templates. Somehow someone forgot to either offer a reset button or repository with them.

Want to thank me? 
Leave a like to https://www.facebook.com/riCompro :)

# Hirachy of Templates and Snippets

##Templates
abandoned_cart_email.html (Enterprise only)
|-> %%FIRSTNAME%% (Gobal Variable)
|->	%%GLOBAL_AC_EmailBody%% (Snippet)
|-> %%CHECKOUTLINK%% (Gobal Variable)
	|-> %%CARTCONTENTS%% (Snippet)
		|	Line Items of Cart
		|-> %%GLOBAL_ProductUrl%% (Global Variable)
		|-> %%GLOBAL_HideThumbnail%% (Global Variable)
		|-> %%GLOBAL_ProductThumbnailUrl%% (Global Variable)
		|-> %%GLOBAL_ProductName%% (Global Variable)
		|-> %%GLOBAL_ProductQuantity%% (Global Variable)
		|->	%%GLOBAL_ProductAttributes%% (Global Variable)
	|-> %%COUPONCODEBOX%% (Snippet) 
|-> %%GLOBAL_EmailFooter%% (Snippet)
|-> %%GLOBAL_AC_UnsubscribeLink%% (Global Variable)

# Variables

## Truely Global (works everywhere)
%%GLOBAL_ShopPathNormal%% - URL with http (use %%GLOBAL_ShopPathSSL%%)
%%GLOBAL_ShopPathSSL%% - URL with https
%%GLOBAL_StoreDomainName%% - URL of your Store
%%GLOBAL_StoreName%% - Name of the Store

## Text Strings
%%LNG_AC_ContactDetailsSubheading%%	 = "Contact Details"

## Customer
%%GLOBAL_CustomerName%% > Customer Full Name
%%GLOBAL_ChangedCustomerFields%% > Array of Changes to a customer
%%FIRSTNAME%% * To be tested

## Cart (Abandoned Cart)
%%CARTCONTENTS%% (Snippet)
%%COUPONCODEBOX%% (Snippet)
%%CHECKOUTLINK%% (Global Variable)