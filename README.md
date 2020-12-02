# The Default BC Templates
The BigCommerce default email templates. Somehow someone forgot to either offer a reset button or repository with them.

Want to thank me? 
Leave a like to https://www.facebook.com/riCompro :)

# Hirachy of Templates and Snippets

##Templates
### abandoned_cart_email.html (Enterprise only)
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

### Invoice
|->	%%GLOBAL_NoPaymentTaken%% (Snippet)
	|-> %%GLOBAL_NoPaymentTakenModuleInTestMode%% (Global Variable)
|->	%%GLOBAL_OrderNumber%% (Global Variable)
|->	%%GLOBAL_ViewOrderStatusMsg%% (Global Variable)
|->	%%GLOBAL_Mandate%%  (Global Variable)
|-> %%GLOBAL_PendingPaymentNotice%%
|-> %%GLOBAL_ShippingAddress%%
|-> %%GLOBAL_HideShippingEmail%%
|-> %%GLOBAL_ShippingEmail%%
|-> %%GLOBAL_BillingAddress%%</div>
|-> %%GLOBAL_HideBillingEmail%%
|->	%%GLOBAL_PendingPaymentDetails%%
|-> %%GLOBAL_OrderCommentBlock%%
|-> %%GLOBAL_CartItemColumns%%
|-> %%SNIPPET_CartItems%%
|-> %%SNIPPET_TotalRows%%
|-> %%SNIPPET_PaymentMethod%%
|-> %%GLOBAL_EmailFooter%%

# Variables

## Truely Global (works everywhere)
%%GLOBAL_ShopPathNormal%% - URL with http (use %%GLOBAL_ShopPathSSL%%)
%%GLOBAL_ShopPathSSL%% - URL with https
%%GLOBAL_StoreDomainName%% - URL of your Store
%%GLOBAL_StoreName%% - Name of the Store

## Text Strings
%%LNG_AC_ContactDetailsSubheading%%	 = "Contact Details"
%%LNG_InvoicePendingPaymentText%% = "Your order requires payment before it can be finalized. Details on how to pay are shown below."
## Customer
%%GLOBAL_CustomerName%% > Customer Full Name
%%GLOBAL_ChangedCustomerFields%% > Array of Changes to a customer
%%FIRSTNAME%% * To be tested

## Cart (Abandoned Cart)
%%CARTCONTENTS%% (Snippet)
%%COUPONCODEBOX%% (Snippet)
%%CHECKOUTLINK%% (Global Variable)