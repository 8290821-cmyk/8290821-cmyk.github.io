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
      username: me
      text: ''
      button:
        text: Download CV
        url: uploads/resume.pdf # 确认一下这里，之前建议改成 /uploads/resume.pdf
      headings:
        about: ''
        education: ''
        interests: ''
    design:
      background:
        gradient_mesh:
          enable: true
      name:
        size: md
      avatar:
        size: medium
        shape: circle

  # 这里是你之前提到的 Research 介绍，你可以把文字改成你自己的，或者干脆也删掉这一段
  - block: markdown
    content:
      title: '📚 My Research'
      subtitle: ''
      text: |-
       I explore how virtual environments and digital characters can be designed to improve human well-being and social interaction. From investigating user behavior in VR to developing interactive prototypes for digital healthcare, my goal is to create seamless and meaningful experiences. I enjoy combining technical development with empirical user research to understand the impact of emerging technologies on users."
    design:
      columns: '1'

  # 如果你还没有发表论文，建议把下面这两个 block 也删掉，或者暂时留着
  - block: collection
    id: papers
    content:
      title: Featured Publications
      filters:
        folders:
          - publications
        featured_only: true
    design:
      view: article-grid
      columns: 2

  - block: collection
    content:
      title: Selected Works
      text: ''
      filters:
        folders:
          - publications
        exclude_featured: false
    design:
      view: citation

  # ----- 我已经帮你删掉了 Recent News 和 Recent & Upcoming Talks -----
