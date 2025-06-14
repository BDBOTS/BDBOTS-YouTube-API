BDBots YouTube API

![Alt text](https://raw.githubusercontent.com/BDBOTS/BDBOTS-YouTube-API/main/_aJLJOZKMPa5CRNZZ-iTc.png)

==================

Effortlessly Get YouTube Video Information and Download Links

The BDBots YouTube API provides a simple yet powerful interface to retrieve detailed information about YouTube videos, including their metadata (title, author, thumbnail, duration) and a comprehensive list of available download formats (video and audio) along with their direct, time-limited URLs.

Whether you're building a video downloader, a content management system, or a data analysis tool, our API offers a reliable solution for integrating YouTube video capabilities into your applications.

* * *

Table of Contents
-----------------

*   [Features](#features)
*   [API Details](#api-details)
    *   [Base URL](#base-url)
    *   [Endpoint: Get Video Information](#endpoint-get-video-information)
    *   [Example Response Structure](#example-response-structure)
*   [Contact & Support](#contact--support)
*   [Website](#website)
*   [Copyright](#copyright)

* * *

Features
--------

*   Retrieve comprehensive video metadata (ID, title, author, thumbnail, duration).
*   Access a list of all available video and audio download formats.
*   Get direct, high-quality download URLs for each format.
*   Support for various video qualities (144p to 1080p and beyond, if available).
*   Support for different audio qualities and formats (opus, m4a).

* * *

API Details
-----------

### Base URL

The base URL for all API requests is:

    https://yt.bdbots.xyz

### Endpoint: Get Video Information

This endpoint allows you to fetch details and available download links for a specific YouTube video.

*   **URL:** `/dl`
*   **Method:** `GET`
*   **Parameters:**
    *   `url` (required): The full YouTube video URL (e.g., `https://www.youtube.com/watch?v=AzMimnWC4rA`).

#### Example Request:

    curl -X GET "https://yt.bdbots.xyz/dl?url=https://www.youtube.com/watch?v=AzMimnWC4rA"

### Example Response Structure

A successful request will return a JSON object containing detailed video information and an array of available formats, each with its own download URL.

    {
      "api": "BDBots YouTube API",
      "api_url": "https://yt.bdbots.xyz",
      "timestamp": "2025-06-13T06:13:29.181004",
      "video_info": {
        "id": "AzMimnWC4rA",
        "title": "Gaibona | Sumon & Anila | Album Ekhon Ami | Official HIt Music Video",
        "author": "",
        "thumbnail": "https://i.ytimg.com/vi/AzMimnWC4rA/hq720.jpg?sqp=-oaymwEcCK4FEIIDSEbyq4qpAw4IARUAAIhCGAFwAcABBg==&rs=AOn4CLA2YFOb5XOdvK-bvfNowg7CnAZwrw",
        "duration": 253,
        "source": "youtube"
      },
      "available_formats": [
        {
          "format_id": 137,
          "type": "video",
          "extension": "mp4",
          "quality": "mp4 (1080p)",
          "url": "https://rr6---sn-uxax4vopj5qx-q0n6.googlevideo.com/videoplayback?expire=1749816807&ei=h8FLaN2zL6WJzPsPqND-2AQ&ip=176.1.144.240&id=o-AAlUBn0AG9E7uyeS1QraOIUX2foyH7neNH7O_eNYPhMs&itag=137&aitags=133%2C134%2C135%2C136%2C137%2C160%2C242%2C243%2C244%2C247%2C248%2C278%2C394%2C395%2C396%2C397%2C398%2C399&source=youtube&requiressl=yes&xpc=EgVo2aDSNQ%3D%3D&met=1749795207%2C&mh=qw&mm=31%2C29&mn=sn-uxax4vopj5qx-q0n6%2Csn-4g5e6nzl&ms=au%2Crdu&mv=m&mvi=6&pl=27&rms=au%2Cau&initcwndbps=1490000&bui=AY1jyLOVJIptEfLQ3X4FtLVcOxQf6uXBfm37XYF5j-7wZb31x2aVDpSdDIy3VnLDYaUDKnCSdtS9CteO&spc=l3OVKbxjLwmxwhrmg7Wq0HJSuutCr6oWF2XLpQGaw-GIWYjcy71v&vprv=1&svpuc=1&mime=video%2Fmp4&ns=1QXyy720t2R1nhz9p06sK00Q&rqh=1&gir=yes&clen=50574931&dur=253.360&lmt=1713842823365208&mt=1749794939&fvip=4&keepalive=yes&fexp=51331020&c=MWEB&sefc=1&txp=5532434&n=uzW6aIkQvM3Cgg&sparams=expire%2Cei%2Cip%2Cid%2Caitags%2Csource%2Crequiressl%2Cxpc%2Cbui%2Cspc%2Cvprv%2Csvpuc%2Cmime%2Cns%2Crqh%2Cgir%2Cclen%2Cdur%2Clmt&lsparams=met%2Cmh%2Cmm%2Cmn%2Cms%2Cmv%2Cmvi%2Cpl%2Crms%2Cinitcwndbps&lsig=APaTxxMwRgIhANGLwYV6e4Vi8zF7tVCTDdXCvmLRJoBpAcbYVNN0r3-3AiEArTtcWGjdt6D5Ckxgr4bch8gOrjRv0l4UJNgtICEf5jM%3D&sig=AJfQdSswRQIgWD2CpZ601JKIdR1_w0Jk-ekdFzugAssgX9zKD443IAkCIQDhwblozIgB8XHG4F6qGQpxRcCpIQs0s4EkSKVL_7MVEg%3D%3D&pot=MnQngtbXEwKkvCe-F7SpRZ6LCyfbHGI4vChE_gFez_OG2pSZM-QQhXwoTqHCyRdWAHiv2gVqKZC3Fsol2EFv-cn4jWcf4RaJHmCGJbPDRUzJQNxMuj2mkobDDH3Q1fgkaZC8mwe2PunT4BB8yYWJ4g-QvZmBNA==",
          "bitrate": 4334179,
          "width": 1920,
          "height": 1080,
          "fps": 25,
          "mime_type": "video/mp4; codecs=\"avc1.640028\"",
          "file_size": "2.07 MB"
        },
        {
          "format_id": 248,
          "type": "video",
          "extension": "webm",
          "quality": "webm (1080p)",
          "url": "https://rr6---sn-uxax4vopj5qx-q0n6.googlevideo.com/videoplayback?expire=1749816807&ei=h8FLaN2zL6WJzPsPqND-2AQ&ip=176.1.144.240&id=o-AAlUBn0AG9E7uyeS1QraOIUX2foyH7neNH7O_eNYPhMs&itag=248&aitags=133%2C134%2C135%2C136%2C137%2C160%2C242%2C243%2C244%2C247%2C248%2C278%2C394%2C395%2C396%2C397%2C398%2C399&source=youtube&requiressl=yes&xpc=EgVo2aDSNQ%3D%3D&met=1749795207%2C&mh=qw&mm=31%2C29&mn=sn-uxax4vopj5qx-q0n6%2Csn-4g5e6nzl&ms=au%2Crdu&mv=m&mvi=6&pl=27&rms=au%2Cau&initcwndbps=1490000&bui=AY1jyLOVJIptEfLQ3X4FtLVcOxQf6uXBfm37XYF5j-7wZb31x2aVDpSdDIy3VnLDYaUDKnCSdtS9CteO&spc=l3OVKbxjLwmxwhrmg7Wq0HJSuutCr6oWF2XLpQGaw-GIWYjcy71v&vprv=1&svpuc=1&mime=video%2Fwebm&ns=1QXyy720t2R1nhz9p06sK00Q&rqh=1&gir=yes&clen=31355027&dur=253.360&lmt=1713843134703834&mt=1749794939&fvip=4&keepalive=yes&fexp=51331020&c=MWEB&sefc=1&txp=5537434&n=uzW6aIkQvM3Cgg&sparams=expire%2Cei%2Cip%2Cid%2Caitags%2Csource%2Crequiressl%2Cxpc%2Cbui%2Cspc%2Cvprv%2Csvpuc%2Cmime%2Cns%2Crqh%2Cgir%2Cclen%2Cdur%2Clmt&lsparams=met%2Cmh%2Cmm%2Cmn%2Cms%2Cmv%2Cmvi%2Cpl%2Crms%2Cinitcwndbps&lsig=APaTxxMwRgIhANGLwYV6e4Vi8zF7tVCTDdXCvmLRJoBpAcbYVNN0r3-3AiEArTtcWGjdt6D5Ckxgr4bch8gOrjRv0l4UJNgtICEf5jM%3D&sig=AJfQdSswRgIhAJESCdADDGSsi0l9QtSZzG5uiHTeQlGc4IcpJ-SCDpqYAiEAwCL96M7zbJBsEhxigyrFoxDtCBjs4PSMFlWfWez87qs%3D&pot=MnQngtbXEwKkvCe-F7SpRZ6LCyfbHGI4vChE_gFez_OG2pSZM-QQhXwoTqHCyRdWAHiv2gVqKZC3Fsol2EFv-cn4jWcf4RaJHmCGJbPDRUzJQNxMuj2mkobDDH3Q1fgkaZC8mwe2PunT4BB8yYWJ4g-QvZmBNA==",
          "bitrate": 3002969,
          "width": 1920,
          "height": 1080,
          "fps": 25,
          "mime_type": "video/webm; codecs=\"vp9\"",
          "file_size": "1.43 MB"
        }
        
      ],
      "request": {
        "url": "https://www.youtube.com/watch?v=AzMimnWC4rA",
        "format": null,
        "quality": null,
        "type": null
      },
      "api_info": {
        "name": "BDBots YouTube API",
        "version": "1.1.0",
        "website": "https://yt.bdbots.xyz",
        "documentation": "https://yt.bdbots.xyz/docs",
        "copyright": "© 2025 BDBots. All rights reserved."
      }
    }

* * *

Contact & Support
-----------------

Got questions? Need custom bots or API solutions? We're here to help!

*   **Telegram Channel:** [https://bdbots.t.me/](https://bdbots.t.me/)
*   **Telegram Chat:** [https://t.me/bdbots\_chat](https://t.me/bdbots_chat)
*   **Github Organization:** [https://github.com/bdbots](https://github.com/bdbots)

### Buy API and Telegram Bots or Code

Contact us directly to discuss your needs and pricing:

[https://t.me/bdbots\_bot](https://t.me/bdbots_bot) (contact)

Website
-------

Visit our official website for more information about BDBots and our services:

[bdbots.xyz](https://bdbots.xyz)

* * *

Copyright
---------

    © 2025 BDBots. All rights reserved.
