---
# Leave the homepage title empty to use the site title
title: ''
summary: ''
date: 2022-10-24
type: landing

design:
  # Default section spacing
  spacing: '6rem'

sections:
  - block: resume-biography-3
    content:
      # Choose a user profile to display (a folder name within `content/authors/`)
      username: me
      text: ''
      # Show a call-to-action button under your biography? (optional)
      #button:
      #  text: Download CV
      #  url: uploads/resume.pdf
      headings:
        about: ''
        education: ''
        interests: ''
    design:
      # Use the new Gradient Mesh which automatically adapts to the selected theme colors
      background:
        gradient_mesh:
          enable: true

      # Name heading sizing to accommodate long or short names
      name:
        size: md # Options: xs, sm, md, lg (default), xl

      # Avatar customization
      avatar:
        size: medium # Options: small (150px), medium (200px, default), large (320px), xl (400px), xxl (500px)
        shape: circle # Options: circle (default), square, rounded
  - block: markdown
    content:
      title: '📚 About Me'
      subtitle: ''
      text: I build high-speed perception and localization pipelines for robots and autonomous platforms, with a focus on event-based vision, neuromorphic localization, and LiDAR/IMU odometry. I enjoy working at the intersection of deep tech and strategy – turning research into deployed systems for aerospace manufacturing, autonomous racing, and beyond.
    design:
      columns: '1'
  - block: collection
    id: news
    content:
      title: News
      subtitle: ''
      text: ''
      # Page type to display. E.g. post, talk, publication...
      page_type: news
      # Choose how many pages you would like to display (0 = all pages)
      count: 2
      # Filter on criteria
      filters:
        author: ''
        category: ''
        tag: ''
        exclude_featured: false
        exclude_future: false
        exclude_past: false
        publication_type: ''
      # Choose how many pages you would like to offset by
      offset: 0
      # Page order: descending (desc) or ascending (asc) date.
      order: desc
    design:
      view: article-grid
      columns: 2
  - block: collection
    id: publications
    content:
      title: Recent Publications
      text: ""
      filters:
        folders:
          - publications
        exclude_featured: false
    design:
      view: citation
  - block: markdown
    content:
      title: '📚 Conferences'
      subtitle: ''
      text: |-
        - CVPR 2025 Workshop on Event-based Vision   
    design:
      columns: '1'
#  - block: collection
#    id: students
#    content:
#      title: 指导学生情况
#      filters:
#        folders:
#          - students
#    design:
#      view: article-grid
#      columns: 1
  - block: contact-info
    id: contact
    content:
      title: Contact
      subtitle: "Let's build something amazing together"
      text: |-
        If you are interested in collaborating, contact me!
      email: farah99removeme@icloud.com
      autolink: true
    design:
      columns: '1'
      background:
        color:
          light: "#ffffff"
          dark: "#0d0d12"
      spacing:
        padding: ["4rem", "0", "4rem", "0"]
---
