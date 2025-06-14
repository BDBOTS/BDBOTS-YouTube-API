
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>BDBots YouTube API Documentation</title>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600;700&display=swap" rel="stylesheet">
    <style>
        :root {
            --primary-color: #007bff; /* Blue */
            --secondary-color: #6c757d; /* Gray */
            --accent-color: #6f42c1; /* Purple */
            --bg-light: #f8f9fa;
            --bg-dark: #343a40;
            --text-dark: #212529;
            --text-light: #f8f9fa;
            --code-bg: #e9ecef;
            --code-border: #dee2e6;
            --border-radius: 0.375rem;
            --shadow-light: rgba(0, 0, 0, 0.05);
        }

        body {
            font-family: 'Inter', sans-serif;
            line-height: 1.6;
            color: var(--text-dark);
            background-color: #ffffff; /* White background */
            margin: 0;
            padding: 20px;
            display: flex;
            justify-content: center;
        }

        .container {
            max-width: 900px;
            width: 100%;
            background-color: #fff;
            padding: 40px;
            border-radius: var(--border-radius);
            box-shadow: 0 4px 12px var(--shadow-light);
        }

        h1, h2, h3, h4 {
            color: var(--accent-color);
            margin-top: 1.5em;
            margin-bottom: 0.8em;
            line-height: 1.2;
        }

        h1 {
            font-size: 2.8em;
            text-align: center;
            color: var(--primary-color);
            margin-bottom: 0.5em;
            font-weight: 700;
        }

        h1 + p {
            text-align: center;
            font-size: 1.2em;
            color: var(--secondary-color);
            margin-bottom: 2em;
        }

        h2 {
            font-size: 2.2em;
            border-bottom: 2px solid var(--code-border);
            padding-bottom: 0.3em;
            margin-top: 2.5em;
            color: var(--text-dark);
        }

        h3 {
            font-size: 1.8em;
            color: var(--primary-color);
            margin-top: 2em;
        }

        a {
            color: var(--primary-color);
            text-decoration: none;
            transition: color 0.2s ease-in-out;
        }

        a:hover {
            color: var(--accent-color);
            text-decoration: underline;
        }

        ul {
            list-style-type: none;
            padding: 0;
        }

        ul li {
            margin-bottom: 0.8em;
            padding-left: 1.5em;
            position: relative;
        }

        ul li::before {
            content: '👉'; /* Unicode emoji for bullet point */
            position: absolute;
            left: 0;
            color: var(--primary-color);
        }

        .features-list li::before {
            content: '✅';
        }
        .support-list li::before {
            content: '💬';
        }
        .contact-info li::before {
             content: '📞';
        }

        pre {
            background-color: var(--code-bg);
            border: 1px solid var(--code-border);
            border-left: 5px solid var(--accent-color);
            border-radius: var(--border-radius);
            padding: 1em 1.5em;
            overflow-x: auto;
            font-family: 'SFMono-Regular', Consolas, 'Liberation Mono', Menlo, Courier, monospace;
            font-size: 0.9em;
            white-space: pre-wrap; /* Ensures code wraps */
            word-wrap: break-word; /* Ensures code breaks for long lines */
            margin-bottom: 1.5em;
        }

        code {
            font-family: 'SFMono-Regular', Consolas, 'Liberation Mono', Menlo, Courier, monospace;
            background-color: var(--code-bg);
            padding: 0.2em 0.4em;
            border-radius: var(--border-radius);
            font-size: 0.875em;
            color: var(--text-dark);
        }

        hr {
            border: 0;
            height: 1px;
            background-image: linear-gradient(to right, rgba(0, 0, 0, 0), var(--code-border), rgba(0, 0, 0, 0));
            margin: 3em 0;
        }

        .api-contact-btn {
            display: inline-block;
            background-color: var(--accent-color);
            color: var(--text-light);
            padding: 0.8em 1.5em;
            border-radius: var(--border-radius);
            text-decoration: none;
            font-weight: 600;
            transition: background-color 0.2s ease-in-out, transform 0.1s ease-in-out;
            margin-top: 1em;
        }

        .api-contact-btn:hover {
            background-color: darken(var(--accent-color), 10%); /* This won't work in raw CSS, just conceptual */
            background-color: #5a369e; /* A slightly darker purple */
            transform: translateY(-2px);
            text-decoration: none;
        }

        .api-contact-btn img {
            vertical-align: middle;
            margin-right: 8px;
        }

        .logo-small {
            vertical-align: middle;
            margin-right: 5px;
            width: 20px; /* Adjust size as needed */
            height: 20px;
        }

        footer {
            text-align: center;
            margin-top: 3em;
            font-size: 0.9em;
            color: var(--secondary-color);
        }
    </style>
