# terminology

---

## List
|n|name|desc.|O/P|
|-|----|-----|---|
|1|FortiOS|
|2|FortiWeb|
|3|FortiMail|
|4|Models|<ins>1. Entry level</ins><br/>FG-80F<br/>FWF-80F<br/><br/><ins>2. Mid-range</ins><br/>FG-100F<br/>FG-1000F<br/>FG-4200F<br/><br/><ins>3. High-end</ins><br/>FG-4800F<br/>FG-7081F<br/>FG-712F<br/>FG-5114C
|5|FortiGuard Labs|
|6|Static Routing||<img src="https://i.imgur.com/PGia3uk.png">|
|7|Firewall Policy||Accept<br/><img src="https://i.imgur.com/boppLfi.png"><br/>Deny:<br/><img src="https://i.imgur.com/R6d0sR1.png"><br/>FG can blocked a virus if its a virus:<br/><img src="https://i.imgur.com/BvmKp4P.png">|
|8|Policy Table||<img src="https://i.imgur.com/GE9gjCA.png">|
|9|Flow-Based Inspection|||
|10|Proxy-Based Inpsection||<img src="https://i.imgur.com/jJVwwBq.png">|
|11|Configuring FW auth||<img src="https://i.imgur.com/TJpX6EI.png">|
|12|Guest Accounts||<img src="https://i.imgur.com/aYbNmWa.png">|
|13|Cfg Remote auth||<img src="https://i.imgur.com/3TOySbb.png"><br/><img src="https://i.imgur.com/QrukF7E.png"><br/>Radius SRV:<br/><img src="https://i.imgur.com/q9sIZL6.png"><br/>Cfg LDAP SRV:<br/><img src="https://i.imgur.com/SKG5WVg.png">|
|14|Types of SSL Inpections|<ins>1. Cert. Inspection</ins><br/>* Inspects the SSL/TLS hadshake<br/>* Verifies the identity of the web server<br/>* Used only with web filtering<br/><br/><ins>2. Deep inspection</ins><br/>* Decrypts incoming traffic to inspect it<br/>* If safe, re-encrypts the traffic & sends it to the recipient<br/>* Used with all types of security scanning|
|15|Preloaded SSL Inspection Profiles||<img src="https://i.imgur.com/FpyhPeM.png">|
|16|cert warnings|<ins>Avoding cert. warning</ins><br/>1. download the fortinet cert<br/>2. use a CA-Issued SSL cert|<img src="https://i.imgur.com/OAmfBkB.png"><br/>Avoiding cert warning<br/><img src="https://i.imgur.com/cY7Huwg.png">|
|17|Virus outbreak prevention||<img src="https://i.imgur.com/mbcDooz.png">|
|18|IPS||<img src="https://i.imgur.com/f4MBiSC.png"><br/>IPS Func overview<br/><img src="https://i.imgur.com/36VkTgQ.png"><br/>Engine Detection Techniques<br/><img src="https://i.imgur.com/uvLszb8.png"><br/>signature<br/><img src="https://i.imgur.com/XVD4ZYP.png"><br/>Proto decoders<br/><img src="https://i.imgur.com/SUCibDb.png"><br/>Best Practices for IPS<br/><img src="https://i.imgur.com/9VpYGx5.png">check if IPS db is up to date<br/><img src="https://i.imgur.com/zgXu6Kz.png"><br/>IPS sensors<br/><img src="https://i.imgur.com/yCzQcGh.png"><br/>IPS both for incoming & outgoing traffic<br/><img src="https://i.imgur.com/lpooScu.png"><br/>fw pol - IPS enabled<br/><img src="https://i.imgur.com/JO3nhzS.png"><br/>Add signature<br/><img src="https://i.imgur.com/yGehmQR.png">|
|19|app control||<img src="https://i.imgur.com/5H8Zovi.png"><br/>Controlling app access<br/><img src="https://i.imgur.com/y5TCeTR.png"><br/>App Control Settings<br/><img src="https://i.imgur.com/i6EPWii.png">|
|20|IPsec VPNs||<img src="https://i.imgur.com/CM8qxbJ.png"><br/> Types of VPNs<br/><img src="https://i.imgur.com/pTIpXD7.png"><br/>Remote Access VPNs (P2S)<br/><img src="https://i.imgur.com/8oQw8v9.png"><br/>S2S VPNs<br/><img src="https://i.imgur.com/JhOlXDo.png"><br/>IKE Proto<br/><img src="https://i.imgur.com/FERnbb2.png"><br/>IKEv1 proto phase1 param<br/><img src="https://i.imgur.com/9OP0tOx.png"><br/>IKEv1 proto phase2<br/><img src="https://i.imgur.com/kGup7x3.png"><br/>IKEv1 proto phase2 params<br/><img src="https://i.imgur.com/tuIWe5n.png"><br/>IKEv2 proto<br/><img src="https://i.imgur.com/YtKtXns.png"><br/>Benefits of using IKEv2 over IKEv1<br/><img src="https://i.imgur.com/FkBCluU.png"><br/>VPN cfg Best practices - fw latest update<br/><img src="https://i.imgur.com/vuJRrDo.png"><br/>VPN cfg Best - practices - overview<br/><img src="https://i.imgur.com/MifkzOz.png">|
|21|ESP||<img src="https://i.imgur.com/yDcfeTw.png">|
|22|SSL VPN||<img src="https://i.imgur.com/2SY4MZH.png"><br/>SSL VPN func<br/><ins>Web mode</ins><br/><img src="https://i.imgur.com/qnbtI4S.png"><br/>Tunnel mode<br/><img src="https://i.imgur.com/0BOWMzz.png"><br/>Best Practices<br/><img src="https://i.imgur.com/9Eqk1Qa.png">|
|22|Functions of FG System Maintenance||<img src="https://i.imgur.com/q3dAmEb.png"><br/>bk FG cfg - different build<br/><img src="https://i.imgur.com/fwOres4.png"><br/>Performing fw upgrade - Feature & mature<br/><img src="https://i.imgur.com/AK9uGcS.png"><br/>Recommended upgrade path<br/><img src="https://i.imgur.com/01EkEWa.png"><br/><img src="https://i.imgur.com/TIGnUPZ.png"><br/>Recommended upgrade path - example<br/><img src="https://i.imgur.com/UbXnNWL.png">Fortinet upgrade path tool<br/><img src="https://i.imgur.com/GhDGl9A.png">|
