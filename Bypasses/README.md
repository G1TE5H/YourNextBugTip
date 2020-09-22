# Bypasses
## Rate Limit Bypass

*[Youtube's Video](https://youtu.be/it_V3ig1_4o) By [Assetnote](https://twitter.com/assetnote)*    
*Tool: [FireProx Repo](https://github.com/ustayready/fireprox) Created By Mike Felch [@ustayready](https://twitter.com/ustayready)
```
FireProx can bypass IP Based rate limiting using AWS. Try It
```

*[Tweet](https://twitter.com/ome_mishra/status/1241664059650404352) By [Ome Mishra](https://twitter.com/ome_mishra)*
```
Rate limiting Bypass by X-Host: 127.0.0.1 ..
If block after some request then try to increse the address from ...1 to ...2 and so on .
```

*[Tweet](https://twitter.com/udit_thakkur/status/1241832273898430464) By [Udit Thakkur](https://twitter.com/udit_thakkur/)*
```
Rate limit bypass:
Add header/s with request
X-Originating-IP: IP
X-Forwarded-For: IP
X-Remote-IP: IP
X-Remote-Addr: IP
X-Client-IP: IP
X-Host: IP
X-Forwared-Host: IP

If bypass successful, & after a while blocking request again. Increment the last octate
```

*[Tweet](https://twitter.com/harrmahar/status/1247306384128872448?s=20) By [Harrmahar](https://twitter.com/harrmahar/)*
```
Wanna Bypass Rate Limit ?
Try Bypass with adding null payload %00, %0d%0a, %09, %0C, %20, %0 on email. 
Not Works ?
Just try adding "blank space" on the email, works!
```

## Bypass Checks
*[Report #792895](https://hackerone.com/reports/792895) by [Green catz (hoangn1441)](https://hackerone.com/hoangn1441)*
- This trick can works for all kind of checks Old Password Check, Email Check, CSRF Token Check etc. :fire:

1. Change `parameter=value` to `parameter[]=value`
2. Bypass Successful

---------------------------------------------------------------------------------

## Writeups
### *[Methods to Bypass Rate Limit](https://medium.com/@huzaifa_tahir/methods-to-bypass-rate-limit-5185e6c67ecd) by [Huzaifa Tahir](https://medium.com/@huzaifa_tahir)* 
#### Places to find Rate Limit 
Login, Reset Password, 2FA, Sign up, Sending messages, Forums, comments, etc.
##### Bypassing WAF
 ```
X-Originating-IP: 127.0.0.1
X-Forwarded-For: 127.0.0.1
X-Remote-IP: 127.0.0.1
X-Remote-Addr: 127.0.0.1
or
Try with X-Forwarded-For: IP Header 2x times Instead of One time. (Tip from Kiraak Boy)
```
 - Using null byte and CRLF (a tip from [Zseano](https://twitter.com/zseano)) %00, %0d%0a, %09, %0C, %20, %0
 - Changing user-agents, cookies and IP address

---------------------------------------------------------------------------------
