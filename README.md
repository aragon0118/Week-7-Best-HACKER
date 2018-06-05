# Project 7 - WordPress Pentesting

Time spent: 12 hours spent in total

> Objective: Find, analyze, recreate, and document 3 vulnarabilities affecting an old version of WordPress

## Pentesting Report

1. 4.2 - Unauthenticated Corss-Site Scripting (XSS)
  - [x] Summary: 
    - Vulnerability types: XSS
    - Tested in version: 4.2
    - Fixed in version: 4.2.1
  - [x] GIF Walkthrough: ![](https://github.com/aragon0118/Week-7-Best-HACKER/blob/master/XSS%20Week%207.gif)
  - [x] Steps to recreate: Commented with the following string and replaced ...[64 KB]... with 65536 A's (characters) 
```
(<a title='x onmouseovlert(unescape(/BEST%20HACKER/.source)) style=position:absolute;left:0;top:0;width:5000px;height:5000px  AAAAAAAAAAAA...[64 kb]..AAA'></a>er=a)
```
  - [x] Affected source code:
    - [Reference](https://klikki.fi/adv/wordpress2.html)
2. Username Disclosure (User Enumeration)
  - [x] Summary: 
    - Vulnerability types: user enumeration
    - Tested in version: 4.2.2
    - Fixed in version: -
  - [x] GIF Walkthrough: ![](https://github.com/aragon0118/Week-7-Best-HACKER/blob/master/Username%20Week%207.gif)
  - [x] Steps to recreate: When you try to login with a non-existent username the error page states "ERROR: Invalid username." Unlike when using known username but wrong password to login the error page states "ERROR: The password you entered for the username **admin** is incorrect."
  - [x] Affected source code:
    - [Reference](https://www.wpwhitesecurity.com/wordpress-security/wordpress-username-disclosure-vulnerability/)
3. Privilege Escalation
  - [ ] Summary: 
    - Vulnerability types: privilege escalation
    - Tested in version: 4.2
    - Fixed in version: 4.7.2
  - [x] GIF Walkthrough: ![](https://github.com/aragon0118/Week-7-Best-HACKER/blob/master/PrivilegeEscalation%20Week%207.gif)
  - [x] Steps to recreate: When any user/non-registered user posts a comment on a page or post it needs approval from the admin. Yet, once one comment is approved any comments posted after no longer need approval. 
  - [] Affected source code:
   

## Assets

List any additional assets, such as scripts or files

## Resources

- [WordPress Source Browser](https://core.trac.wordpress.org/browser/)
- [WordPress Developer Reference](https://developer.wordpress.org/reference/)

GIFs created with [LiceCap](http://www.cockos.com/licecap/).

## Notes

Describe any challenges encountered while doing the work

## License

    Copyright [yyyy] [name of copyright owner]

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

        http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.
