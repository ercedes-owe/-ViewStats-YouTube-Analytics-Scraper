# ViewStats YouTube Analytics Scraper
>This scraper gathers detailed analytics data for YouTube creators by scraping information from ViewStats.com. With just a YouTube handle or channel URL, it pulls subscriber counts, view totals, video counts, and historical performance metrics — ideal for content researchers, marketers, and analytics dashboards. It transforms raw creator data into structured insights you can use right away.

<p align="center">
  <a href="https://bitbash.dev" target="_blank">
    <img src="https://github.com/Z786ZA/Footer-test/blob/main/media/scraper.png" alt="Bitbash Banner" width="100%"></a>
</p>
<p align="center">
  <a href="https://t.me/Bitbash333" target="_blank">
    <img src="https://img.shields.io/badge/Chat%20on-Telegram-2CA5E0?style=for-the-badge&logo=telegram&logoColor=white" alt="Telegram">
  </a>&nbsp;
  <a href="https://wa.me/923249868488?text=Hi%20BitBash%2C%20I'm%20interested%20in%20automation." target="_blank">
    <img src="https://img.shields.io/badge/Chat-WhatsApp-25D366?style=for-the-badge&logo=whatsapp&logoColor=white" alt="WhatsApp">
  </a>&nbsp;
  <a href="mailto:sale@bitbash.dev" target="_blank">
    <img src="https://img.shields.io/badge/Email-sale@bitbash.dev-EA4335?style=for-the-badge&logo=gmail&logoColor=white" alt="Gmail">
  </a>&nbsp;
  <a href="https://bitbash.dev" target="_blank">
    <img src="https://img.shields.io/badge/Visit-Website-007BFF?style=for-the-badge&logo=google-chrome&logoColor=white" alt="Website">
  </a>
</p>

<p align="center" style="font-weight:600; margin-top:8px; margin-bottom:8px;">
  Created by Bitbash, built to showcase our approach to Scraping and Automation!<br>
  If you are looking for <strong>ViewStats YouTube Analytics Scraper</strong> you've just found your team — Let's Chat. 👆👆
</p>

## Introduction
The ViewStats YouTube Analytics Scraper retrieves comprehensive creator and channel statistics from ViewStats.com based on a YouTube handle or channel identifier. It’s perfect for anyone analyzing growth trends, evaluating influencers, or tracking performance metrics over time.

### What You Get From It
- Basic channel metrics: subscriber count, total views, video count, verification status.  
- Historical performance data: daily, weekly, monthly series including view and upload trends.  
- Video-level analytics: stats for long-form videos and Shorts, including views, likes, comments, upload dates.  
- Estimated monetization and revenue ranges based on channel activity.  
- Bulk processing and high-performance scraping for multiple creators in one run.

---
## Features
| Feature | Description |
|---------|-------------|
| Handle-Based Lookup | Enter a YouTube handle (e.g., `@mrbeast`) or channel ID to start scraping. |
| Rich Analytics | Retrieves subscribers, view count, video count, and rankings. |
| Historical Metrics | Offers 7-day, 28-day, 90-day, yearly, and all-time statistics for channels. |
| Video Analytics | Extracts detailed stats per video including view counts, engagement, duration, and thumbnails. |
| Revenue & Projection Estimates | Provides revenue estimates and growth projections based on performance. |
| Bulk & Concurrent Scraping | Supports multiple channels per run with optimized concurrency and retries. |
| JSON Output | Data is returned in clean, structured JSON for easy integration with dashboards or data pipelines. |

---
## What Data This Scraper Extracts
| Field Name | Field Description |
|------------|-------------------|
| id | Unique channel identifier (e.g., YouTube channel ID). |
| displayName | Channel name as displayed on YouTube. |
| handle | YouTube handle or username. |
| subscriberCount | Total number of subscribers. |
| viewCount | Lifetime view count. |
| videoCount | Number of uploaded videos. |
| verified | Whether the channel is verified. |
| country | Channel’s associated country if available. |
| bannerUrl | URL to the channel banner image. |
| avatarUrl | URL to the channel profile picture. |
| stats7, stats28, stats90, stats365 | Historical metrics over various periods (subscribers, views, uploads). |
| videoStats | Detailed list of video-level performance metrics including views, likes, comments, upload dates, and thumbnails. |
| estimatedRevenueUsd | Estimated revenue based on views and engagement. |
| globalViewsRanking, globalSubscribersRanking, countrySubscriberRanking | Aggregated rankings at global and regional levels. |

---
## Example Output
    
    {
      "id": "UCX6OQ3DkcsbYNE6H8uQQuVA",
      "displayName": "ExampleChannel",
      "handle": "examplechannel",
      "subscriberCount": 1_200_000,
      "viewCount": 250_000_000,
      "videoCount": 350,
      "verified": true,
      "country": "US",
      "bannerUrl": "https://yt3.googleusercontent.com/…",
      "avatarUrl": "https://yt3.googleusercontent.com/…",
      "stats7": [ { "date": "2025-11-20", "subscriberCountDelta": 5000, ... } ],
      "videoStats": [
        { "id": "a1B2c3D4", "title": "My Latest Video", "viewCount": 1_500_000, "likeCount": 120_000, ... }
      ],
      "estimatedRevenueUsd": 25000,
      "globalSubscribersRanking": 432,
      "countrySubscriberRanking": 12
    }

