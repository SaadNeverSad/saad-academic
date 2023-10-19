---
# An instance of the Contact widget.
widget: contact

# This file represents a page section.
headless: true

# Order that this section appears on the page.
weight: 130

title: Contact
subtitle:

content:
  # Automatically link email and phone or display as text?
  autolink: true

  # Email form provider
  form:
    provider: netlify
    formspree:
      id:
    netlify:
      # Enable CAPTCHA challenge to reduce spam?
      captcha: false

  # Contact details (edit or remove options as required)
  email: aitchikhsaad3@gmail.com
  phone: +33(0)753932345
  address:
    #street: 20 Av des Buttes de Coesmes
    city: Paris
    postcode: '75000'
    country: France
    country_code: FR

design:
  columns: '2'
---
