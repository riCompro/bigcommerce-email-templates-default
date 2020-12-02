# The Default BC Templates
The BigCommerce default email templates. Somehow someone forgot to either offer a reset button or repository with them.

Want to thank me? 
Leave a like to https://www.facebook.com/riCompro :)

# Hirachy of Templates and Snippets

## Templates
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


### Account Details have changed
|-> %%GLOBAL_CustomerName%%  
|-> %%GLOBAL_CustomerName%%  
|-> %%GLOBAL_ChangedCustomerFields%%  

### Combined Order Status email
|-> %%GLOBAL_OrderStatusChangedHi%%
|-> %%GLOBAL_OrderNumberStatusChangedTo%%  
|-> %%GLOBAL_OrderTotal%%  
|-> %%SNIPPET_RefundedAmountRow%%  
|-> %%GLOBAL_DatePlaced%%  
|-> %%GLOBAL_PaymentMethod%%  
|-> %%SNIPPET_ShippedItems%%  
|-> %%SNIPPET_ToBeShippedItems%%  
|-> %%SNIPPET_ShipmentTracking%%  
|-> %%SNIPPET_DownloadableItems%%  
|-> %%GLOBAL_ViewOrderStatusLink%%  
|-> %%GLOBAL_EmailFooter%%  

## createaccount_email
|-> %%GLOBAL_FirstName%%  
|-> %%GLOBAL_StoreName%%  
|-> %%GLOBAL_Email%%  
|-> %%GLOBAL_Password%%  
|-> %%GLOBAL_ShopPathNormal%%  
|-> %%GLOBAL_StoreName%%  
|-> %%GLOBAL_ShopPathNormal%%  
|-> %%GLOBAL_EmailFooter%%  

## createguestaccount_email
|-> %%GLOBAL_FirstName%%  
|-> %%GLOBAL_StoreName%%  
|-> %%GLOBAL_NewGuestAccountResetLink%%
|-> %%GLOBAL_NewGuestAccountResetLink%%
|-> %%GLOBAL_ShopPathNormal%%
|-> %%GLOBAL_StoreName%%
|-> %%GLOBAL_ShopPathNormal%%
|-> %%GLOBAL_EmailFooter%%

## giftcertificate_email
|-> %%GLOBAL_ToName%%  
|-> %%GLOBAL_Intro%%  
|-> %%GLOBAL_ExpiryInfo%%  
|-> %%GLOBAL_GiftCertificateRedeemLink%%  
|-> %%GLOBAL_EmailFooter%%  


### Invoice
|->	%%GLOBAL_NoPaymentTaken%% (Snippet)  
	|-> %%GLOBAL_NoPaymentTakenModuleInTestMode%% (Snippet)  
|->	%%GLOBAL_OrderNumber%% (Global Variable)  
|->	%%GLOBAL_ViewOrderStatusMsg%% (Global Variable)  
|->	%%GLOBAL_Mandate%%  (Global Variable)  
|-> %%GLOBAL_PendingPaymentNotice%%  
|-> %%GLOBAL_ShippingAddress%%  
|-> %%GLOBAL_HideShippingEmail%%  
|-> %%GLOBAL_ShippingEmail%%  
|-> %%GLOBAL_BillingAddress%%  
|-> %%GLOBAL_HideBillingEmail%%  
|-> %%GLOBAL_BillingEmail%%  
|->	%%GLOBAL_PendingPaymentDetails%%  
|-> %%GLOBAL_OrderCommentBlock%%   
|-> %%GLOBAL_CartItemColumns%%   
|-> %%SNIPPET_CartItems%%  
|-> %%SNIPPET_TotalRows%%  
|-> %%SNIPPET_PaymentMethod%%  
|-> %%GLOBAL_EmailFooter%%  

### ordermessage_notification.html
|->	%%GLOBAL_StoreName%%
|->	%%GLOBAL_OrderMessageFromMerchant%%  
|->	%%GLOBAL_OrderMessageFromMerchant%%  
|->	%%GLOBAL_ShopPathSSL%%  
|->	%%GLOBAL_EmailFooter%%  

### passwordless_login_email.html
|->	%%GLOBAL_SignIn_Link%%
|->	%%GLOBAL_EmailFooter%%
|->	%%GLOBAL_StoreName%%  

### product_review_email.html
|->	%%SNIPPET_ProductReviewItems%%  
|->	%%GLOBAL_EmailFooter%%  
|->	%%GLOBAL_ProductReviewEmailUnsubscribeStyle%%  
|->	%%GLOBAL_ProductReviewEmailUnsubscribeLink%%  

### return_confirmation_email.html
|->	%%GLOBAL_ShopPath%%
|->	%%GLOBAL_ReturnReason%%
|->	%%GLOBAL_ReturnAction%%
|->	%%GLOBAL_ReturnComments%%
|->	%%SNIPPET_ReturnItems%%
|->	%%GLOBAL_EmailFooter%%

### return_statuschange_email.html
%%GLOBAL_CustomerFirstName%%
%%GLOBAL_ProductQuantity%%
%%GLOBAL_ProductName%%
%%GLOBAL_ReturnStatus%%
%%GLOBAL_ReturnReceivedCredit%%
%%GLOBAL_ReturnInstructions%%
%%GLOBAL_ShopPath%%
%%GLOBAL_EmailFooter%%

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
%%GLOBAL_ChangedCustomerFields%% > Array of Changes to a customer, only on Account Details have changed email
%%FIRSTNAME%% * To be tested
%%GLOBAL_ChangedCustomerFields%% > Array of Field Labels changed (only in context of )
%%GLOBAL_ResetPasswordLink%% > Link to reset passwords

## Cart (Abandoned Cart)
%%CARTCONTENTS%% (Snippet)
%%COUPONCODEBOX%% (Snippet)
%%CHECKOUTLINK%% (Global Variable)