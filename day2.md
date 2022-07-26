- # WAF BYPASS ON SOME OF WEB BUGS 
- #### hello guys today im going to talk about some tricks to bypass the WAF (web application fire wall ) on some of web vulnerabilities
- #### first we need to start with some difinitions 
- ## what is a WAF 
![image](https://raw.githubusercontent.com/ADNXB/test/adc25427878b5c98188c119caa4bd91555fa7d0d/WAF.svg)
- #### A WAF or web application firewall helps protect web applications by filtering and monitoring HTTP traffic between a web application and the Internet. It typically protects web applications from attacks
- # How to bypass the WAF on ssrf 
- ## what is ssrf (Server-side request forgery)
- ![image](https://raw.githubusercontent.com/ADNXB/test/main/SSRF-1.png)
- #### Server-side request forgery (also known as SSRF) is a web security vulnerability that allows an attacker to induce the server-side application to make requests to an unintended location.
- ## WAF Bypass
- ### WAF Bypass using http:localhost instead of the ip
- #### if the WAF filter just the 127.0.0.1 ip we can use http://localhost instead of it 
- ### WAF bypass using IPV6
- #### if the WAF filter the 127.0.0.1 , we can bypass the waf using the IPV6 and it is by using http://::1 instead of 127.0.0.1
- ### WAF Bypass using domained local host
- #### in this way we can use a domained local host that redirect us to 127.0.0.1 this domain is an exemple localtest.me , 
- ### WAF Bypass using long ip
- #### we can convert the ip adress which is 127.0.0.1 to a Hexadecimal value , and the server will understand it like a 127.0.0.1 using this website https://www.smartconversion.com/unit_conversion/IP_Address_Converter.aspx
![image](https://raw.githubusercontent.com/ADNXB/test/main/long.PNG)