---
## Directory Structure Tree
    
    ViewStats YouTube Analytics Scraper/
    ├── src/
    │   ├── main.js
    │   ├── scraper/
    │   │   ├── channel_scraper.js
    │   │   ├── historical_stats_parser.js
    │   │   └── video_data_parser.js
    │   ├── utils/
    │   │   ├── request_manager.js
    │   │   ├── concurrency_controller.js
    │   │   └── output_formatter.js
    │   └── config/
    │       └── settings.example.json
    ├── data/
    │   ├── sample_input.json
    │   └── sample_output.json
    ├── package.json
    └── README.md

---
## Use Cases
- **Marketers & agencies** vet influencer channels and track performance for campaign planning.  
- **Content creators** benchmark growth metrics against competitors.  
- **Researchers** study YouTube growth trends or perform sociological analysis on creator economics.  
- **Platform analysts** monitor changes in channel metrics over time for trend detection.  
- **Developers** feed structured channel and video metrics into dashboards, ML models, or reporting tools.  

---
## FAQs

**What input does the scraper require?**  
Provide a YouTube handle (e.g., `@channelName`) or channel ID as input.  

**Can I scrape multiple channels at once?**  
Yes — the scraper supports processing multiple creators in a single run.  

**What output format is supported?**  
Results are returned in structured JSON format, ready for analysis or storage.  

**Does it include historical data?**  
Yes — it includes various historical metrics such as weekly, monthly, quarterly and all-time stats.  

---
### Performance Benchmarks and Results

**Primary Metric:**  
Retrieves full channel analytics within a few seconds per channel under typical conditions.  

**Reliability Metric:**  
Features built-in retry logic and concurrency controls to handle site performance, with a high stability rate.  

**Efficiency Metric:**  
Efficiently processes multiple channels in parallel with minimal overhead thanks to optimized request handling.  

**Quality Metric:**  
Produces comprehensive, detailed, and accurate creator data with minimal missing fields, making it suitable for analytics, dashboards, and long-term tracking.  


---


<p align="center">
<a href="https://calendar.app.google/74kEaAQ5LWbM8CQNA" target="_blank">
  <img src="https://img.shields.io/badge/Book%20a%20Call%20with%20Us-34A853?style=for-the-badge&logo=googlecalendar&logoColor=white" alt="Book a Call">
</a>
  <a href="https://www.youtube.com/@bitbash-demos/videos" target="_blank">
    <img src="https://img.shields.io/badge/🎥%20Watch%20demos%20-FF0000?style=for-the-badge&logo=youtube&logoColor=white" alt="Watch on YouTube">
  </a>
</p>
<table>
  <tr>
    <td align="center" width="33%" style="padding:10px;">
      <a href="https://youtu.be/MLkvGB8ZZIk" target="_blank">
        <img src="https://github.com/Z786ZA/Footer-test/blob/main/media/review1.gif" alt="Review 1" width="100%" style="border-radius:12px; box-shadow:0 4px 10px rgba(0,0,0,0.1);">
      </a>
      <p style="font-size:14px; line-height:1.5; color:#444; margin:0 15px;">
        "Bitbash is a top-tier automation partner, innovative, reliable, and dedicated to delivering real results every time."
      </p>
      <p style="margin:10px 0 0; font-weight:600;">Nathan Pennington
        <br><span style="color:#888;">Marketer</span>
        <br><span style="color:#f5a623;">★★★★★</span>
      </p>
    </td>
    <td align="center" width="33%" style="padding:10px;">
      <a href="https://youtu.be/8-tw8Omw9qk" target="_blank">
        <img src="https://github.com/Z786ZA/Footer-test/blob/main/media/review2.gif" alt="Review 2" width="100%" style="border-radius:12px; box-shadow:0 4px 10px rgba(0,0,0,0.1);">
      </a>
      <p style="font-size:14px; line-height:1.5; color:#444; margin:0 15px;">
        "Bitbash delivers outstanding quality, speed, and professionalism, truly a team you can rely on."
      </p>
      <p style="margin:10px 0 0; font-weight:600;">Eliza
        <br><span style="color:#888;">SEO Affiliate Expert</span>
        <br><span style="color:#f5a623;">★★★★★</span>
      </p>
    </td>
    <td align="center" width="33%" style="padding:10px;">
      <a href="https://youtu.be/m-dRE1dj5-k?si=5kZNVlKsGUhg5Xtx" target="_blank">
        <img src="https://github.com/Z786ZA/Footer-test/blob/main/media/review3.gif" alt="Review 3" width="100%" style="border-radius:12px; box-shadow:0 4px 10px rgba(0,0,0,0.1);">
      </a>
      <p style="font-size:14px; line-height:1.5; color:#444; margin:0 15px;">
        "Exceptional results, clear communication, and flawless delivery. <br>Bitbash nailed it."
      </p>
      <p style="margin:1px 0 0; font-weight:600;">Syed
        <br><span style="color:#888;">Digital Strategist</span>
        <br><span style="color:#f5a623;">★★★★★</span>
         </p>
