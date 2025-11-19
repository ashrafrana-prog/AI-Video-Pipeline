**Automated AI Video Generation Workflow (n8n)**

**Overview**

This repository contains an n8n automation workflow designed to create AI-generated videos at scale using HeyGen’s API.
The flow processes user input audio, generates an avatar video, checks job status, downloads the finished video, and automatically sends it to Telegram, Discord channels.
This workflow is ideal for:
•	Marketing teams
•	Social media managers
•	Agencies producing bulk content
•	Training/educational content creators
•	Anyone needing consistent, high-quality video production with minimal manual effort
________________________________________
**Key Features**

✓ Fully automated pipeline
From input form → audio → avatar → final rendered video → publishing on channels.
✓ Bulk video generation
Submit multiple requests and let n8n produce videos automatically without human monitoring.
✓ Consistent quality
Ensures uniform branding, voice, avatar, and output settings across all videos.
✓ Time & cost savings
•	Removes the need for manual video editing
•	Cuts down hours of production work to literally minutes
•	Reduces dependency on expensive editors or voice-over artists
•	Zero repetitive work—once set up, it runs on autopilot
✓ Multi-platform delivery
Automatically posts finished videos to:
•	Telegram
•	Discord
Useful for workflows where you need immediate team review, auto-publishing, or content distribution.
________________________________________
**Workflow Structure**

Below is the logical flow of the n8n automation:
1.	Form Submission Trigger
User submits content (script, title, options, etc.)
2.	Get Audio (HeyGen API)
3.	Get Avatar
Fetches avatar ID/settings for video generation.
4.	Create Video
Posts audio + avatar info to HeyGen to start rendering.
5.	Get Video Status
Polls HeyGen until the video is fully processed.
6.	IF Node
o	If video is ready → continue
o	If not ready → Wait → Retry loop
7.	Download Video
Retrieves the final MP4 
8.	Post to Telegram
Auto-uploads the completed video.
9.	Post to Discord
Sends the video to a designated Discord channel.
________________________________________
**Benefits**

 Significant Time Savings
•	No need to manually generate audio, upload scripts, monitor rendering, or download videos.
•	Human involvement reduced from hours per video to near-zero.
 Cost Efficiency
•	Eliminates the need for video editors for simple template-based videos.
•	Automatic rendering frees teams from repetitive tasks.
•	Scales video production without hiring more resources.
 Bulk Video Production
Generate dozens—or hundreds—of videos with identical branding and quality.
Perfect for personalized marketing videos, training modules, product explainers, and social media content.
Consistency & Accuracy
•	Same avatar, same voice, same style every time
•	No human error and no quality fluctuation
________________________________________
**Requirements**
•	n8n (self-hosted or cloud)
•	HeyGen API Key
•	Telegram Bot token & Chat ID (for publishing)
•	Discord Bot webhook / Bot token (depending on setup)
________________________________________
How to Use
1.	Import the workflow JSON into n8n.
2.	Add credentials for:
o	HeyGen (HTTP API)
o	Telegram
o	Discord
4.	Enable the workflow.
5.	Submit your first form entry — the automation takes over from here.
________________________________________
License
MIT License.
Feel free to modify and use this workflow in your own automation projects.

Author:  imashraf787@gmail.com

