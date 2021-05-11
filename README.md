# Project 7 - WordPress Pentesting

Time spent: **10** hours spent in total

> Objective: Find, analyze, recreate, and document **five vulnerabilities** affecting an old version of WordPress

## Pentesting Report

### 1. (Required) WordPress <= 4.2.2 - Authenticated Stored Cross-Site Scripting (XSS)
  - [X] Summary: 
    - Vulnerability types: XSS
    - Tested in version: 4.2
    - Fixed in version: 4.2.3
  - [X] GIF Walkthrough: <img src="WordPress Exploit 1.gif" alt="WordPress Exploit 1">
  - [X] Steps to recreate: First go to either wpdistillery.vm or 192.168.33.10 as an admin and then go to the Dashboard. Then, in the Dashboard, click on Pages and after you click on Pages, click on Add New. After you click on Add New, insert the following text into body of the Text box: `<a href="</a><a title=" onmouseover=alert('test')  ">link</a>`. After you have added the following text into the body of the Text box, click Publish and view the page. Finally, when viewing the page, an alert will pop up when hovering over the link showing that an XSS attack has been performed.
  - [X] Affected source code: 
    - [Link 1](https://klikki.fi/adv/wordpress3.html)
### 2. (Required) WordPress <= 4.3 - Authenticated Shortcode Tags Cross-Site Scripting (XSS)
  - [X] Summary: 
    - Vulnerability types: XSS
    - Tested in version: 4.2
    - Fixed in version: 4.2.5
  - [X] GIF Walkthrough: <img src="WordPress Exploit 2.gif" alt="WordPress Exploit 2">
  - [X] Steps to recreate: First go to either wpdistillery.vm or 192.168.33.10 as an admin and then go to the Dashboard. Then, in the Dashboard, click on Posts and after you click on Posts, click on Add New. After you click on Add New, insert the following text into the body of the Text box: `TEST!!![caption width="1" caption='<a href="' ">]</a><a href="http://onMouseOver='alert(1)'">Click me</a>`. After you have added the following text into the body of the Text box, click Publish and view the post. Finally, when viewing the post, an alert will pop up when hovering over or clicking on the tag showing that an XSS attack has been performed.
  - [X] Affected source code:
    - [Link 1](https://blog.checkpoint.com/2015/09/15/finding-vulnerabilities-in-core-wordpress-a-bug-hunters-trilogy-part-iii-ultimatum/)
    - [Link 2](https://blog.knownsec.com/2015/09/wordpress-vulnerability-analysis-cve-2015-5714-cve-2015-5715/)
### 3. (Required) WordPress  4.0-4.7.2 - Authenticated Stored Cross-Site Scripting (XSS) in YouTube URL Embeds
  - [X] Summary: 
    - Vulnerability types: XSS
    - Tested in version: 4.2
    - Fixed in version: 4.2.13
  - [X] GIF Walkthrough: <img src="WordPress Exploit 3.gif" alt="WordPress Exploit 3">
  - [X] Steps to recreate: First go to either wpdistillery.vm or 192.168.33.10 as an admin and then go to the Dashboard. Then, in the Dashboard, click on Posts and after you click on Posts, click on Add New. After you click on Add New, insert the following text into the body of the Text box: `[embed src='https://youtube.com/embed/12345\x3csvg onload=alert(1)\x3e'][/embed]`. After you have added the following text into the body of the Text box, click Publish and view the post. Finally, an alert will pop up when you view the post showing that an XSS attack has been performed.
  - [X] Affected source code:
    - [Link 1](https://blog.sucuri.net/2017/03/stored-xss-in-wordpress-core.html)
    - [Link 2](https://github.com/WordPress/WordPress/commit/419c8d97ce8df7d5004ee0b566bc5e095f0a6ca8)
### 4. (Optional) Vulnerability Name or ID
  - [ ] Summary: 
    - Vulnerability types:
    - Tested in version:
    - Fixed in version: 
  - [ ] GIF Walkthrough: 
  - [ ] Steps to recreate: 
  - [ ] Affected source code:
    - [Link 1](https://core.trac.wordpress.org/browser/tags/version/src/source_file.php)
### 5. (Optional) Vulnerability Name or ID
  - [ ] Summary: 
    - Vulnerability types:
    - Tested in version:
    - Fixed in version: 
  - [ ] GIF Walkthrough: 
  - [ ] Steps to recreate: 
  - [ ] Affected source code:
    - [Link 1](https://core.trac.wordpress.org/browser/tags/version/src/source_file.php) 

## Assets

List any additional assets, such as scripts or files

## Resources

- [WordPress Source Browser](https://core.trac.wordpress.org/browser/)
- [WordPress Developer Reference](https://developer.wordpress.org/reference/)

GIFs created with [LiceCap](http://www.cockos.com/licecap/).

## Notes

Describe any challenges encountered while doing the work

## License

    Copyright 2021 Ayush Gopisetty

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

        http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.
