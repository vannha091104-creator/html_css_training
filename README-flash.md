Flash, Video & Audio
HTML provides different ways to add multimedia such as animations, video, and audio to web pages.
How Flash Works
Flash is a technology used to create animations, video, and audio for websites.
Flash Files: Flash content is called Flash movies.
Created using Flash software (Adobe Flash)
Saved as .fla (source file)
Exporting Flash: The .fla file is exported to .swf format.
.swf is the file used on web pages
It contains the final animation or media
Displaying Flash: To view Flash content, browsers needed a plugin called Flash Player.
Flash content was embedded into web pages
Traditionally used <object> or <embed>
Later, JavaScript was commonly used
Limitations:
Requires browser plugin (Flash Player)
Not supported on many mobile devices
Now deprecated and no longer used
Used in the past to add interactive multimedia (animation, video, audio) to websites.







Use Of Flash
Flash was widely used to create animations and multimedia content on websites.
Part Usage:
Initially used for animations
Later used for video, audio, and full websites
Very popular in early web development
Decline of Flash: Several factors led to the decrease in Flash usage:
JavaScript libraries (e.g., jQuery) made animations easier
Mobile devices (iPhone, iPad) did not support Flash
Accessibility issues (not suitable for all users)
Modern Shift:
Browsers now support HTML5 <video> and <audio>
No need for plugins like Flash Player
More developers are switching to HTML5
Flash is now deprecated and rarely used in modern websites.
Previously used to create interactive and multimedia web content, now replaced by HTML5 technologies.









Timeline : Flash, Video & Audio
Web technologies for animation, video, and audio have evolved rapidly over time.
Early Development (1995–2003):
Flash became popular for animations
RealAudio enabled audio streaming
RealVideo enabled video streaming
Flash later supported both audio and video
Growth of Video Platforms (2004–2011):
Vimeo and YouTube launched
Provided alternatives to self-hosting media
Introduced easier video sharing and embedding
Browser Evolution:
Browsers (Chrome, Firefox, Safari, IE) introduced HTML5 <video> and <audio>
Reduced need for plugins like Flash
Impact of Apple Devices:
iPhone (2007) and iPad (2010) did not support Flash
Accelerated the shift to HTML5
JavaScript Libraries:
Libraries like jQuery, Prototype made animations easier without Flash
Modern Trend:
HTML5 replaces Flash for multimedia
No plugins required
Better compatibility across devices
Shows the evolution from Flash-based multimedia to modern HTML5 solutions.





Adding a Flash Movie to Your Web Page
Web technologies for animation, video, and audio have evolved rapidly over time.
Early Development (1995–2003):
Flash became popular for animations
RealAudio enabled audio streaming
RealVideo enabled video streaming
Flash later supported both audio and video
Growth of Video Platforms (2004–2011):
Vimeo and YouTube launched
Provided alternatives to self-hosting media
Introduced easier video sharing and embedding
Browser Evolution:
Browsers (Chrome, Firefox, Safari, IE) introduced HTML5 <video> and <audio>
Reduced need for plugins like Flash
Impact of Apple Devices:
iPhone (2007) and iPad (2010) did not support Flash
Accelerated the shift to HTML5
JavaScript Libraries:
Libraries like jQuery, Prototype made animations easier without Flash
Modern Trend:
HTML5 replaces Flash for multimedia
No plugins required
Better compatibility across devices
Shows the evolution from Flash-based multimedia to modern HTML5 solutions.





Understanding Video Formats and Players
To add video to a website, you need to understand formats and players/plugins.
Video Formats:
Videos come in many formats (MP4, WebM, Ogg, etc.)
Browsers support different formats
Videos may need to be encoded into multiple formats
Ensures compatibility across browsers
Players / Plugins:
Older browsers required plugins (e.g., Flash Player)
Each plugin supported limited formats
Modern browsers support HTML5 <video>
No plugin required
Approach:
Hosted services (recommended):
Use platforms like YouTube or Vimeo
Easy to use and widely supported
Self-hosted:
More control over video
Need to provide multiple formats (e.g., MP4 + WebM)
Ensures videos can be played across different browsers and devices.







Using Hosted Video Services
The easiest way to add a video to your site is to upload it to a hosted service like YouTube or Vimeo.
Advantages:
Hosted services provide video players compatible with most browsers.
No need to encode videos manually; platforms convert formats automatically.
Saves bandwidth costs since videos are hosted externally.
Disadvantages:
Videos are also available on the hosting platform (not exclusive to your site).
Limited control (e.g. ads, branding, restrictions).
Some services may overlay ads or reduce video quality.
Alternative:
Host videos on your own server.
Use HTML5 <video> or older technologies (Flash).
Often requires multiple formats (e.g. MP4, WebM) for compatibility.










Preparing a Flash Video for Your Site
There are three main steps to add a Flash video to a web page.
Convert Video to FLVL:
Video must be converted to FLV format to work with Flash.
Flash provides a built-in Flash Video Encoder.
Some players also support H264 format.
External tools can be used to convert videos (FLV/H264 converters).
Find an FLV Player: 
A Flash video player is required to play the video.
It provides controls like play, pause, etc.
No need for Flash authoring software to use these players.
Embed Player & Video: 
Use JavaScript (e.g. SWFObject) to embed the player.
Specify the video file location for playback.
Some players support:
Playlists
Preview images before playback









