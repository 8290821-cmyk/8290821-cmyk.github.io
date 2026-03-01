---
# Leave the homepage title empty to use the site title
title: ''
summary: ''
date: 2022-10-24
type: landing

design:
  spacing: '6rem'
  

sections:
  - block: resume-biography-3
    content:
      username: me
      text: ''
      button:
        text: Download CV
        # 修正：加上开头的斜杠
        url: "/uploads/resume.pdf"
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

  - block: markdown
    content:
      title: '📚 My Research'
      subtitle: ''
      text: |-
        I explore how virtual environments and digital characters can be designed to improve human well-being and social interaction. From investigating user behavior in VR to developing interactive prototypes for digital healthcare, my goal is to create seamless and meaningful experiences. I enjoy combining technical development with empirical user research to understand the impact of emerging technologies on users.
    design:
      columns: '1'

  - block: collection
    id: papers
    content:
      title: Featured Publications
      filters:
        folders:
          - publications  # 如果你的文件夹叫 publications，请在这里加个 s
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
          - publications  # 如果你的文件夹叫 publications，请在这里加个 s
        exclude_featured: false
    design:
      view: citation

# 关键修复：补全结尾横杠，且下方不要有任何文字
---
