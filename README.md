# NATAS   😊😊

# Natas teaches the basics of serverside web-security.

Each level of natas consists of its own website located at **http://natasX.natas.labs.overthewire.org** where X is the level number. There is no SSH login.

**To access a level, enter the username for that level (e.g. natas0 for level 0) and its password.**

Each level has access to the password of the next level. Your job is to somehow obtain that next password and level up.

# Start here:

Username: natas0\
Password: natas0\
URL:      http://natas0.natas.labs.overthewire.org

# LEVEL 0

Once we are logged in, the level hint will appear in the middle of the screen ie, it is showing that **you can find the password for the next level on this page** Thats it..Nothing else. And you have to find the password for entering into the next level. After searching the web page thoroughly I have gone to the view page source ... then I got the password showing that the password for the next level is ****@@##%$$%^&&**(&^%%$ like this.......

**What u want....password** try it and get it....😂🤣



# LEVEL 0 ➠ LEVEL 1


Once we are logged in, the level hint will appear in the middle of the screen ie, it is showing that **You can find the password for the next level on this page, but rightclicking has been blocked!** 
Thats it ...Nothing else . You have to go to the view command on thw window of the web page there it will show a developer option , there u will get view source click on it..it will open the source code of that page and finally u will get the password -- **@#$%^&*((&^%$#** that will help you to get enter into the next level...

PASSWORD :  **nahhhhhahahaa**😂🤣😂


# LEVEL 1 ➠ LEVEL 2

Once ur logged in, the level hint will appear in the middle of the server ie, **There is nothing on the webpage** . After viewing the source page of that level it is showing that it is containing a png file. To open that I have add /files after the main urls which ur working on it. After viewing that site a new page appears that is **Index of /files** it contains two file ... one is the **pixel.png** file and other is the **user.txt** file. 
After opening the user.txt file it is showing the password for the next level....

PASSWORD : **@#$%^&*(&^%%$**


# LEVEL 2 ➠ LEVEL 3

Once ur logged in, the level hint will appear in the middle of the server ie, **There is nothing on the webpage** Again...in this level the same hint is showing .
**“Not even Google will find it this time…”** is our hint here. If you have some idea of HTML, and about web servers, then you would know that the files it’s referring too is **robots.txt**. When u go to that url using **robots.txt** at last it will display 
User-agent: *\
Disallow: /s3cr3t/\
Then, so the robots.txt is disallowing crawlers to find /s3cr3t/. Let’s go ahead and add it to the end of the webpage, which should look something like this: http://natas3.natas.labs.overthewire.org/s3cr3t/. 
After clicking on the above link it will open a page named **Index of /s3cr3t/** and it is showing a file named **user.txt**.
After opening this file it will show the password of the next level.

PASSWORD : **@#$%^&*()(*&^%**

# LEVEL 3 ➠ LEVEL 4

Once ur logged in, the level hint will appear in the middle of the server ie, **Access disallowed. You are visiting from "http://natas4.natas.labs.overthewire.org/" while authorized users should come only from "http://natas5.natas.labs.overthewire.org/"** ..
So after seeing that I have searched in google, it shows that we have to change the HTTP Referer to natas5 using a web security tools . Then only we can get access to the page where the password id stored.
But Using the inspect element , u can go to network settings and add a Referer and edit it to natas5 and send it.
Then it will not refresh the page automatically, you have to go to reference setting and then it will show the page with index.php page wuth natas5 and what u can see is that the password is here....

PASSWORD : **@#$$%%^^&**


# LEVEL 4 ➠ LEVEL 5

Once ur logged in, the level hint will appear in the middle of the server ie, **Access disallowed .You are not logged in.**
So after seeing that I reached to the view page source there I find nothing ..Just It is showing the same thing .. No file , no hidden file , nothing..
Then I have gone to inspect Element, theere I have seen in the Header section that there is one cookies and it is showing that **loggedin=0** And when I Edited this cookies to **loggedin=1** and then i send it and after that I checked in the response section there the page is loaded and the password for the next level is displayed..

PASSWORD : **@#$$#$%^&**


# LEVEL 5 ➠ LEVEL 6

Once ur logged in, the level hint will appear in the middle of the server ie, **Input secret** And There it is showing view page source.
After clicking the page source it is showing a php file and It seems that the PHP is including a link to a file stored on the webpage **/includes/secret.inc**.
Then I go to that webpae who include that secret.inc there I found a secret key , after pasting it and after submitting it the password for the next level is displayed...

PASSWORD : **@#$%^&&^**


# LEVEL 6 ➠ LEVEL 7

Once ur logged in, the level hint will appear in the middle of the server ie, **only two thing one is Home and other is About**.
After viewing the source page of that page it is displaying extra thing ie, a type of hint **hint: password for webuser natas8 is in /etc/natas_webpass/natas8**.
After clicking on the home link then it is showing a another web apge in which it is showing same Home and About link and other than that it is displaying that it is **the front page**.
Then I try that to edit the URL of the home page ie **http://natas7.natas.labs.overthewire.org/index.php?page=home**
And I have edited the urls remove the home and paste this hint **/etc/natas_webpass/natas8** after page and searched it. Then I have find the password for the next Level...

PASSWORD : **@#$%^&&^%**


# LEVEL 7 ➠ LEVEL 8

Once ur logged in, the level hint will appear in the middle of the server ie, **Input Secret** thats it..
After Viewing the Source code which is displayed in the webpage, It seems that the secret code we need is encoded. Looking though the PHP code we can see that the “secret” entered is converted from bin to hex, reversed, and then base64 encoded.
So for us to get the “secret” we have to reverse engineer this. 
So I have gone in online php editor and use this command :**echo base64_decode(strrev(hex2bin('3d3d516343746d4d6d6c315669563362')));** Then, We can get the secret key from the encoded key by base64 decoding it, reversing the string, and converting the hex back to binary.
If you have done correctly, you should get the secret key **@#$%^&^**. Let’s enter that and see if it works.
Then You should find the password for the next Level....

PASSWORD : **@#$%^&^%**






