#VSLIDE

## Piwik
### Alternative Web Analytics

<span style="font-style: italic; float: right;">Schatz
BC Libraries Cooperative</span>

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
..* GA requires manual JS check

#HSLIDE
## Maximize Privacy in Piwik
#### by...minimizing data collected
1. Anonymize IPs after 2nd octet
	e.g. 208.55.xxx.xxx
2. Set retention period:
..*raw visitor logs for short time
..*archive into aggregated reports
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
Calls tracker from:
* Admin UI: Regex on URL, page title in Action scope
* Client-side API (JS)
* Server-side (PHP)
* Query string param!
..* Modules for PHP-based CMS

```JavaScript
$(".views-field-field-s3-file-upload span").click(function() {
	_paq.push(['setCustomDimension', 1, 'dimensionValue']);
});
```
Then Segment, no scope needed for dimensions!

#HSLIDE
## Goals /Conversions
### Outcomes you are looking for
* Logged-in and downloaded material
* Long session
* Added items to reading list

<br>
Metric x Goal

![Image-Absolute](assets/socialreferrals.png)

#HSLIDE
## Data quality
### Referrer spam vs community-maintained spamlist
Does GA even care?

#VSLIDE
(No.)

#HSLIDE
More varied viz - let's build it
