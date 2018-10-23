# ZeroToBlockchain Chapter 12: Creating, monitoring and consuming events

[Return to Table of Contents](../README.pdf)

In this chapter, we will update the code from Chapter 11 to include event creation and monitoring on the server and event subscription and notification in the browser.

```
Chapter 12
  ↳ controller
     ↳restapi
       router.js
        ↳features
           ↳composer
             autoLoad.js
             hlcAdmin.js
             hlcClient.js          <== Updated
             queryBlockChain.js
             Z2B_Services.js       <== Updated
             Z2B_Utilities.js
           ↳ text
               multi-lingual.js
               resources.js
  ↳ HTML
    index.html
    admin.html
    buyer.html                     <== Updated
    ceateConnectionProfile.html
    createMember.html
    createOrder.html
    deleteConnectionProfile.html
    financeCo.html                 <== Updated
    getMemberSecret.html
    removeMember.html
    provider.html                  <== Updated
    seller.html                    <== Updated
    shipper.html                   <== Updated
    singleUX.html
     ↳CSS
       pageStyles.css
     ↳js
       z2b-admin.js
       z2b-buyer.js                <== Updated
       z2b-events.js               <== Updated
       z2b-financeCo.js            <== Updated
       z2b-initiate.js
       z2b-provider.js             <== Updated
       z2b-seller.js               <== Updated
       z2b-shipper.js              <== Updated
       z2b-utilities.js
  ↳ network
   permissions.acl
   queries.qry
    ↳lib
      sample.js                    <== Updated
    ↳models
      base.cto
      events.cto
      sample.cto                   <== Updated
```
No new files are created.  Fifteen existing files are updated:

## Files used in this chapter
### Web Server Code Unique to this Chapter
 - **hlcClient.jss**
   - add event monitoring to client routines
   - add event notification to browser via web socket. 
     - it should be noted that this is a rough implementation for notifying the user of asynchronous events and is appropriate for a lightweight demo but inappropriate for a PoC or a production system. 

### Defining the business network
 
 - **/models/sample.CTO**
   - add events to sample.CTO file
 - **/lib/sample.js**
   - add event notification to transactions
 

### Web Browser Code 
 - **all UX files**
   - Add placeholder for notification icon and add placeholder for notification counter.
 - **all UX javascript files**
   - use subscribe, unsubscribe and notifyMe routines
 - **z2b-events.js**
   - add event support for alert subscription, notification
 - **CSS/pageStyles.css**
   - add support for notification icon and text