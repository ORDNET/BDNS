<h1>BDNS - .₿itcoin Domain Name Server</h1>
&nbsp;

<i></i>Version 0.2</i>
&nbsp;

This concerns a concept note to see to what extent it is possible to easily link ordinal SNS addresses to a wallet, inscription or transaction for easy receipt of coins and tokens and viewing ordinals via a(n) (ordinal) browser.
&nbsp;

&nbsp;


<h2>DNS - Current infrastructure</h2>
&nbsp;

The current internet uses the DNS model that works (very broadly defined) as follows:
&nbsp;

1. User visits www. domain

2. DNS resolver releases website from cache (if previously visited)

3. www. domain is checked by the DNS root name server

4. Next, www. domain is checked by the TLD name server

5. Last, the www. data is loaded from the central web server

&nbsp;


<h2>₿DNS - Bitcoin ordinal registration</h2>
&nbsp;

Below is an initial outline and should be further reviewed, walked through and tested allowing for adjustments to be made in the future: 
&nbsp;

1. <b>₿DNS ROOT SERVER</b> - SNS (example.₿) will be connected to wallet (1abc...) and wallet registrated as owner
   
2. <b>₿TLD NAME SERVER</b> - SNS will be connected to tx or ordinal inscription number
   
3. <b>₿DNS RESOLVER</b> - Ordinal page will be cached

4. <b>FLAG SYSTEM</b> - Where one can flag ordinals if content is not "correct"

5. <b>BLIST</b> - For wallets and tx that have been flagged multiple times
   
&nbsp;

<h2>Intented method</h2>

The following code could be inscribed via <a href="https://1satordinals.com/" target="_blank">1SatOrdinals.com</a> as text without further text/markdown:
&nbsp;


₿DNS root connection SNS to wallet ```{“p”: “bdns”, “op”: “bdns-reg”, “wllt”: “1abcd....”, “sns”: “example.₿”}```

₿TLD name connection SNS to ordinal ```{“p”: “btld”, “op”: “btld-reg”, “sns”: “example.₿”, “inscr”: “12345678”}```
   
&nbsp;

<h2>Overview</h2>
&nbsp;

1. Through the ₿DNS, each SNS could be linked to a wallet (pay)
   
2. Through the ₿TLD, every SNS could be linked to an ordinal (web3)
   
3. Through the Flag-System one can flag an ordinal if the content is not "correct"
   
4. Through the ₿list for SNS and wallets that have been flagged multiple times in the flag-system one can be blocked
   
&nbsp;

<h2>How to</h2>
&nbsp;

1. How to index the ₿DNS/₿TLD registrations?
   
2. How to make the ₿DNS/₿TLD act as a payment system?
   
3. How to view SNS web3 inscriptions directly outside of ordfs.network and ordnet.io within browser (ord://example.₿)
   
&nbsp;
