# RC2FM2-cURL
RC2FM2-cURL is a free and open-source ***complete re-write*** of our server-side [RingCentral app](https://t.co/XzKvvUs3A9) integration for the Claris FileMaker platform that we are releasing as fully open-source.
 
We have ported all of the backend PHP code for [RC2FM Connector](https://www.rc2fm.com) into 100% native FileMaker scripts and cURL commands, making the functionality of our RingCentral™ API integration available as open source for all FileMaker users to use. All you require is a RingCentral® subscription, a free RingCentral® [developer account](https://developers.ringcentral.com/sign-up), and your own RingCentral [integration app](https://developers.ringcentral.com/guide/getting-started/register-app).

**Features**
- Compatible with RingCentral's [JWT authentication flow](https://developers.ringcentral.com/guide/authentication/jwt-flow).
- :100:**FileMaker native** (fully commented scripts, cURL requests, and FileMaker tables).
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

**What's *not* included**
- No 'look-and-feel' UI (no custom layout themes, menus, buttons, etc). Feel free to design your own interface to match the look of your FileMaker application(s).
- No oAuth authentication support. Only [JWT authentication flow](https://developers.ringcentral.com/guide/authentication/jwt-flow) is supported.
- No technical support. As open-source code, you have entire developer communities to help you on either side of the [FileMaker](https://community.claris.com/) and [RingCentral](https://community.ringcentral.com/spaces/8/index.html) equation.

**Note:**
No Generative pre-trained transformers (GPTs) were hurt during the writing of this code. This repository consists of :100: human-powered developement :slightly_smiling_face: 

**Getting Started**
1. [Set up a RingCentral developer account](https://developers.ringcentral.com/sign-up).
2. [Register a REST API app](https://developers.ringcentral.com/guide/getting-started/register-app).
3. Download and open our '[RC2FM2_cURL.fmp12](https://github.com/Automation-USA/RC2FM-v2-cURL/blob/main/RC2FM2_cURL.fmp12)' FileMaker artifact (requires [Claris FileMaker](https://www.claris.com/filemaker/) version 18+).
4. Set up your RC2FM2 environment:
   -  All API environment configurations are managed from a single FileMaker procedure: ['[Function]__Init__RingCentral.API.Environment( )'](https://github.com/Automation-USA/RC2FM-v2-cURL/blob/main/API/Public/1_AT-STARTUP/%5BFunction%5D__Init__RingCentral.API.Environment(%20).txt). You need to copy/paste the following RingCentral credentials:
      - $appKey (Your RingCentral app key)
      - $appSecret (Your RingCentral app secret) 
      - $$jwt (A user's JWT token, obtained by visiting https://developers.ringcentral.com/console/my-credentials/create?client_id=<YOUR RINGCENTRAL API-APP ID [AKA CLIENT ID]>).
5. Test. Run some of the unit tests, starting with the 'SESSION-TESTS'