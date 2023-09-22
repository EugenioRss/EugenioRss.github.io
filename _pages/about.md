---
# published: true
# last_modified_at: 2020-01-01T00:00:00+01:00
permalink: /about/
title: "About"
excerpt: "About me"
read_time: false
show_date: true
# toc: true
toc_label: "On this page"
toc_icon: "cogs"
---

## Information

```python
me = Person(
    name="Eugenio",
    surname="Rossini",
    birthdate=datetime.date(1994, 7, 21),
    occupation="Machine Learning Engineer",
    city="Rome",
    email=""
)
```

{: .container}
<div>
Hello!

I will write a little bio here (been saying that for years now, so don't hold your breath)...
</div>

## Contact me

<i class="fas fa-hand-point-left"></i> use these links or contact me directly here.

<!-- modify this form HTML and place wherever you want your form -->
<form
  action="https://formspree.io/f/mgepljqa"
  method="POST"
>
  <label>
    Your name:
    <input type="text" name="name">
  </label>
  <label>
    Your email:
    <input type="text" name="_replyto">
  </label>
  <label>
    Your message:
    <textarea name="message"></textarea>
  </label>

  <!-- your other form fields go here -->

  <button type="submit">Send</button>
</form>