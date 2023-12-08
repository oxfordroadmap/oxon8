---
title: 项目与产品--澳恪森进行中与已完成的项目

# Listing view
view: showcase

# Optional banner image (relative to `assets/media/` folder).
banner:
  caption: '荔枝_扇面'
  image: 'Lychees.jpg'


sections:
  - block: collection
    id: 'project'
    content:
      title: '项目'
      subtitle: '进行中项目'
      text: 
      # Display content from the `content/project/` folder
      filters:
        folders:
          - project
    design:
      columns: '2'
      view: showcase
      flip_alt_rows: true
  - block: collection
    id: 'project_done'
    content:
      title: '<i class="ai fa-solid fa-list-check">已完成项目'
      subtitle: '已完成项目'
      text: 
      # Display content from the `content/project_done/` folder
      filters:
        folders:
          - project_done
    design:
      columns: '2'
      view: showcase
      flip_alt_rows: true
---


## 产品 <i class="ai ai-dataverse ai-3x fa-spin"></i>

## 已完成项目 <i class="ai fa-solid fa-list-check"></i>