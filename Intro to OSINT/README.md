# Capstone Project
## [Certificate](https://github.com/alejandro-garf/Blue-Team-Junior-Analyst/blob/main/Intro%20to%20DarkWeb%20Operations/IntroToDarkwebOPs.pdf)
## Scenario
You work for a law enforcement organisation, and you have been assigned to track a person-of-interest, that is believed to be associated with a hacking group that recently compromised a Managed Service Provider (MSP) and are trying to sell the stolen credentials on both the clear net and dark web. Another team is focusing on the dark web lead, so you have been tasked with using OSINT sources to build up a profile on the individual and attempt to locate any evidence that links them to the MSP breach and sale of account details. You have been provided with some information to start your investigation. You should use any of the sources or tools taught in this course, that you deem to be applicable and appropriate. We know that the email address used to register the Twitter account is fake, so do not include this in your report.

### Setting Up
 - Booted up my Vm
 - Turned on my VPN
 - Went on the Tor Browser to the given site
### Getting User Credentials 
 - Go to Login page, right clicked and went to console
 - used the following command
   ```
      use this command & press ctrl+enter
      generateUserCredentials() 
 - Got a Base64 encoded string
 - Decoded it and got:
```
USR:KF7ybuD1, PASS: AlyhfotV9VIWm6W
```
 - Logged In
### Decoding the Page
 - Entire Page seems encoded in Hexadecimaks
 - Decoded and found the drug dealers blog
### Image Forenscics
 - Reverse imaged searched image on the blog and got the location of Flexistowe England
 - Found picture of US Passport on pictures in the blogs indicicating that he is a US Citizen
 - Boarding pass gives name when upscalling the image: Kestner Richard
 - Sticky note in one of the pictures gives Coordiates


## Through this simple investigation I was able to obtain the following details of the dealer;
### Username
### Name
### Location of Delivery
### Country of Origin
### Coordinates
