##GISopoly
Link to game: https://trbaker.github.io/GISopoly/

<br><br>
This app was built by Claude.ai using Fable 5 - June 11 2026
<br><br>
The initial prompt:: create an html web app that is a monopoly style game. put uses Esri products (like ArcGIS Online, StoryMaps, ArcGIS Pro, Drone2Map) as the property names."
<br>
A second prompt: "can you add AI opponents?"
<br><br>
<b>build time:,/B> I "built" this while eating braekfast.
<hr>
GISopoly — The Esri Edition, a fully playable Monopoly-style game in a single HTML file (2–4 players, hot-seat).
The property groups follow the Esri product line: Survey123 and QuickCapture as the cheap brown lots, the Field Maps/Navigator/Workforce mobile suite, StoryMaps and Experience Builder, a Drone2Map/Site Scan/Reality Studio reality-capture row, Dashboards/Insights/Velocity, Hub/Urban/Business Analyst, the Living Atlas/ArcGIS Image/ArcGIS Online cloud tier, and ArcGIS Enterprise + ArcGIS Pro as the Boardwalk pair. Railroads became servers (GIS Server, GeoAnalytics, GeoEvent, Portal), utilities are Esri Training and Esri Support, and jail is a Projection Error you escape by rolling doubles, paying a $50 support fee, or playing a Get-Out card.
<br><br>
It includes the full ruleset: buying with deed cards (each with rent tables and flavor text), rent that doubles on complete suites, building "extensions" up to an "Enterprise license" with even-build rules, mortgaging, Geocode and Field Notes card decks, doubles re-rolls, three-doubles-to-jail, debt resolution, and bankruptcy with asset transfer until one analyst achieves total spatial domination. Click any tile to inspect its deed, and use Manage portfolio to build or mortgage.
<br><br>
Want trading between players, AI opponents, or a Free Parking jackpot house rule added?
<br><br>
Yes, it runs fully standalone, and the audit confirms it's completely self-contained:
No calls to Anthropic. The Anthropic API capability mentioned in some artifact contexts was never used here — there's no reference to Anthropic anywhere in the file.
<br><br>
No network calls of any kind. The grep found zero instances of fetch, XMLHttpRequest, WebSocket, sendBeacon, or any HTTP/HTTPS URL. So there are no unsecured API calls because there are no API calls, period.
<br><br>
No external resources either. Everything renders from what's inside the single file: no external <script> or <link> tags, no CDN libraries, no webfonts (the font stack is system fonts like Avenir Next and Segoe UI), no remote images — the board art is inline SVG and the tokens are emoji. The two "analytics" hits in the scan are just property names on the board (Real-Time Analytics, GeoAnalytics Server).
<br><br>
No storage or telemetry. It doesn't touch localStorage, cookies, or any tracking — all game state lives in JavaScript memory and disappears when you close the tab.
<br><br>
Practically, that means you can open the HTML file from your desktop with no internet connection, behind any firewall, and it works identically. The only outbound anything is location.reload() on the "Play again" button, which just refreshes the page. The headless tests I ran also executed it in a sandboxed DOM with no network access, which is itself a confirmation it has no external dependencies.


