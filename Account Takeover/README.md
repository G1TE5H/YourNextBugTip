> Note: Some tips not work in modern websites, but for old websites you can try everything.

Payloads and Tips
=================
1. java`{“email”:[“victim@gmail.com”,”attacker@gmail.com”]}`
2. `email:victim mail%0d%0acc:hacker`
3. Forgot Password: The attacker changes the mobile number from victims to his mobile number and forwards the request. Token was attached with user
4. [For very old sites and program might accept it] Click [Reset Password] N times
    * If no csrf token then remove oldPassword param and value
    * you will get N links  
    * If first link still works  
    * Then issue as much as links possible  
    * Bruteforcing Token will be easy now. Isn't it?  
    * If there is no rate limit then B000M(Game Over)  
5. Host header on Password Reset Link  
6. Open Redirect, when token leak  
7. CSRF on password change  
8. Oauth Token leak to Acc takeover  

Write Ups
=========
* TR | Full Account Takeover via Reset Password Function
https://sametsahin.net/posts/account-takeover-via-reset-password/

* How re-signing up for an account lead to account takeover
https://medium.com/@zseano/how-re-signing-up-for-an-account-lead-to-account-takeover-3a63a628fd9f
    Submit user's email you wish to takeover.
    Grab id in response
    Visit the /api/create url and…. we’re in!

* Its all in the detail email leak account takeover thanks to waybackmachine extensive
https://medium.com/@zseano/its-all-in-the-detail-email-leak-account-takeover-thanks-to-waybackmachine-extensive-4be365580dd7

* Cross-Site Websocket Hijacking bug in Facebook that leads to account takeover
https://ysamm.com/?p=363

* Using CSRF I Got Weird Account Takeover
https://flex0geek.blogspot.com/2020/02/using-csrf-i-got-weird-account-takeover.html

* Badoo takeover
https://bugbountypoc.com/badoo-account-takeover/
    Steps to reproduce was :-
    1 -Create two Badoo account attacker & victim and link 2 diff fb account in each of them
    2- Login as ‘attacker’ and go to import photos via fb and copy the link from URL bar
    3- Now login as ‘victim’ in diffrent browser and open the link and click cancel.
    4- FB account of ‘victim’ is replaced with FB account of ‘attacker’ (Removed from ‘attacker’ one)
    5-Login via attacker’s FB account and you will be logged in as ‘victim’ account

* https://bugbountypoc.com/booking-token-issue/ [Tip 4]

* Bruteforcing
https://hackerone.com/reports/743545 $1000

* Simple Ones
===========
https://medium.com/@swapmaurya20/a-simple-idor-to-account-takeover-88b8a1d2ec24
