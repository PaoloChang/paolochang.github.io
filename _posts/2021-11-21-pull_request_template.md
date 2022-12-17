---
title: "Git: Pull Request and Template"
date: 2021-11-21 12:00:00 -0500
description: paolochang github-blog github blog PR template
categories: [Version Control, Git]
tags: [Git]
---

회사 프로젝트를 진행하면서 많은 배움을 익히고 있는데 그중 하나가 Git의 사용법이다. 이전 회사에서 SVN을 사용사면서 Git을 익힐 기회가 적었뿐더러 개인 프로젝트를 진행하면서 Git을 사용 할 때에는 혼자하는 소꿉놀이 같았다. 옳은 방법, 혹은 잘못된 방법으로 Git을 사용하는지 알려줄 사람이 없었기 때문이다. 오늘은 Git의 사용법에서 **PULL REQUEST** 에 대한 이야기를 서술하려고 한다.

<img src="/assets/img/git_banner.png" alt="Git" width="100%">

## Principal of PR

회사 혹은 프로젝트 마다 사용하는 PR Standard가 다르겠지만 전반적인 사용방법을 이야기한다.

- Title:
  - 새로운 기능을 나타내는 feature, 버그를 고치는 fix등 또한 내포한다.
  - PR의 목적을 간략하게 서술한다.
- Body:
  - Descriptions and Tasks
  - Tickets
  - Checklist
  - PR type (feature, bugfix, chore, others등)
  - Additional information

## PR Template

```md
## Description:

**Implement PR_PURPOSE with following requirements**

- [ ] add_tasks_here

## Checklist

- [ ] Documentation

## Type of PR

- [ ] Feature
- [ ] Bugfix
- [ ] Chore (code style changes, refactoring, tech debt, etc)
- [ ] Other (please describe)

## Screenshots

|         Originial         |         Updated          |
| :-----------------------: | :----------------------: |
| ** original screenshot ** | ** updated screenshot ** |

## Additional Info

- add additional information or context
```

## Merge Process

현재 진행하고 있는 프로젝트에서는 회사에서 제공하는 테스트 툴이 있는데 이곳에서 요구하는 테스트들을 통과하고 code review를 통과해야 merge 할 수 있다.

- **Lint Code Style**
- Jest와 Enzyme을 사용한 **Test Script**
- **Semantic Pull Request** 라고해서 PR title에 꼭 feature 혹은 bugfix 등 PR의 목적을 표기해야 한다.

## References:

- [Better Pull Requests - GitHub Pull Request Templates - GitHub Project Management Tutorial](https://www.youtube.com/watch?v=18E6o-YiP4o&t=189s)
