
Resouces:
* https://en.wikipedia.org/wiki/Burp_Suite
* David Bombal(Youtube video)
  
BrupSuit:
* Burp Suite is a software security application used for penetration testing of web applications.
* This software is developed by the company PortSwigger
* we doesn't konw what happening in web applications but by using burpsuit we are knowing what happening inside it.
  
Why is Burp Suite Used in Cybersecurity 
* Web crawling-Web crawling is the process of indexing data on web pages by using a program or automated script
* Web application testing, both manually and automatically.
* Analysis of web applications.
* Vulnerability detection

Installation:

* Go to portswigger official website(https://portswigger.net/burp/communitydownload)
* Their you have a download option,download the file execute the .exe file
* After completion of installation if you search for burpsuit
* ![Screenshot (146)](https://github.com/Yamunasri1825/Yamunasri1825/assets/131263371/d078152a-1468-4c54-8108-c9a7a2249096)

* we require foxyproxy
* FoxyProxy helps users configure web browsers like Google and Firefox with proxy servers.
* Installation of foxyproxy
* open firefox search for ‘FoxyProxy standard extension'
  ![Screenshot (143)](https://github.com/Yamunasri1825/Yamunasri1825/assets/131263371/b4041cf5-b321-4d8a-bff0-3b8e207d0413)
 * Now, you will see the pop up that says “FoxyProxy is added”. Click okay on that pop-up. You will find the FoxyProxy icon on the right of the browser toolbar. Click on that icon and click options from the dialog box that appears.
 * After completion of installation
 * ![Screenshot (145)](https://github.com/Yamunasri1825/Yamunasri1825/assets/131263371/8fd10a95-82dd-42f4-9dea-aa47f8b151eb)
 * This may be you will find
   
Brupsuit:
* I notice some http history when we search in web browser
* And also i notice the actions if we made any request what is the response to my request
* i take an example web site chodechef (i searched in firefox and obeserve the http history i obeserve the requests and response)
* ![Screenshot (148)](https://github.com/Yamunasri1825/Yamunasri1825/assets/131263371/f120ca4c-8e56-4aee-8119-7c8e69cf8d6c)

* ![Screenshot (147)](https://github.com/Yamunasri1825/Yamunasri1825/assets/131263371/00bfd142-af73-4a24-9039-c9fe99898eda)
* i obeserve the source code in response side
* if i try to login in into the codechef i observe request method is in POST
* By that i understand we are request our credential to the server(so that the method is post method)
* After that i started target section in that i observe issue definitions(still reading)
  
  2-12-2023
Resources:
* https://www.cybercrowd.co.uk/news/impact-of-a-sql-injection/
* Youtube Video(Rana Khalil)
  
SQL  injection:
  Vulnerability that consist of an attacker interfering with sql queries that application makes a database.

IMPACT OF SQL INJECTION:

* Confidentiality: Since SQL databases generally hold sensitive data, loss of confidentiality is a frequent problem with SQL Injection vulnerabilities.
* Authentication: If poor SQL commands are used to check user names and passwords, it may be possible to connect to a system as another user with no previous knowledge of the password.
* Authorisation: If authorisation information is held in a SQL database, it may be possible to change this information through the successful exploitation of a SQL Injection vulnerability.
* Integrity: Just as it may be possible to read sensitive information, it is also possible to make changes or even delete this information with a SQL Injection attack.
  
* Remote code execution on the operating system.

TYPES OF SQL INJECTION:
1.In-Band(Classic)
   i)error
   ii)Union
2.Inferential(Blind)
 i)Boolean
 ii)Time
3.out-of-band

I solved one lab in portswigger

question:
This lab contains a SQL injection vulnerability in the product category filter. When the user selects a category, the application carries out a SQL query like the following:
SELECT * FROM products WHERE category = 'Gifts' AND released = 1
To solve the lab, perform a SQL injection attack that causes the application to display one or more unreleased products.

SOLUTION:
. SELECT * FROM products WHERE category = 'Pets' AND released = 1
. SELECT * FROM products WHERE category = ''' AND released = 1
.SELECT * FROM products WHERE category = ''--' AND released = 1
.SELECT * FROM products WHERE category = ''
SELECT * FROM products WHERE category = '' or 1=1 --' AND released = 1
