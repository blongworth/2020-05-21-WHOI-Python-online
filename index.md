---
layout: workshop      # DON'T CHANGE THIS.
# More detailed instructions (including how to fill these variables for an
# online workshop) are available at
# https://carpentries.github.io/workshop-template/customization/index.html
venue: "Woods Hole Oceanographic Institution (online)"        # brief name of the institution that hosts the workshop without address (e.g., "Euphoric State University")
address: "Zoom link: "      # full street address of workshop (e.g., "Room A, 123 Forth Street, Blimingen, Euphoria"), videoconferencing URL, or 'online'
country: "us"      # lowercase two-letter ISO country code such as "fr" (see https://en.wikipedia.org/wiki/ISO_3166-1#Current_codes) for the institution that hosts the workshop
language: "en"     # lowercase two-letter ISO language code such as "fr" (see https://en.wikipedia.org/wiki/List_of_ISO_639-1_codes) for the
latitude: "41"        # decimal latitude of workshop venue (use https://www.latlong.net/)
longitude: "-70"       # decimal longitude of the workshop venue (use https://www.latlong.net)
humandate: "May 21, 2020"    # human-readable dates for the workshop (e.g., "Feb 17-18, 2020")
humantime: "8:45 am - 12:30 pm EDT"    # human-readable times for the workshop (e.g., "9:00 am - 4:30 pm")
startdate: 2020-05-21      # machine-readable start date for the workshop in YYYY-MM-DD format like 2015-01-01
enddate: 2020-05-21        # machine-readable end date for the workshop in YYYY-MM-DD format like 2015-01-02
instructor: ["Amber York"] # boxed, comma-separated list of instructors' names as strings, like ["Kay McNulty", "Betty Jennings", "Betty Snyder"]
helper: ["Karen Soenen, Brett Longworth, Stace Beaulieu"]     # boxed, comma-separated list of helpers' names, like ["Marlyn Wescoff", "Fran Bilas", "Ruth Lichterman"]
email: ["adyork@whoi.edu"]    # boxed, comma-separated list of contact email addresses for the host, lead instructor, or whoever else is handling questions, like ["marlyn.wescoff@example.org", "fran.bilas@example.org", "ruth.lichterman@example.org"]
collaborative_notes:  # optional: URL for the workshop collaborative notes, e.g. an Etherpad or Google Docs document (e.g., https://pad.carpentries.org/2015-01-01-euphoria)
eventbrite:           # optional: alphanumeric key for Eventbrite registration, e.g., "1234567890AB" (if Eventbrite is being used)
---

{% comment %} See instructions in the comments below for how to edit specific sections of this workshop template. {% endcomment %}

{% comment %}
HEADER
Edit the values in the block above to be appropriate for your workshop.
If the value is not 'true', 'false', 'null', or a number, please use
double quotation marks around the value, unless specified otherwise.
And run 'make workshop-check' *before* committing to make sure that changes are good.
{% endcomment %}


{% comment %}
Check DC curriculum
{% endcomment %}

{% if site.carpentry == "dc" or site.carpentry == "dc" %}
{% unless site.curriculum == "dc-ecology" or site.curriculum == "dc-genomics" or site.curriculum == "dc-socsci" or site.curriculum == "dc-geospatial" %}
<div class="alert alert-warning">
It looks like you are setting up a website for a Data Carpentry curriculum but you haven't specified the curriculum type in the <code>_config.yml</code> file (current value in <code>_config.yml</code>: "<strong>{{ site.curriculum }}</strong>", possible values: <code>dc-ecology</code>, <code>dc-genomics</code>, <code>dc-socsci</code>, or <code>dc-geospatial</code>). After editing this file, you need to run <code>make serve</code> again to see the changes reflected.
</div>
{% endunless %}
{% endif %}

<h2 id="general">General Information</h2>

{% comment %}
INTRODUCTION
Edit the general explanatory paragraph below if you want to change
the pitch.
{% endcomment %}

{% if site.carpentry == "swc" %}
{% include swc/intro.html %}
{% elsif site.carpentry == "dc" %}
{% include dc/intro.html %}
{% elsif site.carpentry == "lc" %}
{% include lc/intro.html %}
{% endif %}

Are you tired of hand-editing your data to fix errors and formatting issues? Harness the power of regular expressions (regex) to search, match, and manipulate your data.

Whether you are new to regular expressions or would like an overview of capabilities to level up your regex game, this workshop is for you! No programming experience is required. These skills can be implemented in many programming languages, text editors, and the command line.  

