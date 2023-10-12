---
date: "2023-10-11"
sections:
- block: hero
  content:
    image:
      filename: omics-health.png
    text: |
      <br>

      The Omics for Health community (omics4health) endeavors to enhance communication among junior researchers within the realms of omics and human healthcare. The majority of its members comprise PhDs, Postdocs, research scientists, and junior Principal Investigators affiliated with prestigious universities and institutes (Stanford, Harvard, Tsinghua, EMBL, etc.) globally.
    title:

- block: collection
  id: post
  content:
    count: 3
    filters:
      author: ""
      category: ""
      exclude_featured: false
      publication_type: ""
      tag: ""
    offset: 0
    order: desc
    page_type: post
    subtitle: null
    text: null
    title: Latest News
  design:
    columns: "1"
    view: card

- block: collection
  id: event
  content:
    count: 3
    filters:
      author: ""
      category: ""
      exclude_featured: false
      publication_type: ""
      tag: ""
    offset: 0
    order: desc
    page_type: event
    subtitle: null
    text: null
    title: Events
  design:
    columns: "1"
    view: card
    background:
      image: 
        filename: events.jpg
        filters:
          brightness: 0.5
      #  Image fit. Options are `cover` (default), `contain`, or `actual` size.
      size: cover
      # Image focal point. Options include `left`, `center` (default), or `right`.
      position: center
      # Use a fun parallax-like fixed background effect on desktop? true/false
      parallax: true
      # Text color (true=light, false=dark, or remove for the dynamic theme color).
      text_color_light: true


- block: people
  id: people
  content:
    sort_ascending: true
    sort_by: Params.last_name
    title: Team
    subtitle: "[All Team Members](./people/)"
    # text: |-
    #   {{% callout note %}}
    #   [All team members](./people/).
    #   {{% /callout %}}
    user_groups:
    - Co-Chair
    - Committee Members
  design:
    show_interests: false
    show_role: true
    show_social: true

- block: contact
  content:
    # appointment_url: https://calendly.com
    # autolink: true
    # contact_links:
    # - icon: twitter
    #   icon_pack: fab
    #   link: https://twitter.com/xiaotaoshen1990
    #   name: Twitter
    # - icon: weixin
    #   icon_pack: fab
    #   link: https://jaspershen.github.io/image/wechat_QR.jpg
    #   name: WeChat
    email: shenxt1990@outlook.com
    form:
      formspree:
        id: xpzgpjby
      netlify:
        captcha: false
      provider: formspree
    subtitle: null
    text: 
    title: Join US
  design:
    columns: "2"
  id: contact

title: null
type: landing
---
