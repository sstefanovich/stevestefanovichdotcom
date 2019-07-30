Title: Excuse the Dust
Published: 7/29/2019
Tags: [Introduction, Wyam, Netlify]
---
Excuse the dust as I get this site setup. The first order of business is getting the stack in order and I plan to document each step along the way. 

# Step 1: Get a domain. 
Thankfully my surname isn't all that common so getting my own name on the .com TLD turned out to be a non-issue. $11.99 and I'm all set. 

# Step 2: Choose a Platform 
I quickly settled on [Wyam](https://wyam.io/). Open-Source, .NET based, command-line driven and I can use Visual Studio Code to edit everything. The hardest part was picking a theme and writing the introduction. A few things I got hung up on that may be worth noting:
- If you're going to use Visual Studio Code as an editor, [install a spell-checker](https://marketplace.visualstudio.com/items?itemName=streetsidesoftware.code-spell-checker).
- Tags for a post need to be passed as an array: 
    
    Tags: [Introduction, Wyam, Netlify]

or put them on separate lines. 

    Tags: 
    - Introduction
    - Wyam
    - Netlify

If you miss the brackets, you'll get one giant tag with commas included.

# Step 3: Find a Host
I briefly considered Azure Web Sites but unfortunately the free-tier does not include custom domains. I've got a shiny new domain I need to use! While searching, I came across [Netlify](https://www.netlify.com/) and it seems like a great fit. The free tier offers SSL, plenty of bandwidth and custom domain support. The CLI and ease of deployment are nice additions as well. 

# Step 4: Continuous Deployment
Stay tuned for details on this in a future entry. For now I'll be deploying manually.

Now that I have all the pieces in place, there are a few housekeeping items to take care of: DNS entries for my new domain, setting up the site on Netlify and finally, building and deploying the initial version (and getting the code on GitHub). Stay tuned.