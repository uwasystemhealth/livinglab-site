+++
title = "Expression of Interest"
weight = 60
menuname = "Express Interest"
draft = false
+++

<form id="contactform" method="post" action="https://formspree.io/systemhealthlab@gmail.com">
	<div class="field">
		<label for="business_name">Business Name</label>
		<input type="text" name="business_name" id="business_name" placeholder="My Business" required/>
	</div>
	<div class="field">
		<label for="business_website">Business Website</label>
		<input type="text" name="business_website" id="business_website" placeholder="mybusiness.com.au"/>
	</div>
	<div class="field">
		<label for="business_mailing">Business Mailing Address</label>
		<textarea name="business_mailing" id="business_mailing" rows="4" placeholder="Ground Floor, 191 St George's Terrace, Perth WA 6000"></textarea>
	</div>
	<div class="field">
		<label for="contact_name">Contact Name</label>
		<input type="text" name="contact_name" id="contact_name" placeholder="Jane Smith" required/>
	</div>
	<div class="field">
		<label for="contact_phone">Contact Phone</label>
		<input type="text" name="contact_phone" id="contact_phone" placeholder="0412345678"/>
	</div>
	<div class="field">
		<label for="contact_email">Contact Email</label>
		<input type="email" id="contact_email" name="contact_email" placeholder="jane@mybusiness.com.au" required/>
	</div>
	<div class="field">
		<label for="project_description">Brief Project Description</label>
		<textarea name="project_description" id="project_description" rows="4" placeholder="We like to design and manufacture sensors for rocket ships." required></textarea>
	</div>
	<ul class="actions">
		<li><input type="submit" value="Submit" class="special" /></li>
	</ul>
	<input type="hidden" name="_next" value="?sent#eoi" />
	<input type="hidden" name="_subject" value="Living Lab EOI Submission" />
	<input type="text" name="_gotcha" style="display:none" />
</form>
<span id="contactformsent">Thank you for your interest, we'll be in touch shortly.</span>

<script>
$(document).ready(function($) {
    $(function(){
        if (window.location.search == "?sent") {
        	$('#contactform').hide();
        	$('#contactformsent').show();
        } else {
        	$('#contactformsent').hide();
        }
    });
});
</script>


{{< socialLinks >}}
