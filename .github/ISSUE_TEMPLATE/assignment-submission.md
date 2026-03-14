---
name: 作业提交
description: 提交 Quarto 个人网站作业
title: "【作业提交】学号 - 姓名"
labels: ["assignment"]
body:
  - type: input
    id: student_id
    attributes:
      label: 学号
      description: 请输入你的学号
      placeholder: "202430301XXXX"
    validations:
      required: true
  - type: input
    id: name
    attributes:
      label: 姓名
      description: 请输入你的姓名
      placeholder: "张三"
    validations:
      required: true
  - type: input
    id: website_url
    attributes:
      label: 网站链接
      description: 请输入你的 GitHub Pages 网站链接
      placeholder: "https://yourusername.github.io/repo-name/"
    validations:
      required: true
  - type: checkboxes
    id: checklist
    attributes:
      label: 作业要求检查清单
      description: 请确认你的作业满足以下要求
      options:
        - label: 使用 Quarto 创建个人网站
          required: true
        - label: 包含至少两个页面（首页 + 关于）
          required: true
        - label: 已渲染并发布到 GitHub Pages
          required: true
