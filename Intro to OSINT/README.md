# Capstone Project
## [Certificate](https://github.com/alejandro-garf/Blue-Team-Junior-Analyst/blob/main/Intro%20to%20OSINT/Course%20-%20Certificate%20-%20Introduction%20to%20OSINT-course.pdf)
## Scenario
You work for a law enforcement organization, and you have been assigned to track a person-of-interest, that is believed to be associated with a hacking group that recently compromised a Managed Service Provider (MSP) and are trying to sell the stolen credentials on both the clear net and dark web. Another team is focusing on the dark web lead, so you have been tasked with using OSINT sources to build up a profile on the individual and attempt to locate any evidence that links them to the MSP breach and sale of account details. You have been provided with some information to start your investigation. You should use any of the sources or tools taught in this course, that you deem to be applicable and appropriate. We know that the email address used to register the Twitter account is fake, so do not include this in your report.

Your manager has provided you with the following starting information:

    Twitter handle used by actor: @sp1ritfyre

## Steps
### Step One 
 - Googling the twitter handle gives us the twitter account of the POI.
 - There is a link to a website showing on the POI’s profile.
 - At first glance, the website appears to contain random letters and numbers. However, this is actually a base64 encoded string.
### Step Twp
 - I used CyberChef to decode the string.
 - Gives us ``` redhunt.h ``` as the output.
 - corresponds to the third entry displayed on the google search results a while back.
 - I looked at the whois record of redhunt.net but I found no useful information. The website itself also yielded no useful information.
### Step Three
 - I went back to the search results and tried the blogger website.
 - Two things stand out, the contact me email and address
 - This may provide us the POI’s email address.
 - The random letters and numbers showing on the location section is another encoded string.
### Step Four
 - I clicked on the link indicated under “My blogs” and was redirected to the blog.
 - I went back to the user profile and clicked the mailto link in the “contact me” section.
 - Here was presented with an email ``` d1ved33p@gmail.com ```
 -  took note of this email address and decided to investigate further.
### Step Five
 - I decoded the hexadecimal encoded string using CyberChef.
 - I got the following output: ``` https:://samiwoodsec.blogspot.com ```
 - I found an email address (d1ved33p@gmail.com) mentioned in the latest blog entry.
 - This is the same email I found in the “contact me” section of the blogger site I visited earlier.
### Step Six
 - Next, I clicked the “view my complete profile” on the “about me” section of the website.
 - This brought me to a page with all the info on the hacker that I needed to finish the capstone.
```
1. What is the hacker’s first name?

Sam

2. What is the hacker’s last name?

Woods

3. What is the hacker’s age?

23

4. What country does the hacker live in?

United Kingdom

5. What are some of the hacker’s interests? (choose 5)

Security, Photography, Gaming, Malware Analysis and Camping

6. What company does the hacker work for?

Philman Security Inc

7. What is the hacker’s position within the company?

Junior Penetration Tester

8. What is the full url of the website owned by the hacker?

https://redhunt.net

9. List any full URLs of websites not owned, but used by the hacker (Blogs only)

https://sp1ritfyrehackerstories.blogspot.com/ https://sammiewoodsec.blogspot.com/

10. What email address has been used by the hacker?

d1ved33p@gmail.com
```
