---
title: "Contact"
date: 2021-02-28T19:44:33-05:00
draft: false
page: true
hidemeta: true
---

{{< rawhtml >}}
<form id="milk" accept-charset="utf-8" action="https://formspree.io/f/meqnkekz" method="post">
    <label for="full-name">Name</label>
    <input type="text" name="name" id="full-name" placeholder="Name" required="">
    <label for="email-address">Email Address</label>
    <input type="email" name="email" id="email-address" placeholder="email@example.com" required="">
    <label for="message">Message</label>
    <textarea rows="5" name="message" id="message" placeholder="" required=""></textarea>
    <input type="hidden" name="_subject" id="email-subject" value="Contact Form Submission">
    <input type="text" name="_gotcha" tabindex="-1" class="whole-milk" />
    <button type="submit">Send</button>
</form>
{{< /rawhtml >}}