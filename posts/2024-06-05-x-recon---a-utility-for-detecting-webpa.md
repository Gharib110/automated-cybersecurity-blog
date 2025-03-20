---
title: "X-Recon - A Utility For Detecting Webpage Inputs And Conducting XSS Scans"
date: Wed, 5 Jun 2024 08:30:00 -0400
draft: false
type: posts
categories: 
- Bugbounty,Bughunting,Hunt,X-Recon,XSS,XSS scanner,Xssscan
---
# X-Recon - A Utility For Detecting Webpage Inputs And Conducting XSS Scans

<br/>

<br/>
[![](https://blogger.googleusercontent.com/img/a/AVvXsEjkNqkJ4JSTGMe9h7TUb4TWZZ5WUL2p7ATWLSN3jdoFYNTMiswJ2vpDwz_XHRP3JAnB5GrSKBa-5CgUBIdOi-AT6ZadGolG7n8kBKRR3nEOKHK8t_mEtjdU1K0pQwp-dbYQkCxAiEvqJLL-8SzYmtR21_yOIHM3z1ZpAfqQWdNUD9u-nbiXhobrUupzHDc=w640-h260)](https://blogger.googleusercontent.com/img/a/AVvXsEjkNqkJ4JSTGMe9h7TUb4TWZZ5WUL2p7ATWLSN3jdoFYNTMiswJ2vpDwz_XHRP3JAnB5GrSKBa-5CgUBIdOi-AT6ZadGolG7n8kBKRR3nEOKHK8t_mEtjdU1K0pQwp-dbYQkCxAiEvqJLL-8SzYmtR21_yOIHM3z1ZpAfqQWdNUD9u-nbiXhobrUupzHDc)
=================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================

#### A utility for identifying web page inputs and conducting XSS scanning.

  

### Features:

-   **Subdomain Discovery:**
-   Retrieves relevant [subdomains](https://www.kitploit.com/search/label/Subdomains "subdomains") for the target website and consolidates them into a [whitelist](https://www.kitploit.com/search/label/Whitelist "whitelist"). These [subdomains](https://www.kitploit.com/search/label/Subdomains "subdomains") can be utilized during the [scraping](https://www.kitploit.com/search/label/Scraping "scraping") process.
    
-   **Site-wide Link Discovery:**
    
-   Collects all links throughout the website based on the provided whitelist and the specified `max_depth`.
    
-   **Form and Input Extraction:**
    
-   Identifies all forms and inputs found within the extracted links, generating a JSON output. This JSON output serves as a foundation for leveraging the XSS [scanning](https://www.kitploit.com/search/label/Scanning "scanning") capability of the tool.
    
-   **XSS Scanning:**
    
-   Once the start recon option returns a custom JSON containing the extracted entries, the X-Recon tool can initiate the XSS vulnerability testing process and furnish you with the desired results!

  

  

[![](https://blogger.googleusercontent.com/img/a/AVvXsEhF4ziki6Ns3j29jVJbK1d1pqwjOplRkzn_3HpLNaR-LkDi31d29PI4NUMS5zzDMJfG0E0JPsWre8kifiZXVvWttaFc_hLg4MQkL_ZHd9SWMJTpkiFI1t-cmL24AoS2X9gLDkB7u4K1ZXPxwDn6uSV3lC9qJgtyIh_vZcGtuKx7eZ2U5Vo0s7Xjuzcgv44=w640-h412)](https://blogger.googleusercontent.com/img/a/AVvXsEhF4ziki6Ns3j29jVJbK1d1pqwjOplRkzn_3HpLNaR-LkDi31d29PI4NUMS5zzDMJfG0E0JPsWre8kifiZXVvWttaFc_hLg4MQkL_ZHd9SWMJTpkiFI1t-cmL24AoS2X9gLDkB7u4K1ZXPxwDn6uSV3lC9qJgtyIh_vZcGtuKx7eZ2U5Vo0s7Xjuzcgv44)

[](https://github.com/joshkar/X-Recon "A utility for detecting webpage inputs and conducting XSS scans. (9)")  

**Note:**

> The scanning functionality is currently inactive on SPA (Single Page Application) web applications, and we have only tested it on websites developed with PHP, yielding remarkable results. In the future, we plan to incorporate these features into the tool.

  
  

[![](https://blogger.googleusercontent.com/img/a/AVvXsEhklSe168rzKvEepwK1pOEYbMjfMBDDFLDZF5PBbBYHXgXH6DZ5HXRPd3J4EbmqJAv9RIWE8ZPhbci6xV3vrXngLcstIfgzZINk8PhXAWuzwSvbkUDqegRe-AOmo1guRZCkCHLRWVmXnOd4fsmLjEciNfxhOXB42tWy1UpHU3cMbNxqoK7iDRTaFozqLow=w640-h382)](https://blogger.googleusercontent.com/img/a/AVvXsEhklSe168rzKvEepwK1pOEYbMjfMBDDFLDZF5PBbBYHXgXH6DZ5HXRPd3J4EbmqJAv9RIWE8ZPhbci6xV3vrXngLcstIfgzZINk8PhXAWuzwSvbkUDqegRe-AOmo1guRZCkCHLRWVmXnOd4fsmLjEciNfxhOXB42tWy1UpHU3cMbNxqoK7iDRTaFozqLow)

[](https://github.com/joshkar/X-Recon "A utility for detecting webpage inputs and conducting XSS scans. (10)")  

**Note:**

> This tool maintains an [up-to-date](https://www.kitploit.com/search/label/Up-to-date "up-to-date") list of file extensions that it skips during the exploration process. The default list includes common file types such as images, stylesheets, and scripts (`".css",".js",".mp4",".zip","png",".svg",".jpeg",".webp",".jpg",".gif"`). You can customize this list to better suit your needs by editing the setting.json file..

### Installation

```
$ git clone https://github.com/joshkar/X-Recon$ cd X-Recon$ python3 -m pip install -r requirements.txt$ python3 xr.py
```

Target For Test:
----------------

> You can use this address in the Get URL section

```
  http://testphp.vulnweb.com
```

  
  

**[Download X-Recon](https://github.com/joshkar/X-Recon "Download X-Recon")**

<br/>
[Source](http://www.kitploit.com/2024/06/x-recon-utility-for-detecting-webpage.html)
---
