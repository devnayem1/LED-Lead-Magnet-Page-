LED SOLUTIONS — COMMERCIAL LIGHTING SAVINGS PAGE
Editing + launch guide (no coding needed)

ONE FILE = THE WHOLE PAGE
-------------------------
index.html contains the design, the behaviour and the content. Everything you
will ever want to change is in ONE block near the top of the file, between the
comment lines:

    EDIT HERE — ALL CONTENT LIVES IN THIS ONE BLOCK
    window.LEDS_CONFIG = { ... }

Only change text that sits inside "quote marks". Do not delete commas, brackets
or braces. Open the file in any text editor (Notepad, VS Code), save, upload.
It does NOT need shared.css. The other pages (02–09) still use shared.css.


LAUNCH CHECKLIST (do these 5 things, in this order)
---------------------------------------------------
[ ] 1. FORM ENDPOINT  (section 2 in the config)
       Create a free form on Formspree.io (or Web3Forms, Getform, or use a
       Zapier/Make webhook or your CRM's form URL). Copy the URL they give you
       and paste it here:   endpoint: "https://formspree.io/f/xxxxxxx"
       Web3Forms needs a key:  extraFields: { access_key: "your-key" }
       Until this is filled in, the form opens a pre-filled email to Kieran
       instead, so no enquiry is lost, but you MUST set the endpoint before
       running ads.
[ ] 2. ANALYTICS  (section 1)
       Paste your real GTM ID (GTM-XXXXXXX) OR your GA4 ID (G-XXXXXXXXXX).
       Use one, not both. To watch events fire, set debug: true, open the page,
       press F12, open Console. Set it back to false before launch.
[ ] 3. LOGO  (section 4)
       Download the official logo from ledsolutions.com.au, upload it beside
       index.html (e.g. in a folder called assets), then set:
       logo: { src: "assets/logo.svg", alt: "LED Solutions" }
[ ] 4. CANONICAL URL
       Near the top of the file, un-comment the canonical line and put the real
       address of this page. Do not point it at the homepage.
[ ] 5. TEST
       Submit a real test enquiry on phone and desktop. Check it arrives, and
       that form_submit / generate_lead appear in GA4 or GTM Preview.


HOW TO CHANGE THINGS
--------------------
Replace the hero image ........ section 5:  hero.image.src / alt / caption
Change the hero headline ....... section 5:  hero.variants.a.headline / sub
Test a different headline ...... edit variant "b", then share the link with
                                 ?v=b on the end (e.g. yoursite.com/page/?v=b)
Move the form under the hero ... add ?form=top to the link
Change button wording .......... section 6 (updates every button at once)
Update the Google rating ....... section 7 (rating, count). Keep it current.
Update phone / email / licence . section 3
Add or edit testimonials ....... section 8. Copy one { quote, name, detail }
                                 block, paste it after a comma. REAL reviews
                                 only, word for word. The carousel arrows appear
                                 automatically when there is more than fits.
Update the case study .......... section 9. Fill in "challenge" and "results"
                                 ONLY with measured numbers supplied by the
                                 client, e.g. results: ["Energy reduction: 41%"].
                                 Add "photo": { src, alt } to show a project photo.
Add before/after photos ........ section 10. The whole "See the difference"
                                 section (and its menu link) is hidden until you
                                 add at least one pair. Use real photos from the
                                 same position/angle. JPG/WebP, about 1600px
                                 wide is plenty.

Images: either paste a full web address (https://...) or upload the file next
to index.html and use its name, e.g. src: "assets/carpark-after.jpg".


WHAT THE PAGE TRACKS
--------------------
cta_click (location: header, hero, signs, case, sticky, final)
secondary_cta_click        phone_click        email_click
form_start                 form_step_complete   form_validation_error
form_submit                generate_lead        form_submit_error
before_after_interact      demo_2am_toggle      testimonial_nav
google_reviews_click
Every event also carries page_variant (a or b) so headline tests can be compared.
UTM values and gclid in the page URL are saved with each enquiry.


CONTENT THAT STILL NEEDS THE CLIENT
-----------------------------------
- Official logo file.
- Real before/after photos (the client's own Our Work page says these are
  still being collected).
- Measured results for the IRT Kangara Waters case study (energy reduction,
  payback), and permission to name the client.
- More real testimonials about energy savings and payback (only the two
  already on ledsolutions.com.au are used).
- Privacy policy URL (config: contact.privacyUrl).
- Confirm the lights-installed figure: the handoff says 57,000+, the live
  ledsolutions.com.au homepage still says 80,000+. The page uses 57,000+.
  To change it, search index.html for "57,000+".

Photos currently on the page are hosted on ledsolutions.com.au. For best speed,
download them and host them beside index.html.
