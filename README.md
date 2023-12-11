<h1>BDNS - .₿itcoin Domain Name Server</h1>
&nbsp;

<i></i>Version 0.3</i>
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

1. <b>₿DNS ROOT SERVER (/INDEX) </b> - SNS (example.₿) will be connected to wallet (1abc...) and wallet registrated as owner
   
2. <b>₿TLD NAME SERVER (/INDEX) </b> - SNS will be connected to tx or ordinal inscription number
   
3. <b>₿SLD NAME SERVER (/INDEX) </b> - Sub level domain will be connected to tx or ordinal inscription number
   
4. <b>₿DNS RESOLVER</b> - Ordinal page will be cached

5. <b>FLAG SYSTEM</b> - Where one can flag ordinals if content is not "correct"

6. <b>BLIST</b> - For wallets and tx that have been flagged multiple times
   
&nbsp;

<h2>Intented method</h2>

&nbsp;

The following code could be inscribed via <a href="https://1satordinals.com/" target="_blank">1SatOrdinals.com</a> as text without further text/markdown:


&nbsp;

🟡 <b>₿DNS root connection SNS to wallet</b> ```{“p”: “bdns”, “op”: “bdns-reg”, “wllt”: “1abcd....”, “sns”: “example.₿”}```

&nbsp;

🟠 <b>₿DNS multi-chain root connection SNS to wallet</b> ```{“p”: “bdns”, “op”: “bdns-reg”, “chain”: “bsv”, “wllt”: “1abcd....”, “sns”: “example.₿”}```

&nbsp;

🟡 <b>₿TLD name connection SNS to ordinal</b> ```{“p”: “btld”, “op”: “btld-reg”, “sns”: “example.₿”, “inscr”: “12345678”}```

&nbsp;

🟠 <b>₿TLD multi-chain name connection SNS to ordinal</b> ```{“p”: “btld”, “op”: “btld-reg”, “chain”: “bsv”, “sns”: “example.₿”, “inscr”: “12345678”}```

&nbsp;

🟡 <b>₿SLD name connection SUB-SNS to ordinal</b> ```{“p”: “bsld”, “op”: “bsld-reg”, “sns”: “sub.example.₿”, “inscr”: “12345678”}```

&nbsp;

🟠 <b>₿SLD multi-chain name connection SUB-SNS to ordinal</b> ```{“p”: “bsld”, “op”: “bsld-reg”, “chain”: “bsv”, “sns”: “sub.example.₿”, “inscr”: “12345678”}```

&nbsp;

🟡 <b>SUB-SNS name registration</b>  ```{“p”: “sub-sns”, “op”: “reg”, “sns”: “sub.example.₿”}```
   
&nbsp;

<h2>Overview</h2>
&nbsp;

1. Through the ₿DNS, each SNS could be linked to a wallet (pay)
   
2. Through the ₿TLD, every SNS could be linked to an ordinal (web3)
   
3. Through the ₿SLD, every SUB-SNS could be linked to an ordinal (sub-web3)
   
4. Through the Flag-System one can flag an ordinal if the content is not "correct"
   
5. Through the ₿list for SNS and wallets that have been flagged multiple times in the flag-system one can be blocked
   
&nbsp;

<h2>Questions</h2>
&nbsp;

1. How to index the ₿DNS/₿TLD registrations?
   
2. How to connect the ₿DNS/₿TLD to a payment system or wallet?
   
3. How to view SNS web3 inscriptions directly outside of ordfs.network and ordnet.io within browser (ord://example.₿)?
   
4. Is there any way to create an SNS relay without the need to have the relevant SNS in the wallet used to connect the relay? In other words, could I create an SNS relay from wallet [a] with an ordinal located in wallet [b], or should the SNS be located in the wallet where the ordinal or transaction with which the relay is being laid is located?

5. Is there a puzzle-to-mint or quest-to-mint possible for inscribing ordinals? The OP-NS and L2M methods have both proven not to limit the time frame in which ordinals can be minted. Physically solving a puzzle (achieving a certain score after playing 30 minutes of tetris) after which the inscription can be made, seems to be the only solution where only a time factor is taken into account.

6. How should a sub domain be registered? Should the existing SNS code be used or should a custom SUB-SNS be created for optimal indexing? How to have the index validate only a SUB-SNS if created by the holder of the SNS? What if an SNS is transferred to another wallet? How could the SBS-SNS then be taken offline immediately?
   
&nbsp;
