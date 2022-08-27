---
title: "Contact"
date: 2021-02-28T19:44:33-05:00
draft: false
page: true
hidemeta: true
---

{{< rawhtml >}}
      <script src="https://www.google.com/recaptcha/api.js?render=6LckhbIhAAAAAPg4s3RnZLYN-VLAIxznpCiw8rcQ"></script>
      <script>
          grecaptcha.ready(function () {
              grecaptcha.execute('6LckhbIhAAAAAPg4s3RnZLYN-VLAIxznpCiw8rcQ', {action: 'submit'}).then(function (token) {
                  console.info("got token: " + token);
                  document.getElementById('g-recaptcha-response').value = token;
              });
          });
      </script>

<form id="milk" accept-charset="utf-8" action="https://formspree.io/f/meqnkekz" method="post">
    <label for="full-name">Name</label>
    <input type="text" name="name" id="full-name" placeholder="First and Last" required="">
    <label for="email-address">Email Address</label>
    <input type="email" name="email" id="email-address" placeholder="email@domain.tld" required="">
    <label for="message">Message</label>
    <textarea rows="5" name="message" id="message" placeholder="" required=""></textarea>
    <input type="hidden" name="_subject" id="email-subject" value="Contact Form Submission">
    <input type="hidden" id="g-recaptcha-response" name="g-recaptcha-response">
    <input type="text" name="_gotcha" style="display:none" />
  <input type="submit" value="Submit">
  <p id="milk-status"></p>
</form>


<!-- Place this script at the end of the body tag -->
<script>
    var form = document.getElementById("milk");
    
    async function handleSubmit(event) {
      event.preventDefault();
      var status = document.getElementById("milk");
      var data = new FormData(event.target);
      fetch(event.target.action, {
        method: form.method,
        body: data,
        headers: {
            'Accept': 'application/json'
        }
      }).then(response => {
        if (response.ok) {
          status.innerHTML = "Message sent!";
          form.reset()
        } else {
          response.json().then(data => {
            if (Object.hasOwn(data, 'errors')) {
              status.innerHTML = data["errors"].map(error => error["message"]).join(", ")
            } else {
              status.innerHTML = "Oops! There was a problem submitting your form"
            }
          })
        }
      }).catch(error => {
        status.innerHTML = "Oops! There was a problem submitting your form"
      });
    }
    form.addEventListener("submit", handleSubmit)
</script>
{{< /rawhtml >}}