Adding a Flash Video to Your Pages
This example uses the OS FLV player to display a video (puppy.flv).
Using SWFObject:
Flash video is embedded using SWFObject (JavaScript).
It replaces an HTML element with the video player.
Passing Data to Flash: 
Flash players often need additional information (e.g. video path).
This is passed using JavaScript variables: 
var flashvars = {};
var params = { movie: "../videos/puppy.flv" };
Key Points: 
flashvars: used to pass extra data (empty in this example).
params: contains the path to the video file.
SWFObject uses these values to load and play the video.










HTML5: Preparing Video for Your Pages
HTML5 Video Limitation:
At the time of writing, HTML5 <video> does not support DRM.
DRM (Digital Rights Management) is used for copy protection.
This can be a limitation for protected content.
WebM Support: 
Supported by:
Android
Chrome
Firefox
Opera
Helps reduce the number of video formats needed.
Browser Support:
Chrome, Firefox, Opera support WebM.
Flash players can support:
H264
WebM
Different browsers support different formats
Problems with Flash Players: 
Can behave inconsistently:
Menus may drop over video
Layout breaks when resizing window
HTML5 <video> helps solve these issues.






HTML5: Adding Video to Your Pages
src: Specifies the path to the video file.
poster:
Specifies an image to show before the video plays.
Also shown while the video is downloading.

preload:
Tells the browser how the video should be loaded when the page loads.
Values:
none: do not load video
metadata: load only basic info (duration, size…)
auto: load the whole video
width & height: Specify the size of the video player (in pixels).
controls: Displays default video controls (play, pause, volume…).
autoplay: Video will start automatically when the page loads.
loop: Video will repeat continuously.
HTML5: Multiple Video Sources
The <source> element is used inside the <video> tag to specify video files, it replaces the src attribute and allows multiple video formats.
Key Attributes:
src: Path to the video file
type: Video format (e.g., video/mp4)
codecs: Specifies encoding (optional but recommended)




HTML5: Combining Flash & HTML5 Video
To ensure maximum compatibility, videos can be provided in both HTML5 and Flash formats.
This allows most users to view the video regardless of browser support.
HTML5 video can be used as the primary option
Flash video can be used as a fallback
Or vice versa, depending on requirements
Some Flash players support H.264 encoding.
In this case, you only need: H.264(MP4), WebM
When working with HTML5 video, you can:
Create custom playback controls
Provide different video versions for different screen sizes
Trigger actions on the page at specific video times
Combining HTML5 and Flash:
Improves compatibility across browsers
Reduces format requirements (with H.264 support)
Enables more advanced features using HTML5
Adding Audio to Web Pages
The most common audio format on the web is MP3.
There are three main ways to add audio to a web page.
Use a Hosted Service:
Upload audio to platforms like SoundCloud
Embed their audio player into your page
Easy to use and widely supported
Use Flash:
Flash players can play MP3 files
Can provide advanced features (playlists, controls)
More complex and now outdated
Use HTML5:
HTML5 introduces the <audio> element
Browsers provide built-in audio controls
Similar to the <video> element
Adding a Flash MP3 Player
There are many pre-built Flash MP3 players available online
Each player offers different features, so you should choose based on your needs.
A Flash MP3 player is embedded into a web page using JavaScript (SWFObject)
The player needs to know the path to the MP3 file
Using SWFObject
Two JavaScript variables are required:
var flashvars = {};
var params = {
  mp3: "music/noise.mp3"
};
Explanation:
flashvars: Required by SWFObject (can be empty)
params: Contains configuration data
mp3: Specifies the path to the audio file
These variables are passed into the SWFObject function to embed the MP3 player into the page.
Flash MP3 players provide ready-made audio solutions
They require JavaScript integration
Now mostly replaced by HTML5 <audio>



HTML5: Adding HTML5 Audio to Your Pages
HTML5 introduced the <audio> element to add audio to web pages.
Different browsers support different audio formats.
Key Attributes:
src: Path to the audio file
controls: Displays audio controls
autoplay: Plays audio automatically
loop: Repeats audio after finishing
preload: Defines how the audio loads
Preload Values:
none: Do not load audio
auto: Load entire audio
metadata: Load only basic info
Not all browsers support the same formats
Example: OGG works in Chrome/Firefox, but not in Safari/IE
You may need to provide multiple formats
<audio> is the modern way to add sound
Provides built-in controls
More flexible than Flash
HTML5: Multiple Audio Sources
The <source> element is used inside the <audio> tag to provide multiple audio files.
This improves compatibility because different browsers support different formats.
Key Attributes: 
src: Path to the audio file
type: Specifies the audio format (optional but recommended)
<source> allows multiple audio formats
Improves browser compatibility
Always include fallback content

Summary Flash, Video & Audio
Flash allows you to add animations, video and audio to the web.
Flash is not supported on iPhone or iPad.
HTML5 introduces new <video> and <audio> elements for adding video and audio to web pages, but these are only supported in the latest browsers.
Browsers that support the HTML5 elements do not all support the same video and audio formats, so you need to supply your files in different formats to ensure that everyone can see/hear them.
