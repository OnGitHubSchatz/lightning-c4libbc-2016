#VSLIDE

![Image-Absolute](assets/piwik.png)
### Alternative Web Analytics

<span style="font-size: 0.6em; font-style: italic; float: right;">Schatz
<br>BC Libraries Cooperative</span>

#HSLIDE
## About the project
- Self-host or Piwik Cloud
- LAMP stack
- FOSS, active on GitHub
- Privacy focus
- Contributed modules

#HSLIDE
### Privacy virtues
- Self-hosted -> data control, 1st-party cookie
- PII/SPI safeguards by default
- Honours DoNotTrack at tracker level
  - GA requires manual JS check

#HSLIDE
## Maximize User Privacy
#### by...minimizing data collected
1. Anonymize IPs after two octets 
<br> e.g. 208.55.xxx.xxx
2. Set retention period:
 * raw visitor logs for short time
 * archive into aggregated reports
3. Offer opt-out link (cookie)
4. TLS on tracker and tracked site

#HSLIDE
## Standard Metrics
Visits (Sessions), Pageviews<br>
Bounces, "Landing pages"
<br>
Visit & Action (views, events) scopes
Custom Variables, Dimensions for reports and segments

#VSLIDE
Simple custom variable tally
![Image-Absolute](assets/s3byorgtally.png)

#HSLIDE
## Dashboard
Pare down to basic wigets + customize

![Image-Absolute](assets/dashboard.png)

#HSLIDE
## Custom Dimension
<br>
###Calls tracker from:
* Admin UI: Regex on URL, page title in Action scope
* Client-side API (JS)
* Server-side (PHP)
  * Modules for Drupal/WordPress etc
* Query string param!

```JavaScript
$(".views-field-field-s3-file-upload").click(function() {
	_paq.push(['setCustomDimension', 1, 'dimensionValue']);
});
```
Then segment, no scope needed for dimensions!

#HSLIDE
## Goals /Conversions
### Outcomes you are looking for
* Session -> downloaded more than 3 items
* Session -> watched tutorial
* Referred by email -> bookmarked items for later

#HSLIDE
## Metric x Goal
![Image-Absolute](assets/socialreferrals.png)

#HSLIDE
## Data quality
### Referrer spam vs community-maintained spamlist
Does GA even care?

#VSLIDE
(No.)

#HSLIDE
More varied viz - let's build it
:shipit:
