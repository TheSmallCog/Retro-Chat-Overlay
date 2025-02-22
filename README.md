<h1>Thank you for choosing my Retro Chat Overlay!</h1>
A simple, customizable Twitch chat overlay that you can easily use in OBS. The overlay displays chat messages with customizable styling for different user roles. 

<h3>Features</h3>

- Role-Based Styling: Different styles for streamers, mods, subscribers, followers, and non-followers.
- Third-Party Emotes: Supports BTTV and FFZ emotes.
- Animated Messages: Comes with a basic but snappy slide animation.
- Screen-reader compatibility.
- Keyboard-only friendly.
- Customizable Text and Outline Colors: Adjust the text color, outline color, and outline thickness via a small on-screen collapsable menu.
- Persistent Preferences: Your text customization preferences are saved in your browser's local storage.

<h1>Installation and Setup</h1>

This can be done using Github's web broswer interface, all you need is a GitHub account. If you don't have one make one before continuing (it's free!)

<b>If you wish to contribute to the original project, you can clone the repo instead. If that is your goal I will assume you know how to do so or are okay with figuring it out.</b>

<h3>Step 1: Fork the Repository</h3>

Locate the "Fork" button at the upper-right corner of the repository

<img src="https://raw.githubusercontent.com/TheSmallCog/Retro-Chat-Overlay/refs/heads/main/Tutorial%20Images/Fork%20Button.png"></src>

Click it

<img src="https://raw.githubusercontent.com/TheSmallCog/Retro-Chat-Overlay/refs/heads/main/Tutorial%20Images/Create%20Fork.png"></src>

Rename the repository and adjust the description as desire, then click the "Create Fork" button. It will take some time to load and then you'll have a brand-new forked repository. 
   
<h3>Step 2: Open <code>index.html</code> and replace <code>'YOURCHANNELHERE'</code></h3>

Open the <code>index.html</code> file and click on the small pencil icon in the upper-right corner to edit the file

<img src="https://raw.githubusercontent.com/TheSmallCog/Retro-Chat-Overlay/refs/heads/main/Tutorial%20Images/Edit%20Button.png"></src>

Once you're in editing mode, replace all instances of <code>'YOURCHANNELHERE'</code> with your Twitch username. There are two places where you need to make this change:

  >In the fetchThirdPartyEmotes function call at line 635:

<code> fetchThirdPartyEmotes('YOURCHANNELHERE').then(emotes => { </code>
  
  >In the ComfyJS.Init function call at line 686:

<code> ComfyJS.Init('YOURCHANNELHERE'); </code>

Don't forget to save the file when you're done!

<h3>Step 3:Get Your Browser Link</h3>

<b>To use this overlay in OBS or another streaming software as a browser source, you need to host the <code>index.html</code> file. You can host it using various methods, however that free GitHub account you made will let you host a free webpage for the forked repository, courtesy of GitPages.</b>

Click "Settings" at the top right of the depository

<img src="https://raw.githubusercontent.com/TheSmallCog/Retro-Chat-Overlay/refs/heads/main/Tutorial%20Images/settings%20button.png"></src>

Click "Pages" on the left menu

<img src="https://raw.githubusercontent.com/TheSmallCog/Retro-Chat-Overlay/refs/heads/main/Tutorial%20Images/Pages%20button.png"></src>

Navigate to the "Branch" section and click "None", then Select "Main" in the drop-down menu
<img src="https://raw.githubusercontent.com/TheSmallCog/Retro-Chat-Overlay/refs/heads/main/Tutorial%20Images/Choose%20Branch.png"></src>

Click the "Save" button

<img src="https://raw.githubusercontent.com/TheSmallCog/Retro-Chat-Overlay/refs/heads/main/Tutorial%20Images/Save%20Branch.png"></src>

After you've saved, go back to the main page of the repository and click on the "Actions" tab

<img src="https://raw.githubusercontent.com/TheSmallCog/Retro-Chat-Overlay/refs/heads/main/Tutorial%20Images/Actions%20tab.png"></src>ll

This page will show the progess of any actions you take regarding the repository. 
Right now, the only thing you should see is the status of your deployment. 

<img src="https://raw.githubusercontent.com/TheSmallCog/Retro-Chat-Overlay/refs/heads/main/Tutorial%20Images/Deployed%20Checkmark.png"></src>

If the checkmark is green, congratulations! You have successfully deployed the GitHub page and are ready to put the URL into OBS as a browser source.

<h3>Step 4: Add the Overlay to OBS</h3>

Open OBS and go to the scene where you want to add the chat overlay
Click the + button under "Sources" and select Browser

Name the source (eg."Retro Chat Overlay")

<img src="https://raw.githubusercontent.com/TheSmallCog/Retro-Chat-Overlay/refs/heads/main/Tutorial%20Images/Name%20Source.png"></src>

In the "URL" field, enter the URL of your newly created GitHub deployment (not the page, the deployment)

<img src="https://raw.githubusercontent.com/TheSmallCog/Retro-Chat-Overlay/refs/heads/main/Tutorial%20Images/browser%20link.png"></src>

Adjust width and height as needed for your particular stream. If you don't want the collapsable menu to appear on screen, I recommend putting it just off of the canvas in OBS, there's enough padding that the messages will still show in their entirety.

<img src="https://raw.githubusercontent.com/TheSmallCog/Retro-Chat-Overlay/refs/heads/main/Tutorial%20Images/showing%20padding%20for%20menu.png"></src>

<h3>Step 5: Customize the Overlay</h3>

In OBS, right-click the browser source and select Interact.
Click on the gear icon in the collapsable menu to customize the text color, outline color, and outline thickness.

<img src="https://raw.githubusercontent.com/TheSmallCog/Retro-Chat-Overlay/refs/heads/main/Tutorial%20Images/Menu%20button.png"></src>

<img src ="https://raw.githubusercontent.com/TheSmallCog/Retro-Chat-Overlay/refs/heads/main/Tutorial%20Images/default%20customization.png"></src>

Your preferences will be saved automatically. Whenever you want to save a specific text palette just hit the "Save Palette" button and type in a name and hit 'Enter'. Once saved, you can hit the "Load Palette" button to bring up a dropdown menu of all your saved palettes, and then select the one you want at any time.


<h2>Credits</h2>

Huge thanks to InstaFluff (https://github.com/instafluff) for creating the ComfyJS library and making this all possible. 
Equal thanks as well to Anetaa Wamono for creating the basic twitch chat overlay tutorial (https://github.com/annetawamono/twitch-chat-tutorial) that was the inital foundation for this project.

<h2>License</h2>

This project is open-source and available under the MIT License. Feel free to modify and distribute it as needed.