{% comment %}
AUDIENCE
Explain who your audience is.  (In particular, tell readers if the
workshop is only open to people from a particular institution.
{% endcomment %}

{% if site.carpentry == "swc" %}
{% include swc/who.html %}
{% elsif site.carpentry == "dc" %}
{% include dc/who.html %}
{% elsif site.carpentry == "lc" %}
{% include lc/who.html %}
{% endif %}

<p>This workshop is targeted towards the technical WHOI staff in order to improve project efficiency and build technical skills.
It will only be held for 10 people at a time through an online Zoom meeting.  Registration is required. Please contact <a href='mailto:stace@whoi.edu'>stace@whoi.edu</a> for availability.</p>
<p>Workshop sponsorship: WHOI Academic Programs Doherty Award and a DDVPR Technical Staff Training Award.</p>

{% comment %}
LOCATION
{% endcomment %}

{% comment %}
DATE
This block displays the date and links to Google Calendar.
{% endcomment %}

{% comment %}
{% if page.humandate %}
<p id="when">
  <strong>When:</strong>
  {{page.humandate}}.
  {% include workshop_calendar.html %}
</p>
{% endif %}
{% endcomment %}

{% if page.humandate %}
<p id="when">
  <strong>When:</strong>
  {{page.humandate}}
</p>
{% endif %}

{% comment %}

SPECIAL REQUIREMENTS

Modify the block below if there are any special requirements.
{% endcomment %}


<p id="requirements">
  <strong>Requirements:</strong> 

<ul>
  <li> A desktop or laptop computer.</li>
  <li> Participants will need to join a Zoom video conference. Installing free zoom conference software is recommended.  You will not need a paid account. See <a href="https://support.zoom.us/hc/en-us/articles/201362193-Joining-a-Meeting">Joining a meeting from Zoom Help Center</a></li>
  <li> A web browser. Students will use a free, online regular expression editor (e.g. https://regex101.com/)</li>
  <li> No other software or operating system required.</li>
</ul>  

</p>

<p id="requirements">
  <strong>Handouts:</strong> 
These are not required materials but they are useful for reference. 
<ul>
<li><a href="http://www.qa-distiller.com/files/CheatSheet.pdf">Regular Expression Cheat Sheet (PDF)</a> from qa-distiller.com. If you have access to a printer it would be useful to print this for reference during the workshop.</li>
<li>More detailed <a href="https://cheatography.com/davechild/cheat-sheets/regular-expressions/pdf_bw/">Regular Expression Cheat Sheet (PDF)</a> by Dave Child from <a href="https://cheatography.com/davechild/cheat-sheets/regular-expressions/">Regex page on cheatography.com</a>.  This cheat sheet has more detail than you will need in this workshop.</li>
</ul>
<p>

{% comment %}
ACCESSIBILITY
Modify the block below if there are any barriers to accessibility or
special instructions.
{% endcomment %}

<p id="accessibility">
  <strong>Accessibility:</strong>
{% if online == "false" %}
  We are committed to making this workshop
  accessible to everybody. The workshop organizers have checked that:
</p>
<ul>
  <li>The room is wheelchair / scooter accessible.</li>
  <li>Accessible restrooms are available.</li>
</ul>
<p>
  Materials will be provided in advance of the workshop and
  large-print handouts are available if needed by notifying the
  organizers in advance.  If we can help making learning easier for
  you (e.g. sign-language interpreters, lactation facilities) please
  get in touch (using contact details below) and we will
  attempt to provide them.
{% else %}
  We are dedicated to providing a positive and accessible learning environment for all. Please
  notify the instructors in advance of the workshop if you require any accommodations or if there is
  anything we can do to make this workshop more accessible to you.
</p>
{% endif %}

{% comment %}
CONTACT EMAIL ADDRESS

Display the contact email address set in the configuration file.
{% endcomment %}
<p id="contact">
  <strong>Contact</strong>:
  Please email
  {% if page.email %}
  {% for email in page.email %}
  {% if forloop.last and page.email.size > 1 %}
  or
  {% else %}
  {% unless forloop.first %}
  ,
  {% endunless %}
  {% endif %}
  <a href='mailto:{{email}}'>{{email}}</a>
  {% endfor %}
  {% else %}
  to-be-announced
  {% endif %}
  for more information.
</p>

<hr/>

<h2 id="why-regex">Why should I learn regular expressions?</h2>
<ul>
  <li>If you have ever had to clean a dataset to change timestamps in various formats into one consistent format, regex is for you.</li>
  <li> If you have had to comb through data files to find all abundance values next to a specific set of specific species identifiers, regex is for you.</li>
  <li> If you have had to make repetitive changes to data in flat files, regex is for you.</li>
</ul>
<p>
Regular expressions can seem like a mysterious super-power but there is no need to be intimidated. We are going to go through this together.  Once you get a handle on them they can make life a lot easier for you!
</p>

<center>
<figure>
  <a href="https://xkcd.com/208/" target="_blank"><img src="https://imgs.xkcd.com/comics/regular_expressions.png" alt="Regular expression xkcd comic" style="width:60%">
  <figcaption><img alt="Creative Commons License" style="border:none;height=10px" src="http://creativecommons.org/images/public/somerights20.png"> by xkcd https://xkcd.com/208/</figcaption>
</a>
</figure>
</center>

{% comment %}

SYLLABUS

Show what topics will be covered.

1. If your workshop is R rather than Python, remove the comment
around that section and put a comment around the Python section.
2. Some workshops will delete SQL.
3. Please make sure the list of topics is synchronized with what you
intend to teach.
4. You may need to move the div's with class="col-md-6" around inside
the div's with class="row" to balance the multi-column layout.

This is one of the places where people frequently make mistakes, so
please preview your site before committing, and make sure to run
'tools/check' as well.
{% endcomment %}

{% comment %}


{% if site.carpentry == "swc" %}
{% include swc/syllabus.html %}
{% elsif site.carpentry == "dc" %}
{% include dc/syllabus.html %}
{% elsif site.carpentry == "lc" %}
{% include lc/syllabus.html %}
{% endif %}

<hr/>
{% endcomment %}

<h2 id="syllabus">Syllabus</h2>

<p>Syllabus pending. This workshop will use content from the <a href="https://librarycarpentry.org/lc-data-intro/01-regular-expressions/">Library Carpentry Regular Expression lesson.</a> See <a href="https://carpentries.org/">https://carpentries.org/</a> for more information about the Carpentries organization. </p>

<p>
Participants will receive an overview of regular expression capabilities and where they can be used (languages, command line, text-editors, etc.). 
</p>
<p>
We will cover regular expression patterns and syntax as well as strategies for forming regular expression patterns.  Using an online regular expression editor we will see in real-time how our patterns match and manipulate data.  
</p>
<p>
Participants will be given exercises to practice regular expression skills.

{% comment%}
CODE OF CONDUCT
{% endcomment %}
<h2 id="code-of-conduct">Code of Conduct</h2>

<p>
We will be using the Carpentries code of conduct for this workshop.  
</p>
<p>Everyone who participates in this workshop is required to conform to the <a href="https://docs.carpentries.org/topic_folders/policies/code-of-conduct.html">Code of Conduct</a>. 
</p>

{% comment %}
<p>This document also outlines how to report an incident if needed.</p>
<p class="text-center">
  <a href="https://goo.gl/forms/KoUfO53Za3apOuOK2">
    <button type="button" class="btn btn-info">Report a Code of Conduct Incident</button>
  </a>
</p>
{% endcomment %}

<hr/>


{% comment %}
Collaborative Notes

If you want to use an Etherpad, go to

https://pad.carpentries.org/YYYY-MM-DD-site

where 'YYYY-MM-DD-site' is the identifier for your workshop,
e.g., '2015-06-10-esu'.

Note we also have a CodiMD (the open-source version of HackMD)
available at https://codimd.carpentries.org
{% endcomment %}
{% if page.collaborative_notes %}
<h2 id="collaborative_notes">Collaborative Notes</h2>

<p>
We will use this <a href="{{ page.collaborative_notes }}">collaborative document</a> for chatting, taking notes, and sharing URLs and bits of code.
</p>
<hr/>
{% endif %}


{% comment %}
SURVEYS - DO NOT EDIT SURVEY LINKS
{% endcomment %}
<h2 id="surveys">Surveys</h2>

<p>Please be sure to complete these surveys before and after the workshop.  If you aleady filled out a survey for the WHOI workshop on May 22nd, you don't have to fill this out again.</p>
<p><a href="{{ site.pre_survey }}{{ site.github.project_title }}">Pre-workshop Survey</a></p>
<p><a href="{{ site.post_survey }}{{ site.github.project_title }}">Post-workshop Survey</a></p>

<hr/>


{% comment %}
SCHEDULE

Show the workshop's schedule.  Edit the items and times in the table
to match your plans.  You may also want to change 'Day 1' and 'Day
2' to be actual dates or days of the week.

<h2 id="schedule">Schedule</h2>
{% endcomment %}

{% if site.carpentry == "swc" %}
{% include swc/schedule.html %}
{% elsif site.carpentry == "dc" %}
{% include dc/schedule.html %}
{% elsif site.carpentry == "lc" %}
{% include lc/schedule.html %}
{% endif %}

<hr/>

</p>

{% comment %}
SETUP

{% endcomment %}

<h2 id="setup">Setup</h2>

{% comment %}
<p>
  To participate in a
  {% if site.carpentry == "swc" %}
  Software Carpentry
  {% elsif site.carpentry == "dc" %}
  Data Carpentry
  {% elsif site.carpentry == "lc" %}
  Library Carpentry
  {% endif %}
  workshop,
  you will need access to the software described below.
  In addition, you will need an up-to-date web browser.
</p>
{% endcomment %}

It is recommended that you download and install free Zoom conference software.  No other setup required.
See <a href="https://support.zoom.us/hc/en-us/articles/201362193-Joining-a-Meeting">Joining a meeting from Zoom Help Center</a>).

You will need an up-to-date web browser.

{% comment %}
<p>
  We maintain a list of common issues that occur during installation as a reference for instructors
  that may be useful on the
  <a href = "{{site.swc_github}}/workshop-template/wiki/Configuration-Problems-and-Solutions">Configuration Problems and Solutions wiki page</a>.
</p>
{% endcomment %}

{% if site.carpentry == "swc" %}
{% include swc/setup.html %}
{% elsif site.carpentry == "dc" %}
{% include dc/setup.html %}
{% elsif site.carpentry == "lc" %}
{% include lc/setup.html %}
{% endif %}
