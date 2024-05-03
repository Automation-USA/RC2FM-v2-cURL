# RC2FM2-cURL
RC2FM2-cURL is a free and open-source ***complete re-write*** of our server-side [RingCentral app](https://t.co/XzKvvUs3A9) integration for the Claris FileMaker platform that we are releasing as fully open-source.
 
We have ported all of the backend PHP code for [RC2FM Connector](https://www.rc2fm.com) into 100% native FileMaker scripts and cURL commands, making the functionality of our RingCentral™ API integration available as open source for all FileMaker users to use. All you require is a RingCentral® subscription, a free RingCentral® [developer account](https://developers.ringcentral.com/sign-up), and your own RingCentral [integration app](https://developers.ringcentral.com/guide/getting-started/register-app).

**Features**
- Compatible with RingCentral's [JWT authentication flow](https://developers.ringcentral.com/guide/authentication/jwt-flow).
- 100% FileMaker native (fully commented scripts, cURL requests, and FileMaker tables).
- Unified logs FileMaker table consolidates RingCentral call log and message log schema.
- Test scripts show you how to call the APIs that make the magic work.
- Full feature parity with our (now retired) commercial product:
  -  RingOut outbound call support
  -  SMS/MMS outbound message support
  -  FaxOut outbound faxing support
  -  Call Log history downloading
     - Call recording attachment downloading
  -  Message Log history (SMS, MMS, Fax) downloading
     - Message attachment downloading
- JSON parsing and scripted inserting of RingCentral data into FileMaker records