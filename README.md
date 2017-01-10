# Tanager

My Junco, Grebe, Scaup, Veery, and Wren web publishing apps have the option to use a simple, JavaScript-based “editor” for creating and updating posts. 

In 2013, I started with this person’s code [borgar.github.io/textile-js](http://borgar.github.io/textile-js). 

The original JavaScript provides a Textile live preview editor. The app splits the screen within a web browser. An author writes markup in the left pane while the right pane provides a live preview of the formatted text. The brower JavaScript converted the Textile markup to HTML.

When testing the code in the summer of 2013, I found the flashing of the live preview to be annoying and distracting as I typed. I could see the live preview out of the corner of my eye.

I modified the original code a lot to support my needs. I removed the live-preview, since my web apps also support Markdown and and, at times, my own custom formatting commands. I did not want to try to add all my formatting options to client-side JavaScript. I prefer to let the server app do all of the formatting. For example, the Junco app contains Wiki functionality, which requires server-side formatting.

My version accesses the API endpoints in my web publishing apps. Using REST and JSON, the editor sends markup to the server, and it receives back the formatted HTML. 

Other functionality that I added to the editor includes a single-screen view to create a larger writing area, keyboard shortcuts, and auto-save. I also added a line of buttons across the top to switch to single screen or split screen and to save or preview a post.

The original code used jQuery. When I added my changes, I added the usage of the small minified.js framework.

I've been wanting to start over and convert the simple editor utility into vanilla JavaScript, which I have done with Tanager.

At the moment, the Tanager version is used only with my Wren publishing app. The functionality for the end-user is the same as the version(s) used with my other web publishing apps. But Tanager now consists of only one JavaScript file that is approximately 12K in size before minifying. And no frameworks are used.

"Editor" may be an inappropriate term to use describe this browser-based JavaScript tool. It's more like a gateway that uses JSON to send markup and receive HTML.

Keyboard shortcuts:

* ctrl-s = save
* ctrl-p = preview (I don't use a printer, so this is fine for me). This sends markup to the server for formatting, and then the HTML is displayed in the right pane. If writing in single-screen mode, then the screen switches to the preview also in single-screen mode.
* ctrl-j = simpler, single screen view that removes the line of buttons at the top
* ctrl-h = provides a tiny, simplified window for writing that is only five lines tall 
* ctrl-d = switches the default display from black text on white background to light grey text on a black background
* ctrl-b = return to the standard, split-screen view with the small row of buttons across the top


The editor works fine on the phone's web browser. Obviously, it's easier to write on the phone with the editor in single screen mode.


The default writing environment. The button with the arrows pointing right is used to switch to single screen mode. The button with the arrows point left is used to switch to split screen mode.

![](https://c2.staticflickr.com/6/5740/22319004206_d8d5623a12_z.jpg)


Single screen mode for writing.

![](https://c1.staticflickr.com/1/749/22319046156_c8f246cf6b_z.jpg)


Single screen mode for previewing a post.

![](https://c1.staticflickr.com/1/620/22157337188_65fa9fb1c4_z.jpg)


This is a desktop / laptop view after hitting ctrl-j to create a simplified writing environment. No buttons. 

![](https://c1.staticflickr.com/1/613/22157039920_d16dc37249_z.jpg)


This is a desktop / laptop view after hitting ctrl-d to change the default colors when using the simplified writing environment.

![](https://c1.staticflickr.com/1/675/22355736491_4b81679023_z.jpg)



This is a desktop / laptop view after hitting ctrl-h to reduce the writing window to only five lines tall.

![](https://c1.staticflickr.com/1/750/21723990313_06f7a469a0_z.jpg)



