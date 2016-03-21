---
layout: page
title: Contact
permalink: /contact/
comments: false
---

<form action="https://formspree.io/jus@envyserve.com"
      method="POST">
   Name: <input type="text" name="name">
   Email: <input type="email" name="_replyto">
    <input type="submit" class="smallbutton lightgray left" value="Send">
</form>


<form id="contact_form" action="https://formspree.io/jus@envyserve.com" method="POST">
	<div class="row">
		<label for="name">Your name:</label><br />
		<input id="name" class="input" name="name" type="text" value="" size="30" /><br />
	</div>
	<div class="row">
		<label for="email">Your email:</label><br />
		<input id="email" class="input" name="email" type="text" value="" size="30" /><br />
	</div>
	<div class="row">
		<label for="message">Your message:</label><br />
		<style>.texarea { padding: 8px 15px;
    background: #fff;
    border: 2px solid #808080;
    font: 600 15px 'Open Sans', Serif;
    border-radius: 4px 4px;
    }</style>
    <textarea id="message" class="input" name="message" rows="7" cols="30"></textarea><br />
	</div>
	<input id="submit_button" type="submit" value="Send email" />
</form>				
