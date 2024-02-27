--------------------------------------------------------------------------------------------------  

# Found bugs/issues:  

Forced to use "not-so-secret" password during sign-up for the first user  

### When creating a user on the "people" page  

password not obfuscated -------------------------- FIXED (/app/src/scenes/user/list.js -> line 144)  
user's name not set in the *Name* field -------------------------- FIXED (/app/src/scenes/user/list.js -> line 132)  
    
### When changing user's detail  

can't change user's name -------------------------- FIXED (FEATURE?) (/app/src/scenes/user/view.js -> line 63)  
*Update* button not working -------------------------- FIXED (/app/src/scenes/user/view.js -> line 136)  

### On "People" page  

search bar throwing fatal error -------------------------- FIXED (was due to previous bug "can't change user's name" fixed at /app/src/scenes/user/view.js -> line 63)  

### After creating a project  

needs reloading before being visible  
when clicked: fatal error on a *toSring* method -------------------------- FIXED (/app/src/scenes/project/view.js -> line 74)  
when clicked: name not displayed -> data is undefined -------------------------- FIXED (/api/src/controllers/project.js -> lines 22 and 23)  
when clicked: thus the edit panel can't load (*id* is undefined) -------------------------- FIXED (was due to previous bug, fixed in the api)  

--------------------------------------------------------------------------------------------------  

# Feature  

In a project's details, once you edit the project and define a "Budget max / month", the large "Budget consumed this month" is replaced with the progress bar.  
This is great but the key information is really small in my opinion. That's why I added the current spent budget inline with "Budget consummed this month:" in a large font.  
This way the key element is displayed in large and is easily readable (instead of being written in a really small font under the progress bar).  
I also added a large bold red "OVER BUDGET!" to accentuate the gravity of the issue on top of the jumping over-budget progress bar.  

/app/src/scenes/project/view.js -> lines 126 to 132

--------------------------------------------------------------------------------------------------  

# Feedback  

This was really fun! :)

Most of my issues had nothing to do with the project itself. 
I had some issues with npm which I fixed most of.

About the project, my first issue was not being able to sign up as a new user: I didn't know if it didn't work because of a bug I needed to fix or because of a real issue on my system/environment.
Ultimately, I searched the code for some hints, found the "not-so-secret" password and it worked. I could finally start working seriously on the project.

Everything went smoothly, I was already used to the api-app split thanks to working on an Android weather app project with a custom api hosted on a server. (Although I did everything locally here.)

All the bugs I found are listed above. I went ahead and fixed more than 3 (I didn't see time passing ahah).
I didn't really know what was expected for the "quick win feature" so I just identified something that I thought needed to be implemented and I did.

I was a bit lost when the "sign up" didn't work and when I was figuring out how the code was structured and "what did what" but I wanted to be 100% autonomous so I kept digging and it went really smoothly afterwards.

Anyway, that's pretty much it, it was quite fun.