</head>
<body>
    <div class="container">
        <header>
            <h1>🚀 BDBots YouTube API</h1>
            <p>Effortlessly Extract YouTube Video Information & Download Links!</p>
        </header>

        <hr>

        <nav>
            <h2>📖 Table of Contents</h2>
            <ul>
                <li><a href="#key-features">Key Features</a></li>
                <li><a href="#api-usage">API Usage</a>
                    <ul>
                        <li><a href="#base-url">Base URL</a></li>
                        <li><a href="#endpoint-get-video-information">Endpoint: Get Video Information</a></li>
                        <li><a href="#example-response-structure">Example Response Structure</a></li>
                    </ul>
                </li>
                <li><a href="#support--community">Support & Community</a></li>
                <li><a href="#get-in-touch">Get in Touch</a></li>
                <li><a href="#official-website">Official Website</a></li>
                <li><a href="#copyright">Copyright</a></li>
            </ul>
        </nav>

        <hr>

        <section id="key-features">
            <h2>✨ Key Features</h2>
            <ul class="features-list">
                <li><strong>Comprehensive Metadata:</strong> Get video ID, title, author, high-quality thumbnail, and duration.</li>
                <li><strong>Multiple Formats:</strong> Access a wide array of available video (MP4, WebM) and audio (Opus, M4A) formats.</li>
                <li><strong>Quality Options:</strong> Retrieve links for various video qualities (e.g., 144p, 360p, 480p, 720p, 1080p).</li>
                <li><strong>Direct Download URLs:</strong> Obtain time-limited direct links for seamless integration into your applications.</li>
                <li><strong>Developer-Friendly:</strong> Simple GET request with a clear JSON response.</li>
            </ul>
        </section>

        <hr>

        <section id="api-usage">
            <h2>💻 API Usage</h2>

            <h3 id="base-url">Base URL</h3>
            <p>All API requests should be made to the following base URL:</p>
            <pre><code>https://yt.bdbots.xyz</code></pre>

            <h3 id="endpoint-get-video-information">Endpoint: Get Video Information</h3>
            <p>To retrieve details and download links for a YouTube video, use the <code>/dl</code> endpoint.</p>
            <ul>
                <li><strong>URL:</strong> <code>/dl</code></li>
                <li><strong>Method:</strong> <code>GET</code></li>
                <li><strong>Parameters:</strong>
                    <ul>
                        <li><code>url</code> (required): The full YouTube video URL.</li>
                        <li><strong>Example:</strong> <code>https://www.youtube.com/watch?v=AzMimnWC4rA</code></li>
                    </ul>
                </li>
            </ul>

            <h4>Example Request (using curl):</h4>
            <pre><code class="language-bash">curl -X GET "https://yt.bdbots.xyz/dl?url=https://www.youtube.com/watch?v=AzMimnWC4rA"</code></pre>

            <h3 id="example-response-structure">Example Response Structure</h3>
            <p>A successful API call will return a JSON object similar to this, containing <code>video_info</code>, <code>available_formats</code>, and <code>api_info</code>:</p>
            <pre><code class="language-json">{
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
    // ... (rest of the formats omitted for brevity)
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
}</code></pre>
        </section>

        <hr>

        <section id="support--community">
            <h2>🌐 Support & Community</h2>
            <p>Join our community and get support!</p>
            <ul class="support-list">
                <li><a href="https://bdbots.t.me/"><img src="https://www.svgrepo.com/show/447118/telegram-fill.svg" alt="Telegram Channel" class="logo-small"> Telegram Channel: https://bdbots.t.me/</a></li>
                <li><a href="https://t.me/bdbots_chat"><img src="https://www.svgrepo.com/show/447118/telegram-fill.svg" alt="Telegram Chat" class="logo-small"> Telegram Chat: https://t.me/bdbots_chat</a></li>
                <li><a href="https://github.com/bdbots"><img src="https://www.svgrepo.com/show/512317/github-142.svg" alt="GitHub Organization" class="logo-small"> Github Organization: https://github.com/bdbots</a></li>
            </ul>
        </section>

        <section id="get-in-touch">
            <h2>💰 Get in Touch</h2>
            <p>Need to buy API access, custom Telegram Bots, or specialized code? Contact us directly!</p>
            <a href="https://t.me/bdbots_bot" class="api-contact-btn">
                <img src="https://www.svgrepo.com/show/475635/telegram-fill.svg" alt="Telegram Bot" width="20" height="20">
                Contact via Telegram Bot
            </a>
        </section>

        <section id="official-website">
            <h2>🔗 Official Website</h2>
            <p>Explore more about BDBots and our services:</p>
            <p><a href="https://bdbots.xyz">bdbots.xyz</a></p>
        </section>

        <hr>

        <footer>
            <p><code>© 2025 BDBots. All rights reserved.</code></p>
        </footer>
    </div>
</body>
</html>
